# SteerSpec

**AI configuration as code — versioned, templated, and synchronized across your entire org.**

Your `CLAUDE.md` drifts. `.claude/agents/` mutates. New repos miss critical setup. SteerSpec fixes this by treating AI configuration files like infrastructure: define once in a central manifest, propagate everywhere via pull request, detect drift on a schedule.

> *Because vibe coding without a spec is just vibing.*

---

## What's here

| Repo | Description |
|------|-------------|
| [strspc-rules](https://github.com/SteerSpec/strspc-rules) | Canonical rule format — self-referential rule definitions and schemas (Python) |
| [strspc-manager](https://github.com/SteerSpec/strspc-manager) | Core enforcement engine — rule-lint, rule-diff, rule-eval, rule-resolve (Go) |
| [strspc-sync](https://github.com/SteerSpec/strspc-sync) | GitHub Action & CLI for template distribution via PR (Go) |
| [strspc-CLI](https://github.com/SteerSpec/strspc-CLI) | User-facing CLI tooling (Go) |

**Website:** [steerspec.dev](https://steerspec.dev)

---

## Status

SteerSpec is under active development. The rule format is defined, the core engine and sync action are functional, and the CLI is taking shape. Things will change. Feedback welcome.
