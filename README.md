# workflows

Reusable GitHub Actions workflows shared across dcwalker's repos.

## Workflows

- **claude-review.yml** — automated Claude PR review, gated on the `review / gate` status check. Callers add a thin caller stub invoking this with `uses: dcwalker/workflows/.github/workflows/claude-review.yml@main` (see the header comment in the file for a full example).
- **sensitive-info-check.yml** — scans PRs, pushes, and (weekly) full history for denylisted sensitive patterns. Callers add a thin caller stub invoking this with `uses: dcwalker/workflows/.github/workflows/sensitive-info-check.yml@main` (see `self-sensitive-info-check.yml` in this repo for a full example).

This repo is public so that public callers (e.g. [ai-skills](https://github.com/dcwalker/ai-skills)) can use these workflows — GitHub does not allow a public repository to call a reusable workflow hosted in a private one.

## This repo's own checks

`self-review.yml` and `self-sensitive-info-check.yml` are this repo's own caller stubs, applying both checks to itself.
