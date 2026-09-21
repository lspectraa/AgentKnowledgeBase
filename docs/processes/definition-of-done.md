# Definition of Done

Use this list on a major change or when the human asks. Do not paste it into routine replies. No default git.

- Change is scoped to the requested task
- No secrets or environment-specific credentials in source
- Tests still pass where this area is already tested
- Docs updated only if contracts or behavior changed
- High-impact unspecified changes reported as `## WARNING` plus a `---` rule ([[report-major-changes]])
- Processes this session started have been stopped ([[stop-what-you-start]])

The human opens the PR. Run [[pre-review-qa]] only after a major change or when asked.
