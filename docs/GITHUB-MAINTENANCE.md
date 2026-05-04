# GitHub Maintenance

## Release Readiness

Before publishing a release:

1. Run `_codex-session/validate_v4_package.py`.
2. Confirm exactly 20 root Markdown files.
3. Confirm the Instructions block in `GPT-BUILDER-CONFIG.md` is current.
4. Run GPT Builder Preview tests from `EVALUATION-CHECKLIST.md`.
5. Confirm artifact ZIPs open and match root files.
6. Confirm no secret-like material was introduced.
7. Mark any host, CI, cloud, local-machine, or production claim as `NOT VERIFIED` unless actually tested.

## Label Set

Recommended labels:

- `package`
- `documentation`
- `safety`
- `validation`
- `github-actions`
- `dependencies`
- `triage`
- `good first issue`
- `blocked`
- `not verified`

## Branch Policy

Use `main` as the release branch.

Recommended protections after the remote repository exists:

- Require the `Validate GPTsAgent package` workflow.
- Require pull request review before merge.
- Dismiss stale approvals when new commits are pushed.
- Restrict force pushes.
- Restrict deletions.

## Maintainer Rules

- Keep `.env` local and ignored.
- Rotate any token that appears in terminal logs, issues, pull requests, commits, or screenshots.
- Do not add root Markdown files casually; the package is designed around the GPT Builder Knowledge limit.
- Treat generated ZIPs as release artifacts, not as replacements for source files.
