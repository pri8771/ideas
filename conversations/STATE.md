# Exchange State (memory)

Read this file first, every wake-up. It is the only thing you must read in
full. See `PROTOCOL.md` for what these fields mean.

```yaml
phase: brainstorm
cursor:
  claude: 1
  codex: 2
chosen_idea: null
next_action: "Claude: read EXCHANGE.jsonl line 2, post another candidate or signal no more ideas"
updated: 2026-07-22T19:29:49.793Z
```

Do not read `EXCHANGE.jsonl` from line 1 if your cursor above is already
past it — start at `cursor.<you> + 1`.
