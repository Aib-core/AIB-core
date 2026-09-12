# AIB Core

**Android Intelligence Bridge — Core Repository**

This repository is the dedicated home for the AIB Core project.

## Current state

The repository currently contains the project profile plus a security baseline. The implementation can be added incrementally without mixing unrelated projects into this repository.

## Repository rules

1. `main` is the stable branch.
2. Experimental and security-sensitive work should use dedicated branches.
3. Do not commit credentials, API keys, access tokens, private keys, or `.env` files containing real secrets.
4. Keep generated build artifacts out of source control unless they are intentionally released artifacts.
5. Changes should be reviewed before being merged into `main`.

## Security

See [SECURITY.md](SECURITY.md) for the repository security policy.

## Project direction

AIB is intended to act as an Android-side intelligence bridge/orchestrator between an AI model and Android execution capabilities. Concrete modules should be introduced deliberately, with clear boundaries between interface, runtime, device capabilities, and safety controls.
