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

## Round 2 — moneymaking filter (current)

Per a follow-up human request: the goal is now explicitly revenue and
growth, not a portfolio piece. Round 2 added ~150 more overgenerated
candidates in `ideas/CANDIDATES_ROUND2.md`, screened against 7 hard
gates (an idea failing any one is disqualified, not just noted):

1. Beautifully, magically designed — a specific "aha" moment, not generic "clean UI."
2. Real viral potential — a named, specific mechanism.
3. Monetizes without feeling cheap or scammy — a named mechanism.
4. Genuinely unique — names the cliché/competitor and the differentiator.
5. Not dumb or gimmicky — real utility/entertainment beyond the novelty.
6. Vibe-codeable — one dev, AI-assisted, on-device frameworks, no custom backend/ML training.
7. Privacy is NOT a design constraint — data-driven monetization is fair game where it fits; don't default to privacy caution out of habit.

**Round 2 final targets** (supersedes Round 1 counts where they differ):
3 each for Business/Developer/Education/Entertainment/Finance/Food &
Drink/Graphics & Design; 5 for Games (aiming for ~2 idle + ~2 puzzle +
1 other genre); 5 for Health & Fitness; 7 for Medical; 2 each for Music/
Navigation/Social Networking/Sports/Travel/Utilities/Weather. **Reference
and Shopping are dropped this round** (human's explicit call — Round 1's
entries in those categories remain in the pool but aren't being actively
filtered toward a target). Plus 2 user-specified concept apps
(`GroundCover`, `Compendium` — see `CANDIDATES_ROUND2.md`) that count
regardless of category-slot math.

**No docs yet.** Per the human: this stage is ideas only. `IDEA.md`
documentation only starts after the human greenlights the filtered
shortlist — do not scaffold `ideas/NNNN-<slug>/` folders yet.

Codex's independent exact-count hard-gate pass is in
`ideas/CODEX_FILTER_ROUND2.md`. Claude's independent pass is in
`ideas/CLAUDE_FILTER_ROUND2.md`. The two converged on 15 of 17 category
slates exactly (Health & Fitness and Medical matched candidate-for-
candidate). The remaining 4 contested slots were resolved by dual
scoring — see "Scoring" and "Selected idea" below. **The full slate is
now finalized and posted for human review — it is a proposal, not an
automatic green light to start writing `IDEA.md` docs.**

## Selection approach for a large pool

The base protocol's dual-scoring method (score every candidate 1-5 on 4
criteria) doesn't scale cleanly to 200+ candidates. Amendment, until
superseded:

0. **Hard-gate filter first** (Round 2 only): drop anything failing one
   of the 7 gates above before shortlisting.
1. **Shortlist first.** Each agent independently picks its favorites
   across all categories (not per category) — aiming toward roughly the
   Round 2 final target counts per category — posted as a turn, without
   reading the other agent's shortlist first.
2. **Union the shortlists**, dedupe overlaps (including the near-duplicate
   concepts flagged inline in `CANDIDATES_ROUND2.md`, e.g. `Tideline`
   appearing in both rounds, `Swatchbound`/`Palette Cam`/`Palette
   Alchemist` all being the same idea).
3. Apply the base protocol's full dual-scoring (1-5 on `market_need`,
   `feasibility_for_one_dev`, `novelty`, `monetization_potential`) only to
   that shortlist union.
4. Highest total wins per category slot; tie-break rules unchanged from
   `PROTOCOL.md`.

## Scoring (contested slots only — the other slots were unanimous)

| Candidate | Slot | market_need (C) | feasibility (C) | novelty (C) | monetization (C) | market_need (X) | feasibility (X) | novelty (X) | monetization (X) | Total | Result |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Ledger Line | Business 3rd | 3 | 5 | 5 | 3 | 3 | 5 | 5 | 3 | 32 | loses tie-break |
| WarrantyVault | Business 3rd | 4 | 5 | 3 | 4 | 4 | 5 | 3 | 4 | 32 | **wins** (tie-break b: earlier posting order, n:1 vs n:4) |
| SF Symbols Studio | Developer 3rd | 3 | 2 | 3 | 4 | 4 | 2 | 3 | 4 | 25 | loses |
| RegexArena | Developer 3rd | 3 | 5 | 4 | 3 | 3 | 5 | 4 | 3 | 30 | **wins** |
| Idle Bakery Legacy | Games idle 2nd | 4 | 5 | 3 | 4 | 4 | 5 | 4 | 4 | 33 | loses |
| Cascade Vault | Games idle 2nd | 4 | 4 | 5 | 4 | 4 | 4 | 5 | 4 | 34 | **wins** |
| ProofSweep | Utilities 2nd | 5 | 4 | 4 | 5 | 5 | 4 | 4 | 5 | 36 | **confirmed** |

`(C)` = Claude's score, `(X)` = Codex's score.

## Selected idea

**Status: finalized slate, proposed to the human — awaiting explicit
approval before any `IDEA.md` documentation begins.** Per
`conversations/PROTOCOL.md`'s `select` phase, this is a multi-app slate
(54 items: 52 category slots + 2 required concepts), not a single
winner.

| Category | Selected |
|---|---|
| Business | InvoiceSnap · HuddleSplit · WarrantyVault |
| Developer | CodeShot · JSON Detective · RegexArena |
| Education | StudyStreak Rooms · Flashcard Alchemist · Handwriting Coach |
| Entertainment | Ghostwriter's Ear · Constellation Diary · Encore |
| Finance | SplitStack · Subscription Autopsy · NetWorth Snap |
| Food & Drink | Plate Roulette · Pour Over Pace · Leftover Alchemist |
| Graphics & Design | Signature Studio · Poster Remix · Type Rhythm |
| Games | Idle Aquarium Architect (idle) · Cascade Vault (idle) · Tideline (puzzle) · Chromatic (puzzle) · Ricochet Rooms (other) |
| Health & Fitness | Rep Ghost · Face the Week · Cravings Timer · Squad Steps · Zen Garden Breath |
| Medical | MedList Pro · Waitroom · Bedside Manner · Caregiver Relay · DoseClock · Afterglow (Recovery Countdown) · The White Coat Ledger |
| Music | HarmonyMirror · CrateDigger |
| Navigation | Scenic Route Composer · Convoy |
| Social Networking | Most Likely · Two |
| Sports | Trophy Case · FinishLine Story |
| Travel | TripFilm · Layover Genie |
| Utilities | Anything Scanner Pro · ProofSweep |
| Weather | SkyCast Bets · Golden Hour |
| Required concepts | GroundCover · Compendium |

Full pitches for every one of these: `ideas/CANDIDATES_ROUND2.md` (and
`ideas/CANDIDATES.md` for anything carried over from Round 1). Feasibility
conditions attached to specific ideas during filtering (e.g. GroundCover
using ZCTAs, Compendium launching POI/region-first, Plate Roulette
dropping the paid reroll, Layover Genie scoping to a small airport pack)
are recorded in `ideas/CODEX_FILTER_ROUND2.md`'s "Conditions before
scoring" section and should carry into each idea's eventual `IDEA.md`.

## Documented ideas

| Slug | Folder | Status |
|---|---|---|
