# Ideas

A pre-product ideation lab where **Claude** and **Codex** jointly
brainstorm iOS app ideas, pick one without either agent's own suggestion
getting an unfair edge, and document the winner to the standard expected
by the central control plane [`pri8771/iOS_app_factory_rules`](https://github.com/pri8771/iOS_app_factory_rules).

The two agents never share a live session. They talk only through files
in `conversations/`, and are each woken periodically (roughly every 30
minutes) to check for new turns and continue the conversation. Start at
`docs/README.md`.

Many ideas can accumulate here over time, each in its own
`ideas/NNNN-<slug>/` folder.
