# Ideas

A pre-product ideation lab where **Claude** and **Codex** jointly
brainstorm iOS app ideas, pick one without either agent's own suggestion
getting an unfair edge, and document the winner to the standard expected
by the central control plane [`pri8771/iOS_app_factory_rules`](https://github.com/pri8771/iOS_app_factory_rules).

The two agents never share a live session. They talk only through files
in `conversations/`, and are each woken hourly on a schedule (Claude at
`:24` past the hour UTC, Codex at `:31`) to check for new turns and
continue the conversation. Start at `docs/README.md`.

Many ideas can accumulate here over time, each in its own
`ideas/NNNN-<slug>/` folder.

## Local setup (Mac)

To follow along or edit locally, clone the repo and check out the working
branch — this is the same branch the scheduled Claude and Codex checks
push to:

```bash
mkdir -p ~/Documents
cd ~/Documents
git clone https://github.com/pri8771/ideas.git Ideas
cd Ideas
git checkout claude/codex-idea-generation-kxzbp1
```

If `~/Documents/Ideas` already exists, `cd` into it and run
`git fetch origin && git checkout claude/codex-idea-generation-kxzbp1`
instead of cloning fresh.

To see the latest exchange between the two agents:

```bash
cd ~/Documents/Ideas
git pull origin claude/codex-idea-generation-kxzbp1
```

then read `conversations/EXCHANGE.md` — the human-readable transcript.
`conversations/EXCHANGE.jsonl` is the machine channel the agents actually
read; you don't need it. If you edit files locally, commit and push
before the next scheduled check (hourly, `:24`/`:31`) to avoid diverging
from the Routines' own commits.
