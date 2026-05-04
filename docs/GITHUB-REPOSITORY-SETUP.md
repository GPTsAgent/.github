# GitHub Repository Setup

GPTsAgent now uses two public repositories:

- `GPTsAgent/.github`: organization profile and community health defaults.
- `GPTsAgent/GPTsAgent`: full working directory, development, issues, pull requests, configuration, and instructions.

## Organization Profile

GitHub displays the organization profile from:

```text
GPTsAgent/.github/profile/README.md
```

This repository should stay small and profile-focused.

## Development Repository

The development repository is:

```text
https://github.com/GPTsAgent/GPTsAgent
```

Users can download a full working directory from:

```text
https://github.com/GPTsAgent/GPTsAgent/archive/refs/heads/main.zip
```

Or clone:

```bash
git clone https://github.com/GPTsAgent/GPTsAgent.git
cd GPTsAgent
python3 scripts/validate_workspace.py
```

## What Goes Where

Use `GPTsAgent/GPTsAgent` for:

- `config/`: the 20 GPT Builder Knowledge files.
- `instructions/`: the canonical system instructions.
- `scripts/`: validators and release helpers.
- `docs/`: contributor and maintainer documentation.
- issues and pull requests.

Use `GPTsAgent/.github` for:

- `profile/README.md`;
- organization-level community health files;
- profile validation workflow.

## GPT Builder Knowledge

Upload exactly the 20 Markdown files from `GPTsAgent/GPTsAgent/config/` as GPT Builder Knowledge.

Do not upload:

- `.github/`
- `docs/`
- `profile/`
- `scripts/`
- `.env`
- generated caches
- source ZIPs
- repository metadata
