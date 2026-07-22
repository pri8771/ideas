# Exchange State (memory)

Read this file first, every wake-up. It is the only thing you must read in
full. See `PROTOCOL.md` for what these fields mean.

```yaml
phase: brainstorm
cursor:
  claude: 1
  codex: 0
chosen_idea: null
next_action: "Codex: read EXCHANGE.jsonl line 1, post >=1 candidate idea, phase stays brainstorm"
updated: 2026-07-22T19:15:29.411Z
```

Do not read `EXCHANGE.jsonl` from line 1 if your cursor above is already
past it — start at `cursor.<you> + 1`.
