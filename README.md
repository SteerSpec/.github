<div align="center">

<img src="https://steerspec.dev/assets/logo.svg" alt="SteerSpec logo" width="72" height="72">

# SteerSpec community health files

**Org-wide defaults and the public profile for the [SteerSpec](https://github.com/SteerSpec) organization.**

[![CI](https://github.com/SteerSpec/.github/actions/workflows/ci.yml/badge.svg)](https://github.com/SteerSpec/.github/actions/workflows/ci.yml)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)

[Contents](#contents) · [How defaults apply](#how-defaults-apply) · [Branches and releases](#branches-and-releases) · [Contributing](#contributing)

</div>

This repository holds the community health files GitHub applies to every SteerSpec repository that
doesn't define its own, plus the README rendered on the organization page. For the project itself,
visit [steerspec.dev](https://steerspec.dev).

## Contents

| File | Purpose |
| ---- | ------- |
| [`profile/README.md`](profile/README.md) | The public organization profile |
| [`CONTRIBUTING.md`](CONTRIBUTING.md) | How to propose changes |
| [`CODE_OF_CONDUCT.md`](CODE_OF_CONDUCT.md) | Community standards |
| [`SECURITY.md`](SECURITY.md) | How to report a vulnerability |
| [`LICENSE`](LICENSE) | Apache 2.0 |
| [`.github/workflows/`](.github/workflows) | CI: markdown lint, link integrity, SteerSpec checks, PR auto-approve, release sync-back |

## How defaults apply

A repository inherits these files unless it ships its own copy. A repo's own file always wins, so
override per repo whenever the org default doesn't fit.

## Branches and releases

`develop` is the default branch. Pull requests go to `develop` and are squashed, so the PR title
becomes the commit release-please reads. A `chore: promote develop to main` pull request, merged with
a merge commit, carries the bundle to `main`. release-please then opens a release PR; merging it tags
`vX.Y.Z`, moves `v1`, and opens a pull request that syncs the release back into `develop`.

Callers that pin `@main` see only promoted workflows, and callers that pin `@v1` only released ones.
Release tags cannot be moved or deleted, and only the release workflow can move `v1`.

## Contributing

Changes here affect every repository in the org, so keep them small and open a pull request. See
[`CONTRIBUTING.md`](CONTRIBUTING.md).
