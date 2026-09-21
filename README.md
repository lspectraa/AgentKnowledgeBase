# Agent Knowledge Base

IDE-neutral vault. Unpack at the **repo root**.

Canonical (every agent reads these):

- `AGENTS.md` — always-on guide
- `skills/<name>/SKILL.md` — skills (Agent Skills spec)
- `docs/` — living notes, on-demand only

Thin adapters (optional, point at the files above):

- `CLAUDE.md`
- `.github/copilot-instructions.md`
- `.cursor/rules/agent-knowledge-base.mdc` and `.cursor/hooks/session-start.cjs`
- `.agents/README.md`

Do not keep a second edited copy of a skill under `.cursor/skills/` or `docs/skills/`.

```
AGENTS.md
CLAUDE.md
skills/<name>/SKILL.md
docs/
  index.md
  playbook.md
  app/architecture.md
  processes/
  prompts/integrate-into-repo.md
.github/copilot-instructions.md
.cursor/rules/          # Cursor only
.cursor/hooks/          # Cursor only
.agents/                # pointer only
```

Install into a live app: `docs/prompts/integrate-into-repo.md`. First index: `docs/prompts/index-existing-app.md`. Slim an old vault: `docs/prompts/optimize-vault.md`.
