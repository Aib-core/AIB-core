# Security Policy

## Scope
This repository is the AIB Core project. Keep credentials, API keys, access tokens, private keys, cookies, and other secrets out of the repository and out of commit history.

## Secret handling
- Store secrets only in the appropriate local environment or secret-management system.
- Never commit `.env` files containing real credentials.
- Never paste GitHub tokens, OpenAI API keys, SSH private keys, or passwords into source files, issues, or pull requests.
- If a secret is exposed, revoke/rotate it immediately and then remove it from the working tree and history as appropriate.

## Change safety
Security-sensitive changes should be made on a dedicated branch and reviewed before merging into `main`.

## Reporting
For a suspected security issue, do not publish the secret or exploit details in a public issue. Use GitHub's private security-reporting mechanisms when available.
