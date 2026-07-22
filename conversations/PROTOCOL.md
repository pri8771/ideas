---
id: DOC-PROTOCOL
canonicalFor: claude-codex-exchange-protocol
status: active
lastVerified: 2026-07-22
owners: [claude, codex]
readWhen:
  - joining this repo for the first time
  - resuming after the other agent has posted
related:
  - conversations/STATE.md
  - conversations/EXCHANGE.jsonl
  - conversations/EXCHANGE.md
supersedes: []
---

# Claude ↔ Codex Exchange Protocol

## Purpose

Let Claude and Codex jointly brainstorm iOS app ideas, pick one without
either agent unilaterally favoring its own suggestion, and document it to
the standard the `iOS_app_factory_rules` control plane expects — all
through committed files, since the two agents never share a live session
and are each woken on a schedule (roughly every 30 minutes) to check for
new turns.

## Files

| File | Purpose | Who reads it fully |
|---|---|---|
| `STATE.md` | Durable memory: phase, cursors, chosen idea, next action | Everyone, every wake-up, in full (it's tiny) |
| `EXCHANGE.jsonl` | Machine channel of record. One compact JSON object per line = one turn. Append-only, never edited or reordered. | Only from your cursor onward |
| `EXCHANGE.md` | Human-readable mirror of the same turns, regenerated/appended alongside the jsonl | The human user only |
| `ideas/README.md` | Index of all candidate/selected ideas | When entering `select` or `document` phase |
| `ideas/NNNN-<slug>/IDEA.md` | Final documentation for a chosen idea | When entering `document` phase |

**Token discipline:** never re-read `EXCHANGE.jsonl` from the start. Read
`STATE.md` first; it tells you your last-processed line number. Read only
new lines past it. Update your cursor in `STATE.md` after processing.

## Turn record (EXCHANGE.jsonl)

One line per turn, JSON, keys kept short on purpose:

```json
{"n":3,"to":"codex","from":"claude","ts":"2026-07-22T19:42:07.123Z","day":"Monday","agent":"claude-sonnet-5/medium","phase":"brainstorm","msg":"..."}
```

- `n` — 1-indexed line number, matches physical line number in the file.
- `to` / `from` — `"claude"` or `"codex"`.
- `ts` — RFC3339 UTC timestamp, millisecond precision.
- `day` — full weekday name, redundant with `ts` but kept for cheap human
  scanning without a date parser.
- `agent` — `"<model>/<effort-or-reasoning-level>"` self-reported by the
  posting agent.
- `phase` — the phase this turn belongs to: `brainstorm` | `select` |
  `document` | `done`.
- `msg` — the actual content. Free text or compact markdown. Terse is
  fine — this channel does not need to be pretty, only unambiguous.

## Human mirror (EXCHANGE.md)

Every append to `EXCHANGE.jsonl` gets a matching block appended to
`EXCHANGE.md` in this exact framing (per the user's requested format):

```text
---

To Codex, Monday, 2026-07-22, 19:42:07.123 UTC

<msg, rendered as normal markdown>

— Claude (claude-sonnet-5 / medium)

---
```

Swap `To Codex,` / `To Claude,` and the trailing attribution depending on
`from`. Always UTC, always millisecond precision, always full weekday
name, matching `STATE.md`'s clock rules.

## STATE.md (memory)

Kept under ~30 lines at all times. Holds:

- `phase`: current workflow phase.
- `cursor.claude` / `cursor.codex`: last `n` each agent has fully
  processed (i.e., safe to skip on next read).
- `chosen_idea`: null until `select` phase concludes, then the idea slug.
- `next_action`: one line, whoever should act next and what for.
- `updated`: timestamp of last edit to this file.

Whoever posts a turn updates their own cursor and `next_action` in the
same commit. Never let `STATE.md` drift from what `EXCHANGE.jsonl`
actually contains.

## Phases

### 1. `brainstorm`

Each agent posts at least one candidate iOS app idea as a turn (title +
2-4 sentence pitch). Either agent may riff on the other's ideas. No
commitment yet. Move to `select` once there are at least 3 distinct
candidates and neither agent has posted a new one in its last turn (i.e.
both sides signaled "no more ideas" — say so explicitly in `msg`).

### 2. `select` — unbiased choice

To avoid either agent's chosen idea winning just because it proposed it:

1. List every distinct candidate in `ideas/README.md`'s candidate table.
2. Each agent independently scores **every** candidate 1-5 on four fixed
   criteria: `market_need`, `feasibility_for_one_dev`, `novelty`,
   `monetization_potential`. Post scores as a turn — do not read the other
   agent's scores before posting your own (if the other agent already
   posted its scores when you wake up, that's fine, you're not colluding,
   just don't revise yours after seeing them).
3. Sum all 8 numbers (4 criteria × 2 agents) per candidate. Highest total
   wins.
4. Tie-break, in order, until broken: (a) higher sum of
   `feasibility_for_one_dev` across both agents; (b) earlier candidate by
   posting order (lower `n` of its first mention).
5. Whoever computes the final tally posts the result as a turn with
   `phase:"select"` and the winning slug, and sets `chosen_idea` in
   `STATE.md`. The other agent should sanity-check the arithmetic on its
   next wake-up and either confirm or flag a dispute as a turn — do not
   silently redo the whole vote.

### 3. `document`

Winning idea gets a full `ideas/NNNN-<slug>/IDEA.md` per
`ideas/_TEMPLATE/IDEA.md` and the central
`standards/documentation/LLM_DOCUMENTATION_STANDARD.md`. Either agent may
draft it; the other reviews on its next wake-up and either approves (turn
with `phase:"document"`, `msg` starting `APPROVED`) or requests changes.

### 4. `done`

Once both agents have approved the documented idea, post a `phase:"done"`
turn, set `STATE.md.phase: done` and `next_action: none — awaiting human`.
Do not start a new idea cycle automatically; wait for the human to
re-open (e.g. by editing `STATE.md.phase` back to `brainstorm` or asking
directly).

## Bootstrapping a new cycle

To start over for a new idea after `done`, the human (or an explicit
instruction) resets `STATE.md`: `phase: brainstorm`, clears
`chosen_idea`, leaves cursors as-is (history is never deleted).
