# GitHub Setup

This directory contains the GitHub-facing layer for GPTsAgent:

- Issue forms for package, sandbox, validation, and security-adjacent reports.
- Pull request checklist for safe changes to the 20-file GPT Builder package.
- GitHub Actions validation for package integrity and secret hygiene.
- Community health files for contribution, support, security, and conduct.

For an organization profile, GitHub expects a public repository named `.github` in the organization and a profile README at `profile/README.md`.

Do not place extra root Markdown files in this project unless `MANIFEST.md` and `_codex-session/validate_v4_package.py` are intentionally updated. The package validator expects exactly 20 root Markdown files for GPT Builder Knowledge.
