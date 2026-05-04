# GitHub Repository Setup

This project is ready to be published either as the organization profile repository `GPTsAgent/.github` or as a normal project repository under the `GPTsAgent` account.

## Organization Profile Mode

Use this when `GPTsAgent` is a GitHub organization.

GitHub displays an organization profile README from a public repository named `.github`, using this path:

```text
profile/README.md
```

For this project, that file already exists at `profile/README.md`.

Recommended remote:

```bash
git remote add origin https://github.com/GPTsAgent/.github.git
```

Then push:

```bash
git push -u origin main
```

## Personal Account Profile Mode

Use this only if `GPTsAgent` is a personal GitHub user account, not an organization.

GitHub user profiles use a repository with the same name as the user, usually:

```text
GPTsAgent/GPTsAgent
```

In that mode, the visible profile README should be the root `README.md`. This project intentionally keeps the root `README.md` as the Sandbox File Operator package README, so organization mode is the cleaner fit.

## Normal Project Repository Mode

Use this when the profile lives elsewhere and this repository should hold the package itself.

Recommended remote examples:

```bash
git remote add origin https://github.com/GPTsAgent/sandbox-file-operator.git
git remote add origin https://github.com/GPTsAgent/GPTsAgent.git
```

## First Local Commit

From `/home/acer/projects/GPTsAgent`:

```bash
git init -b main
git config user.name "Your Name"
git config user.email "your-email@example.com"
git add .
git status --short
git commit -m "Add Sandbox File Operator package and GitHub profile setup"
```

Use your real GitHub commit identity for `user.name` and `user.email`. Before pushing, confirm that `.env` is not listed by `git status --short`.

## GitHub CLI Path

If `gh` is installed and authenticated:

```bash
gh repo create GPTsAgent/.github --public --source=. --remote=origin --push
```

If the GitHub API is timing out from WSL, create the repository in the browser first, then push after connectivity is restored.

## Validation Before Push

Run:

```bash
python3 _codex-session/validate_v4_package.py
python3 -m py_compile scripts/github_access.py _codex-session/validate_v4_package.py
```

Expected package result: `Status: PASS`.

## What Not To Upload To GPT Builder

Do not upload these as GPT Knowledge:

- `.github/`
- `docs/`
- `profile/`
- `_codex-session/`
- `.env`
- generated caches
- source ZIPs
- repository metadata

GPT Builder Knowledge should receive exactly the 20 root Markdown files listed in `MANIFEST.md`.
