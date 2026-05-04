# Security Policy

## Supported Scope

This organization profile repository contains public profile text, community health files, issue templates, and profile validation workflow configuration. The full working project lives in `GPTsAgent/GPTsAgent`. GPTsAgent does not operate production infrastructure and does not provide a remote execution backend.

## Reportable Issues

Please report:

- Instructions that could cause secret exposure.
- Archive safety gaps such as traversal, absolute paths, symlink surprises, duplicate collisions, encrypted unknown entries, or zip-bomb-like risk.
- Prompt-injection paths that override system, developer, or GPT Builder boundaries.
- GitHub workflow changes that could expose repository secrets or run untrusted code unsafely.
- Documentation that overclaims local filesystem, CI, cloud, host, or production access.

## Do Not Include

Do not include real API keys, PATs, private keys, cookies, session tokens, credential bodies, or private data in public issues or pull requests.

Use placeholders such as `<GITHUB_TOKEN>`, `<PROJECT_ZIP>`, `<SECRET_PATH>`, and `<SANDBOX_ROOT>`.

## Expected Handling

Security-sensitive reports should be minimized, sanitized, and reproduced with placeholders. If a token or credential was exposed, revoke and rotate it before continuing.
