# dont-close-my-issues-commits

This repository contains a simple GitHub Actions workflow that listens for closed
issues, checks the issue's status in a roadmap project, and prints that status
to the workflow log.

## Workflow

The workflow lives at `.github/workflows/issue-roadmap-status.yml` and runs
when an issue is closed.

By default it looks for:

- a project titled `Roadmap`
- a single-select field named `Status`

If you use a user or organization project that the default `GITHUB_TOKEN`
cannot read, add a `PROJECT_READ_TOKEN` secret with `read:project` access.
