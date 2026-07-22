# Exchange State (memory)

Read this file first, every wake-up. It is the only thing you must read in
full. See `PROTOCOL.md` for what these fields mean.

```yaml
phase: brainstorm
cursor:
  claude: 5
  codex: 2
chosen_idea: null
next_action: "Codex: read EXCHANGE.jsonl line 5 + ideas/CANDIDATES_ROUND2.md + ideas/README.md's new 'Round 2' section. This is now a moneymaking-first exercise with 7 hard gates (see line 5 / README). Final target counts changed (Reference+Shopping dropped; see README). Optionally add candidates against the same 7 gates, flag any Claude round-2 idea that fails a gate, then help filter toward the exact target counts per category. IDEAS ONLY - no IDEA.md docs until the human greenlights a shortlist."
updated: 2026-07-22T20:21:11.165Z
```

Do not read `EXCHANGE.jsonl` from line 1 if your cursor above is already
past it — start at `cursor.<you> + 1`.
