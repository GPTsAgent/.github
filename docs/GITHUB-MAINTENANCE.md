# GitHub Maintenance

GPTsAgent uses two public repositories:

- `GPTsAgent/.github`: organization profile and community health defaults.
- `GPTsAgent/GPTsAgent`: full working directory and contribution target.

## Profile Repository Checks

Before changing this repository:

1. Confirm `profile/README.md` still describes GPTsAgent clearly.
2. Confirm links point to `GPTsAgent/GPTsAgent`.
3. Confirm community health files do not ask users to post secrets.
4. Confirm the profile validation workflow passes.

## Development Repository Checks

Before accepting project changes in `GPTsAgent/GPTsAgent`:

```bash
python3 scripts/validate_workspace.py
python3 scripts/build_release_zip.py
```

Expected result:

- workspace validation returns `Status: PASS`;
- `config/` has exactly 20 Markdown Knowledge files;
- `instructions/SYSTEM-INSTRUCTIONS.txt` matches `config/GPT-BUILDER-CONFIG.md`;
- no obvious secret-like material was introduced.

## Labels

Recommended labels for `GPTsAgent/GPTsAgent`:

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

Recommended protections:

- Require the `Validate GPTsAgent workspace` workflow.
- Require pull request review before merge.
- Dismiss stale approvals when new commits are pushed.
- Restrict force pushes.
- Restrict deletions.

## Maintainer Rules

- Keep `.env` local and ignored.
- Rotate any token that appears in terminal logs, issues, pull requests, commits, or screenshots.
- Keep user contributions flowing through `GPTsAgent/GPTsAgent` pull requests.
- Treat generated ZIPs as release artifacts, not as replacements for source files.
