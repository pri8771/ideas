# Agent Instructions — Ideas Lab

## Repository identity

This repository is a pre-product ideation lab, governed at the `idea` /
`research` stages of the lifecycle defined by the central control plane
`pri8771/iOS_app_factory_rules`. It is not a product repository: it holds
no application source code. Its output is a documented, selected iOS app
idea, ready to be handed to `playbooks/START_NEW_PROJECT.md` in the rules
repo when someone decides to build it.

Read `pri8771/iOS_app_factory_rules` `LLM_START_HERE.md` and
`governance/PROJECT_LIFECYCLE.md` if you need lifecycle context. Do not
duplicate that repository's content here — link to it.

## Two agents, one file

This repo is jointly operated by two agents — **Claude** and **Codex** —
who do not share a live channel. They communicate only through committed
files in `conversations/`. Treat repository state as the only durable
memory: do not assume the other agent's private chat history exists.

Before doing anything else in this repo:

1. Read `conversations/STATE.md` (small — durable memory: current phase,
   cursors, chosen idea if any). This alone tells you whether there is
   anything new to read.
2. If `STATE.md` says your cursor is behind, read only
   `conversations/EXCHANGE.jsonl` **from your cursor line onward** — never
   re-read lines already behind your cursor. Use `tail -n +<cursor+1>` or
   equivalent.
3. Do not read `conversations/EXCHANGE.md` for decision-making — it is the
   human-readable mirror only, regenerated from the jsonl. Reading it costs
   more tokens for the same information.
4. Full protocol: `conversations/PROTOCOL.md`.

## Workflow phases

`brainstorm → select → document → done` (see `conversations/PROTOCOL.md`
for the exact rules of each phase, including the unbiased-selection
method). `STATE.md.phase` is the authoritative current phase.

## Documentation rules for a chosen idea

Once an idea is selected, write it to `ideas/NNNN-<slug>/IDEA.md` using
`ideas/_TEMPLATE/IDEA.md`. Follow the central
`standards/documentation/LLM_DOCUMENTATION_STANDARD.md`: metadata header,
facts vs. decisions vs. assumptions vs. proposals kept distinct, proposals
under an explicit "not approved" heading, controlled status vocabulary.
Update `ideas/README.md`'s index in the same change.

Do not scaffold app source code here. This repo stops at a documented,
selected idea.
