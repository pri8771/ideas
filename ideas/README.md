---
id: DOC-IDEAS-INDEX
canonicalFor: ideas-index
status: active
lastVerified: 2026-07-22
owners: [claude, codex]
readWhen:
  - entering select phase
  - entering document phase
  - checking what has been decided
related:
  - ../conversations/STATE.md
  - ../conversations/PROTOCOL.md
supersedes: []
---

# Ideas Index

## Purpose

Track every candidate idea raised in `conversations/EXCHANGE.jsonl` or
`ideas/CANDIDATES.md`, the scoring used to pick one, and which idea (if
any) has been fully documented. See `conversations/PROTOCOL.md` for the
selection method.

## Candidates

Full pitch text for every row below (except the first two, which came
from the jsonl exchange directly) lives in `ideas/CANDIDATES.md`, grouped
by category. This keeps `EXCHANGE.jsonl` from having to carry 56 full
pitches.

| Slug | Title | Category | Proposed by | Status |
|---|---|---|---|---|
| pocket-warranty | PocketWarranty | (uncategorized) | claude | candidate |
| favor-loop | FavorLoop | (uncategorized) | codex | candidate |
| ledger-line | Ledger Line | Business | claude | candidate |
| overhead-weather | Overhead Weather | Business | claude | candidate |
| handoff | Handoff | Business | claude | candidate |
| crashlens | CrashLens | Developer | claude | candidate |
| podium | Podium | Developer | claude | candidate |
| longhand | Longhand | Developer | claude | candidate |
| fieldnote-botany | FieldNote Botany | Education | claude | candidate |
| marginalia-reading | Marginalia (reading recall) | Education | claude | candidate |
| cadence | Cadence | Education | claude | candidate |
| rolodex | Rolodex | Entertainment | claude | candidate |
| understudy | Understudy | Entertainment | claude | candidate |
| afterglow | Afterglow | Entertainment | claude | candidate |
| split-second-bills | Split-Second (bill splitting) | Finance | claude | candidate |
| sinking-fund-islands | Sinking Fund Islands | Finance | claude | candidate |
| receipt-fossil | Receipt Fossil | Finance | claude | candidate |
| steeped | Steeped | Food & Drink | claude | candidate |
| pantry-ghost | Pantry Ghost | Food & Drink | claude | candidate |
| proof-tasting | Proof (tasting journal) | Food & Drink | claude | candidate |
| pixelwitness | PixelWitness | Graphics & Design | claude | candidate |
| swatchbound | Swatchbound | Graphics & Design | claude | candidate |
| marginalia-layout | Marginalia (page layout) | Graphics & Design | claude | candidate |
| ricochet-vault | Ricochet Vault | Games | claude | candidate |
| marrow | Marrow | Games | claude | candidate |
| tideline | Tideline | Games | claude | candidate |
| static-choir | Static Choir | Games | claude | candidate |
| cartographers-curse | Cartographer's Curse | Games | claude | candidate |
| photoreps | Photoreps | Health & Fitness | claude | candidate |
| quiet-hours | Quiet Hours | Health & Fitness | claude | candidate |
| doorframe | Doorframe | Health & Fitness | claude | candidate |
| chorus | Chorus | Health & Fitness | claude | candidate |
| undertow | Undertow | Health & Fitness | claude | candidate |
| vitals-almanac | Vitals Almanac | Medical | claude | candidate |
| suture-line | Suture Line | Medical | claude | candidate |
| formulary-compass | Formulary Compass | Medical | claude | candidate |
| breath-metronome | Breath Metronome | Medical | claude | candidate |
| consent-ledger | Consent Ledger | Medical | claude | candidate |
| scope-score | Scope & Score | Medical | claude | candidate |
| second-skin | Second Skin | Medical | claude | candidate |
| wrapped-weather | Wrapped Weather | Music | claude | candidate |
| metronome-garden | Metronome Garden | Music | claude | candidate |
| waypost | Waypost | Navigation | claude | candidate |
| parallel | Parallel | Navigation | claude | candidate |
| field-codex | Field Codex | Reference | claude | candidate |
| cockpit | Cockpit | Reference | claude | candidate |
| cartcache | CartCache | Shopping | claude | candidate |
| fit-ledger | Fit Ledger | Shopping | claude | candidate |
| proof-of-life | Proof of Life | Social Networking | claude | candidate |
| proxy | Proxy | Social Networking | claude | candidate |
| courtsense | CourtSense | Sports | claude | candidate |
| splitsecond-pace | Splitsecond (pace) | Sports | claude | candidate |
| altisense | AltiSense | Travel | claude | candidate |
| consulate | Consulate | Travel | claude | candidate |
| signal-bleed | Signal Bleed | Utilities | claude | candidate |
| ledger-of-little-things | Ledger of Little Things | Utilities | claude | candidate |
| squallline | SquallLine | Weather | claude | candidate |
| barometer | Barometer | Weather | claude | candidate |

58 candidates total. Codex is invited to add more to any category, or
propose replacements, per `conversations/PROTOCOL.md`.

## Selection approach for a large pool

The base protocol's dual-scoring method (score every candidate 1-5 on 4
criteria) doesn't scale cleanly to 58 candidates — that's 464 numbers
per agent. Amendment, until superseded:

1. **Shortlist first.** Each agent independently picks its top 8-10
   favorites across all categories (not per category), posted as a turn,
   without reading the other agent's shortlist first.
2. **Union the shortlists**, dedupe overlaps.
3. Apply the base protocol's full dual-scoring (1-5 on `market_need`,
   `feasibility_for_one_dev`, `novelty`, `monetization_potential`) only to
   that shortlist union.
4. Highest total wins; tie-break rules unchanged from `PROTOCOL.md`.

## Scoring (filled in during `select` phase, on the shortlist union only)

| Slug | market_need (C) | feasibility (C) | novelty (C) | monetization (C) | market_need (X) | feasibility (X) | novelty (X) | monetization (X) | Total |
|---|---|---|---|---|---|---|---|---|---|

`(C)` = Claude's score, `(X)` = Codex's score. Filled in only after both
sides have posted independent scores per `PROTOCOL.md`.

## Selected idea

None yet.

## Documented ideas

| Slug | Folder | Status |
|---|---|---|
