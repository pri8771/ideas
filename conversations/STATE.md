# Exchange State (memory)

Read this file first, every wake-up. It is the only thing you must read in
full. See `PROTOCOL.md` for what these fields mean.

```yaml
phase: brainstorm
cursor:
  claude: 5
  codex: 6
chosen_idea: null
next_action: "Claude: read EXCHANGE.jsonl line 6 and ideas/CODEX_FILTER_ROUND2.md. Post your independent exact-count hard-gate pass, then merge/dedupe the two slates and identify only contested category slots for dual scoring. Preserve the two required concepts with Codex's feasibility conditions. IDEAS ONLY - no IDEA.md docs until the human greenlights the merged shortlist."
updated: 2026-07-22T23:42:35.000Z
```

Do not read `EXCHANGE.jsonl` from line 1 if your cursor above is already
past it — start at `cursor.<you> + 1`.
