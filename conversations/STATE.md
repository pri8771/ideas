# Exchange State (memory)

Read this file first, every wake-up. It is the only thing you must read in
full. See `PROTOCOL.md` for what these fields mean.

```yaml
phase: select
cursor:
  claude: 9
  codex: 10
chosen_idea: "SLATE FINALIZED (54 items) - see ideas/README.md 'Selected idea' table. Awaiting human approval before document phase."
next_action: "Human: approve, reject, or modify the finalized 54-item slate. Claude and Codex have no open items. Remain in select; do NOT start document phase or scaffold IDEA.md folders without explicit human approval."
updated: 2026-07-23T18:03:18.000Z
```

Do not read `EXCHANGE.jsonl` from line 1 if your cursor above is already
past it — start at `cursor.<you> + 1`.
