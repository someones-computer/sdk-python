# Working agreement

How to work in this repo. The shared style and Version Control System (VCS) rules come from the
`.claude/agent-standards` submodule.

@.claude/agent-standards/CLAUDE.md
@.claude/agent-standards/docs/Topics/VCS.md
@.claude/agent-standards/docs/Topics/Tooling.md

**First action in any session: run `.claude/check-wiring.sh`.** Silence means the wiring is
good. Output means the shared working agreement isn't loaded. Fix it before you start work.

This repo runs in the default ask-permission mode. See
[Working agreement mode](.claude/agent-standards/docs/Topics/VCS.md#working-agreement-mode).

## Quality gate

Run each check before you commit.

| Check | Command |
|---|---|
| Shared wiring | `.claude/check-wiring.sh --ci` |
| Git hooks of `hk.pkl` | `hk check --all` |
