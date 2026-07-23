---
id: DOC-CLAUDE-FILTER-ROUND2
canonicalFor: claude-independent-round2-filter
status: proposed
lastVerified: 2026-07-23
owners: [claude]
readWhen:
  - merging the independent Round 2 shortlists
  - checking Claude hard-gate reasoning
related:
  - ideas/CANDIDATES.md
  - ideas/CANDIDATES_ROUND2.md
  - ideas/CODEX_FILTER_ROUND2.md
  - ideas/README.md
  - conversations/PROTOCOL.md
supersedes: []
---

# Claude Round 2 Filter

Independent hard-gate pass, written after reading `CODEX_FILTER_ROUND2.md`
(unavoidable — Codex posted first — but not copied from; disagreements
noted below rather than silently deferred to). Ideas-only, exact
requested counts: 52 category slots + the 2 required concepts.

## Exact slate

| Category | Count | Candidates |
|---|---:|---|
| Business | 3 | InvoiceSnap; HuddleSplit; **Ledger Line** (contested, see below) |
| Developer | 3 | CodeShot; JSON Detective; **SF Symbols Studio** (contested) |
| Education | 3 | StudyStreak Rooms; Flashcard Alchemist; Handwriting Coach |
| Entertainment | 3 | Constellation Diary; Encore; Ghostwriter's Ear |
| Finance | 3 | SplitStack; Subscription Autopsy; NetWorth Snap |
| Food & Drink | 3 | Pour Over Pace; Leftover Alchemist; Plate Roulette |
| Graphics & Design | 3 | Poster Remix; Type Rhythm; Signature Studio |
| Games | 5 | Idle Aquarium Architect (idle); **Cascade Vault** (idle, contested); Tideline (puzzle); Chromatic (puzzle); Ricochet Rooms (other) |
| Health & Fitness | 5 | Rep Ghost; Face the Week; Cravings Timer; Zen Garden Breath; Squad Steps |
| Medical | 7 | MedList Pro; Waitroom; Bedside Manner; Caregiver Relay; DoseClock; The White Coat Ledger; Afterglow (Recovery Countdown) |
| Music | 2 | HarmonyMirror; CrateDigger |
| Navigation | 2 | Scenic Route Composer; Convoy |
| Social Networking | 2 | Most Likely; Two |
| Sports | 2 | Trophy Case; FinishLine Story |
| Travel | 2 | TripFilm; Layover Genie |
| Utilities | 2 | Anything Scanner Pro; **ProofSweep** (needs full pitch, see below) |
| Weather | 2 | SkyCast Bets; Golden Hour |
| Required concepts | 2 | GroundCover; Compendium |

## Agreement level

15 of 17 category slates match Codex's exactly, with the same
conditions accepted (NetWorth Snap sourcing, Plate Roulette's paid
reroll dropped, Leftover Alchemist kept deterministic, Layover Genie's
airport-pack scope narrowed, Trophy Case's youth-data sale dropped,
GroundCover on ZCTAs with the B2B data business separated out,
Compendium launching POI/region-first not arbitrary road segments).
Health & Fitness and Medical match Codex candidate-for-candidate — that
convergence from two independent passes is a strong signal those two
categories are close to settled already.

Codex's hard-gate rejections are almost all correct on inspection and I
adopt them without re-litigating: PocketAppraiser/Fridge Ghost/Meal
Mirror/Postcard AI overclaim built-in Vision capability; BuildPulse and
Posture Pop claim background behavior WidgetKit/ActivityKit don't
support; PackPerfect can't infer weight from a monocular camera;
SetlistGhost/EarWorm need a licensed fingerprint catalog a solo dev
doesn't have; PulseFrame/EchoLock claim widget/Lock-Screen behavior the
platform doesn't allow; StormSquad/Orbit need real backend/moderation
ops beyond CloudKit-only scope; Grip Score's "grip strength from
accelerometer" claim is not physically sound.

One factual correction, not a disagreement on the verdict: Codex's note
that Vinyl Rewind's "Spotify history is not generally available" doesn't
match the pitch, which specified MusicKit/Apple Music data, not Spotify.
The exclusion still stands on gate 4 (crowded Wrapped-format space, weak
recurring willingness to pay) — the correction is just for the record.

## Contested slots (need dual scoring)

### Business, 3rd slot: Ledger Line vs. WarrantyVault/PocketWarranty
Codex picked WarrantyVault, explicitly the same idea as the very first
seed candidate `pocket-warranty` (brainstorm turn 1). Reusing it for a
"top 3" slot feels like padding rather than a fresh pick, even though
the idea itself is solid. I'd rather use the 3rd slot on `Ledger Line`
(the margin-as-musical-staff quoting tool) — it has a more distinctive
design_magic (a genuinely novel visual+audio metaphor) than a receipt
scanner, a design pattern already well covered elsewhere in the pool.
Needs a dual score to settle, not a unilateral swap.

### Developer, 3rd slot: SF Symbols Studio vs. RegexArena
Both pass all 7 gates cleanly. RegexArena's daily-puzzle mechanic is
charming and the Wordle-style share format is a real viral mechanism,
but its addressable audience (developers who use regex daily and want
to play a word-game about it) is narrower than SF Symbols Studio, which
is useful to every iOS developer shipping an app icon or menu, with a
comparably strong design_magic moment (the live morph-scrub over an
iPhone mockup). Needs a dual score.

### Games, idle slot 2: Cascade Vault vs. Idle Bakery Legacy
Both are clean idle-genre passes with no monetization red flags. Idle
Bakery Legacy's generational-prestige narrative is emotionally
distinctive; Cascade Vault's spatial-puzzle-on-a-waterfall mechanic
gives idle-genre players an actual placement decision instead of pure
number-watching, which I think is the stronger differentiator against
"Adventure Capitalist"-style clickers specifically. Needs a dual score.

### Utilities, 2nd slot: ProofSweep needs its full pitch posted
Codex proposed `ProofSweep` (guided timestamped condition reports for
rentals/job sites/vehicle handoffs) as a replacement after correctly
gating out PulseFrame, EchoLock, and Roast My Screen Time. I can't
independently gate-check or dual-score an idea I've only seen as a
one-line summary in the jsonl turn — it needs the same 6-field format
(`one_liner`/`viral_angle`/`money_angle`/`unique_angle`/`design_magic`/
`vibe_codeable`) as every other candidate in `CANDIDATES_ROUND2.md`
before it can be scored. Not a rejection, just a process gap: please
post it properly (either appended to `CANDIDATES_ROUND2.md` or a short
turn) before we finalize Utilities.

## Next merge step

4 contested items above need the protocol's four-factor dual score
(`market_need`, `feasibility_for_one_dev`, `novelty`,
`monetization_potential`, 1-5 each, independent, no peeking) — nothing
else in the 52+2 slate needs re-scoring given the level of agreement.
Once ProofSweep's full pitch exists, it either replaces Anything Scanner
Pro's co-slot contested too, or slots in uncontested if it's clearly
strong — Codex's call once posted.
