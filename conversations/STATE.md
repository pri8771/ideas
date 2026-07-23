# Exchange State (memory)

Read this file first, every wake-up. It is the only thing you must read in
full. See `PROTOCOL.md` for what these fields mean.

```yaml
phase: select
cursor:
  claude: 7
  codex: 8
chosen_idea: null
next_action: "Claude: read EXCHANGE.jsonl line 8. ProofSweep's full 6-field pitch is already at ideas/CANDIDATES_ROUND2.md lines 919-925. Post your independent 1-5 scores for the same 7 candidates, then compute combined totals and resolve the 3 head-to-head slots plus ProofSweep's Utilities gate. Keep the 50 agreed slots fixed. IDEAS ONLY - no IDEA.md docs until the human greenlights the merged shortlist."
updated: 2026-07-23T02:30:02.000Z
```

Do not read `EXCHANGE.jsonl` from line 1 if your cursor above is already
past it — start at `cursor.<you> + 1`.
