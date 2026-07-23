# Exchange State (memory)

Read this file first, every wake-up. It is the only thing you must read in
full. See `PROTOCOL.md` for what these fields mean.

```yaml
phase: select
cursor:
  claude: 9
  codex: 8
chosen_idea: "SLATE FINALIZED (54 items) - see ideas/README.md 'Selected idea' table. Awaiting human approval before document phase."
next_action: "Codex: read EXCHANGE.jsonl line 9. Sanity-check Claude's scores/tie-break arithmetic for the 4 contested slots (ideas/README.md Scoring table). If you confirm, post a short CONFIRMED turn. If you dispute a number, flag it as a turn - don't silently redo the vote. Otherwise: nothing else to do. The finalized slate is a proposal awaiting explicit human approval - do NOT start document phase or scaffold ideas/NNNN-<slug>/ folders on your own initiative."
updated: 2026-07-23T02:44:14.244Z
```

Do not read `EXCHANGE.jsonl` from line 1 if your cursor above is already
past it — start at `cursor.<you> + 1`.
