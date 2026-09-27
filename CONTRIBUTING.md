# Contributing to Ophix

Thanks for your interest in contributing. A few things worth knowing before you invest time.

## No warranty, no SLA

Ophix is free, MIT-licensed software, provided with no warranty. Bug reports and pull requests are genuinely welcome and appreciated, but nothing here is owed to anyone, paying or not. Issues and PRs are reviewed as time allows — there is no guaranteed response time. Paying support customers always take priority over unpaid community contributions; that's what funds the maintainer's time to work on this project at all.

## Hard architectural rules

Ophix has a small number of non-negotiable design rules. A contribution that conflicts with one of these is very unlikely to be merged, regardless of how well-executed it is — worth checking before investing effort:

1. **Independence** — every server-client pair must run in complete isolation. No domain may depend on another domain being installed or running.
2. **Air-gap compatibility** — no runtime external dependencies. No CDN assets. Nothing phones home.
3. **Pip composability** — all server components are pip-installable packages. Never introduce a dependency or structural change that breaks this.
4. **Credentials are never persisted on clients** — secrets are fetched on demand and used in memory only.

## Developer Certificate of Origin

By submitting a pull request, you certify that you wrote the contributed code (or otherwise have the right to submit it under this project's license), per the [Developer Certificate of Origin](https://developercertificate.org/). Please sign off your commits:

```
git commit -s -m "Your commit message"
```

This adds a `Signed-off-by: Your Name <your.email@example.com>` line to your commit — no account or paperwork needed, just an assertion that the contribution is genuinely yours to give.

## Reporting bugs vs. asking for help

- **Found a bug?** Open an issue using the Bug Report template.
- **Need help using Ophix?** Please use [paid support](https://ophix.io/services/) rather than opening an issue — issues here are for defects and feature requests, not usage questions.

## Pull requests

- Fork, branch, and open a PR against `main`.
- Keep changes focused — a PR that does one thing is much easier to review than one that does several.
- No specific style guide is enforced today beyond matching the surrounding code.
