# Security Policy

This policy covers every repository in the [SteerSpec](https://github.com/SteerSpec) organization
unless that repository ships a `SECURITY.md` of its own.

## Supported versions

Only the latest release of a given major line receives fixes. Where a repository publishes a moving
major tag (`@v1`), that tag always points at the newest release in the line, so pinning it is the
supported way to receive security patches automatically. Older minor and patch releases are not
backported.

## Reporting a vulnerability

**Do not open a public issue, discussion, or pull request for a security problem.**

Report it privately through GitHub: on the affected repository, go to **Security → Report a
vulnerability**, or use the `/security/advisories/new` path directly. That form is private to you
and the maintainers, and it is the only channel we monitor for security reports.

Include what you would want if you were fixing it: the affected repository and version or tag, the
impact, and the smallest set of steps that reproduces the problem. A caller workflow, a redacted
log excerpt, or a proof of concept all help.

## What happens next

- We aim to acknowledge a report within five working days.
- If it is confirmed, we work the fix on a private fork and keep you updated through the advisory
  thread.
- Disclosure is coordinated: we publish a GitHub Security Advisory alongside the release that
  contains the fix, and credit the reporter unless they ask us not to.
- If we conclude a report is not a vulnerability, we explain why in the same thread rather than
  closing it silently.

## Scope

These projects are GitHub Actions and workflows, so the interesting boundary is what a repository
trusts from a pull request and what it hands to a token.

**In scope** — anything that lets untrusted pull request content influence a privileged run: code or
expression injection through PR-controlled values, a workflow reading secrets in a context an
attacker can reach, a token or secret disclosed in logs or outputs, a decision path that can be
tricked into approving a pull request it should have skipped, or a supply-chain issue in what these
repositories publish.

**Out of scope** — configuration mistakes in a repository that *calls* one of these actions. Giving
a bot token more scope than it needs, or wiring an action into a trigger it was not documented for,
is a misconfiguration on the caller's side rather than a vulnerability here. Report it anyway if you
believe our documentation invited the mistake — that is a real problem and we would rather fix the
docs than argue about the label.

Treat any bot credential these projects ask for as a write-scoped credential: keep it in secrets,
scope it as narrowly as the documentation allows, and rotate it periodically.
