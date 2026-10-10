# File contract

The Dispatch's Journal tab reads these files from the public raw URLs of this repository. A missing or malformed file is shown as "unavailable"; the tab never fills a gap with invented data. `schemaVersion` is 1 everywhere it appears.

| File | Written by | Purpose |
|---|---|---|
| `portfolio.json` | PM, via pull request | The rules: positions, weights, targets, review levels, thesis-breakers, triggers, drawdown ladder, calendar |
| `status.json` | PM, daily | Latest snapshot: verdict, NAV, return vs S&P 500, drawdown, per-position price/thesis status, trigger readings |
| `notes/index.json` | PM, daily | List of notes, newest last: `date, title, verdict, kind, file, summary` |
| `notes/YYYY-MM-DD.md` | PM, daily | The morning note (Markdown) |
| `journal/decisions.jsonl` | PM, append-only | One JSON object per line: id, date, type, verdict, title, reasoning, whatWouldChangeMyMind, outcome |
| `journal/challenges.jsonl` | PM, append-only | Codex challenges and replies: id, date, pr, kind (FACT/JUDGEMENT), challenge, evidence, reply, outcome (conceded / partly / overridden), reason |
| `journal/reflections.json` | PM | Week 4 and week 8 reviews: week, date, returnPct, benchmarkReturnPct, alphaPct, text |

## Rules
- Every price in `status.json` carries `price, asOf, source, status` (`ok`, `stale`, `unverified`, `reference`). A figure that could not be checked is published with `status: "unverified"`, never silently dropped or rounded into confidence.
- Journal files are append-only. A correction is a new line that refers to the old one; git history is the audit trail.
- Verdicts are `HOLD`, `WATCH` or `ACT`.
