# 18F/analytics-reporter context
> refreshed 2026-09-03 | upstream default: develop @ 2b9bb4ae10edfec8b90679b4fc47d43905d950a2

## Identity & policies
- upstream: 18F/analytics-reporter, default branch `develop`, primary language JavaScript (Node), English-first (yes — all docs/strings in English).
- CLA/DCO: none (CONTRIBUTING: CC0 public domain dedication, no CLA bot, no signup).
- AI-assisted PR policy: unstated (no mention in CONTRIBUTING or .github).
- signed commits required: no (no branch protection on `develop`).
- PR template: none (`.github/` has only `workflows/`; no PULL_REQUEST_TEMPLATE).
- external tracker: github.

## Conventions (verified from merged PRs)
- branch naming: no dominant pattern (develop/staging, feature/*, fix/*, plain kebab). Fall back to `fix/<kebab>`.
- commit style: plain imperative ("Upgrade the...", "Configure New Relic..."), no Conventional Commits.
- test command: `npm test` (mocha, needs Postgres); lint: `npm run lint` (eslint).
- CI: `.github/workflows/ci.yml` (lint + test + coverage). Fork Actions must be enabled.

## Maintainer picture
- 18F/GSA maintainers (Michael Levin et al.). PRs merged regularly; dependabot-heavy recent history.

## Issue-area health
- No contested/redesign signals relevant to trivial cleanup.

## Gap ledger (dedupe — READ FIRST, never re-pick)
- `2026-09-03` self-found trivial cleanup (stale `deploy/cron.js` refs in package.json + Procfile; typo "fro" in src/publish/disk.js; wrong JSDoc in src/actions/write_analytics_data_to_database.js; typo "it's" in src/process_results/result_formatter.js) — outcome: pr-opened — lesson: cron.js deleted in 069f644 (Bree), refs left stale; dedupe searches for these strings return no upstream PRs.

## Mined gaps (discovered, not yet attempted)
- `2026-09-03` src/process_results/result_totals_calculator.js line 131 `result.date[0].date` vs `result.data` — code bug, NOT trivial (behavior change) — status: dropped(out-of-scope-for-trivial)
