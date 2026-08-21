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
| [strspc-sync](https://github.com/SteerSpec/strspc-sync) | GitHub Action & CLI — template distribution by PR, drift monitoring, conflict detection (Go) |
| [strspc-CLI](https://github.com/SteerSpec/strspc-CLI) | User-facing CLI tooling (Go) |
| [strspc-pr-review](https://github.com/SteerSpec/strspc-pr-review) | GitHub Action — auto-approve PRs on Copilot's review verdict (JavaScript) |
| [.claude](https://github.com/SteerSpec/.claude) | Shared Claude Code agents, skills and settings — installable plugin marketplace |

**Website:** [steerspec.dev](https://steerspec.dev)

---

## Status

SteerSpec is under active development, and most of it ships today.

The rule format and the core engine are published. `strspc-sync` distributes templates by pull request, monitors targets for drift and flags conflicts across the fleet. `strspc-pr-review` approves pull requests on Copilot's verdict — a clean review, or a configurable number of review rounds — and is on the [GitHub Marketplace](https://github.com/marketplace/actions/pr-auto-approve-copilot). The CLI renders, lints and diffs rule files and evaluates changes against them. A hosted API is planned and not yet built.

The specification itself remains `v0.1.0-draft` — the tooling is further along than the spec it implements. Things will change. Feedback welcome.

Everything public here is Apache 2.0.
