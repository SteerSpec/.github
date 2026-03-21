# SteerSpec

**AI configuration as code — versioned, templated, and synchronized across your entire org.**

Your `CLAUDE.md` drifts. `.claude/agents/` mutates. New repos miss critical setup. SteerSpec fixes this by treating AI configuration files like infrastructure: define once in a central manifest, propagate everywhere via pull request, detect drift on a schedule.

> *Because vibe coding without a spec is just vibing.*

---

## What's here

| Repo | Description |
|------|-------------|
| [strspc-spec](https://github.com/steerspec/strspc-spec) | The formal SteerSpec specification |
| [strspc-rules](https://github.com/steerspec/strspc-rules) | The rule format that powers the spec |
| [strspc-sync](https://github.com/steerspec/strspc-sync) | GitHub Action for template distribution |
| [strspc-CLI](https://github.com/steerspec/strspc-CLI) | CLI tooling |

**Website:** [steerspec.dev](https://steerspec.dev)

---

## Status

SteerSpec is in early development — the spec is drafted, tooling is being built. Things will change. Feedback welcome.
