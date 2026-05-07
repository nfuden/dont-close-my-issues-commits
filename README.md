# dont-close-my-issues-commits

This repository contains a simple GitHub Actions workflow that listens for closed
issues, checks the issue's status in a roadmap project, prints that status to
the workflow log, and then writes the issue back to that same project status.

## Workflow

The workflow lives at `.github/workflows/issue-roadmap-status.yml` and runs
when an issue is closed.

By default it looks for:

- a project titled `Roadmap`
- a single-select field named `Status`

If you use a user or organization project that the default `GITHUB_TOKEN`
cannot update, add a `PROJECT_TOKEN` secret with project write access. The
workflow also still accepts `PROJECT_READ_TOKEN` as a fallback token name.
