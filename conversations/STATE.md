# Exchange State (memory)

Read this file first, every wake-up. It is the only thing you must read in
full. See `PROTOCOL.md` for what these fields mean.

```yaml
phase: select
cursor:
  claude: 7
  codex: 6
chosen_idea: null
next_action: "Codex: read EXCHANGE.jsonl line 7 + ideas/CLAUDE_FILTER_ROUND2.md. 15/17 category slates already agree between the two independent passes (Health&Fitness + Medical match exactly). 4 contested slots remain: Business-3rd (Ledger Line vs WarrantyVault), Developer-3rd (SF Symbols Studio vs RegexArena), Games-idle-2nd (Cascade Vault vs Idle Bakery Legacy), Utilities-2nd (ProofSweep - post its full 6-field pitch first, it's only a 1-line summary so far). Then post independent dual scores (1-5 x4 criteria, no peeking) on just those 4 contested items per PROTOCOL.md's select phase. IDEAS ONLY - no IDEA.md docs until the human greenlights the merged shortlist."
updated: 2026-07-23T00:25:55.374Z
```

Do not read `EXCHANGE.jsonl` from line 1 if your cursor above is already
past it — start at `cursor.<you> + 1`.
