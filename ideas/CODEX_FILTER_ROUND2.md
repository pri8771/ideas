---
id: DOC-CODEX-FILTER-ROUND2
canonicalFor: codex-independent-round2-filter
status: proposed
lastVerified: 2026-07-22
owners: [codex]
readWhen:
  - merging the independent Round 2 shortlists
  - checking Codex hard-gate objections
related:
  - ideas/CANDIDATES_ROUND2.md
  - ideas/README.md
  - conversations/PROTOCOL.md
supersedes: []
---

# Codex Round 2 Filter

This is Codex's independent hard-gate pass. It is an ideas-only shortlist,
not selection scoring or `IDEA.md` documentation. The slate contains the
exact 52 requested category slots plus the 2 required concepts.

## Exact slate

| Category | Count | Candidates |
|---|---:|---|
| Business | 3 | InvoiceSnap; WarrantyVault / PocketWarranty (dedupe); HuddleSplit |
| Developer | 3 | CodeShot; RegexArena; JSON Detective |
| Education | 3 | StudyStreak Rooms; Flashcard Alchemist; Handwriting Coach |
| Entertainment | 3 | Ghostwriter's Ear; Constellation Diary; Encore |
| Finance | 3 | SplitStack; Subscription Autopsy; NetWorth Snap |
| Food & Drink | 3 | Plate Roulette; Pour Over Pace; Leftover Alchemist |
| Graphics & Design | 3 | Signature Studio; Poster Remix; Type Rhythm |
| Games | 5 | Idle Aquarium Architect (idle); Idle Bakery Legacy (idle); Tideline (puzzle); Chromatic (puzzle); Ricochet Rooms (other) |
| Health & Fitness | 5 | Rep Ghost; Face the Week; Cravings Timer; Squad Steps; Zen Garden Breath |
| Medical | 7 | MedList Pro; Waitroom; Bedside Manner; Caregiver Relay; DoseClock; Afterglow (Recovery Countdown); The White Coat Ledger |
| Music | 2 | HarmonyMirror; CrateDigger |
| Navigation | 2 | Scenic Route Composer; Convoy |
| Social Networking | 2 | Most Likely; Two |
| Sports | 2 | Trophy Case; FinishLine Story |
| Travel | 2 | TripFilm; Layover Genie |
| Utilities | 2 | Anything Scanner Pro; ProofSweep |
| Weather | 2 | SkyCast Bets; Golden Hour |
| Required concepts | 2 | GroundCover; Compendium |

## Conditions before scoring

- **NetWorth Snap:** source and date the percentile tables; do not imply a
  defensible percentile from ten vague sliders.
- **Plate Roulette:** remove the paid reroll. Sell durable taste profiles,
  dietary packs, and group mode so monetization is not pay-to-undo-randomness.
- **Leftover Alchemist:** keep ingredient entry/scanning deterministic and
  recipe-backed; do not promise arbitrary AI recipe invention.
- **Flashcard Alchemist:** support deterministic PDF/text extraction and make
  Foundation Models an enhancement, not a minimum-device dependency.
- **Scenic Route Composer:** score only routes returned by MapKit in v1; do
  not claim a new routing engine or guaranteed scenic correctness.
- **Layover Genie:** launch with a small, excellent airport pack. The claimed
  400-airport curated corpus is not solo-developer scope.
- **Trophy Case:** subscription, card packs, and print margin are enough.
  Drop sale of youth-performance data; it adds trust and compliance cost
  without strengthening the core business.
- **GroundCover:** treat ZIPs as Census ZCTAs, define a visit from recorded GPS
  samples, and separate the sellable subscription/poster MVP from any B2B
  movement-data business, which would require backend aggregation and consent.
- **Compendium:** ship selectable POIs and administrative regions first.
  Arbitrary road-segment selection and road-level Wikipedia matching require
  map data/indexing that MapKit does not provide directly.

## Representative hard-gate failures

- **PocketAppraiser, Fridge Ghost, Meal Mirror, Postcard AI:** gate 6. Apple's
  built-in Vision APIs do not supply the promised arbitrary-item valuation,
  reliable pantry/meal understanding, or general painterly style transfer.
- **BuildPulse:** gate 6. A Live Activity cannot continuously poll CI in the
  background as pitched; timely remote updates need a push/provider service.
- **GitWrapped, Vinyl Rewind, Palette Cam / Palette Alchemist:** gate 4 or 3.
  These are crowded Wrapped/palette formats with weak recurring willingness
  to pay; Spotify history is also not generally available as pitched.
- **PocketProf:** gate 6. OCR-to-correct narrated animated lessons for arbitrary
  textbook material is substantially beyond an on-device solo MVP.
- **PocketPitch, TipJar Karma, BoardroomBingo:** gate 5. The novelty is clearer
  than durable utility or entertainment retention.
- **Posture Pop:** gate 6. iOS does not permit periodic background front-camera
  posture watching through a Live Activity.
- **Grip Score:** gates 4 and 5. Motion sensors cannot measure grip strength;
  labeling the result a fitness-age score would be misleading.
- **Second Opinion Scanner, Symptom Weather:** gate 5. Lab ranges are
  context-dependent and symptom "forecasts" risk presenting decoration as
  medical interpretation.
- **SetlistGhost, EarWorm:** gate 6. On-device fingerprinting still needs a
  licensed/catalog-scale reference database; a local hash lookup is not one.
- **MirrorMe:** gate 6. It explicitly requires an LLM API and creates keyboard
  extension review/trust complexity. **Orbit** also needs moderation and a
  geo/social backend beyond credible CloudKit-only scope.
- **PackPerfect:** gate 6. A monocular phone camera cannot reliably infer bag
  fit and weight. **PulseFrame** and **EchoLock** fail for similar platform
  reasons: widgets/Lock Screens cannot run the promised continuous arbitrary
  animation or microphone-reactive wallpaper behavior.
- **StormSquad:** gate 6. Real-time public incident media requires moderation,
  abuse handling, and operational infrastructure, not just CloudKit records.

## Next merge step

Claude should post an independent exact-count pass, then merge the two slates.
Only the union/contested slots should receive the protocol's four-factor dual
scores. The two required concepts remain included, with feasibility narrowed
as above, regardless of category math.
