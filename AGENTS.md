# Agent instructions

Primary guide for every IDE and agent. Skills load from `skills/<name>/SKILL.md`. Do not pre-read this vault.

## Hard limits

1. No PR open, merge, or approve.
2. No fake tests. No secrets in files or chat.
3. Stop every server, watcher, or app this session started before finishing.
4. After a large change, run pre-review QA before reporting done (`docs/processes/pre-review-qa.md`). Do not wait to be asked. Also run it when asked. A large change adds a subsystem, public API, or schema, or implements a feature past a one- or two-file fix. Do not print the QA table on a small edit.
5. No default git checks. Use `git status` / `diff` / `log` only when comparing to an earlier version.
6. No pre-flight reading loops. For targeted work, go straight to code.
7. Docs are just-in-time. Read one specific note only when a subsystem is unfamiliar.
8. Default to parallel work. Independent reads, searches, edits, shell commands, and sub-agents run in the same turn. Launch sub-agents for independent workstreams instead of doing those streams serially inline. See `docs/rules/parallel-operations.md`.
9. An ADR is incomplete until every affected site has a short comment pointing at `docs/adrs/NNN-slug.md`.
10. If you delete application logic, report it before you finish as `## WARNING` plus a `---` rule. Do not silently remove branches, handlers, or helpers. See `docs/rules/report-deleted-logic.md`.
11. If you add a hardcoded user-facing string, magic string or number, or an inline mapping, report it before you finish as `## WARNING` plus a `---` rule. See `docs/rules/report-hardcoded-strings.md`.

## Workflow

1. Align on intent.
2. Consult docs on-demand only. Skip for familiar or targeted tasks.
3. Implement in small steps.
4. Update docs only if contracts or behavior changed.
5. Verify runtime or tests when the change needs it. Independent verify commands may run together.
6. Clean up processes you started.
7. If the change is large, run pre-review QA, then report done. Skip the table on a small edit.
8. Finish concisely.

## Concurrency

Default is parallel. Follow `docs/rules/parallel-operations.md`. Stay serial when a later step needs an earlier result, when state is shared and mutable, or when two edits would hit the same file.

## Commands

Fill this table on first index (`docs/app/run-test-lint.md` is the durable copy):

| Action | Command |
| --- | --- |
| Install | |
| Test | |
| Build / typecheck | |
| Dev / run | |

## Skills

| Skill | Path |
|---|---|
| agent-knowledge-base | `skills/agent-knowledge-base/SKILL.md` |
| concurrent-subagents | `skills/concurrent-subagents/SKILL.md` |
| docs-and-mermaid | `skills/docs-and-mermaid/SKILL.md` |
| compounding-knowledge | `skills/compounding-knowledge/SKILL.md` |
| living-adr | `skills/living-adr/SKILL.md` |
| agent-playwright | `skills/agent-playwright/SKILL.md` |
| api-probe | `skills/api-probe/SKILL.md` |

## Vault

`docs/`. Map: `docs/index.md`. Systems: `docs/app/architecture.md` (one file). Install into another repo: `docs/prompts/integrate-into-repo.md`.
