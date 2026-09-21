# Lessons learned

Newest entry at the top.

### 2026-09-06 — Knowledge base efficiency

- Context: agent latency and token bloat from vault pre-reads
- Mistake: mandatory playbook/DoD/architecture reads plus duplicate always-on rules added 15k–25k tokens and 15–30s per routine task
- What to do next time: just-in-time docs, one architecture file, lean always-apply rule, env-only session hook, skills in one tree (`skills/`)
- Files involved: AGENTS.md, .cursor/rules/agent-knowledge-base.mdc, .cursor/hooks/session-start.cjs, docs/app/architecture.md, skills/

### 2026-09-06 — Reviews only on major changes; no git by default

- Context: finishing routine tasks
- Mistake: QA tables and `git status`/`diff` on every small edit
- What to do next time: review only after major work or when asked; git only to compare an earlier version
- Files involved: AGENTS.md, docs/playbook.md, docs/processes/

### 2026-09-04 — Session hooks: `.cjs`, env only

- Context: Cursor sessionStart in a `"type": "module"` repo
- Mistake: `.js` hooks die on `require`; `additional_context` can be dropped
- What to do next time: `node .cursor/hooks/*.cjs`; durable rules in the always-apply mdc; hook payload env only
- Files involved: .cursor/hooks.json, .cursor/hooks/session-start.cjs
