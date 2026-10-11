# Dispatch - Umushroom

**An 8-week paper-money experiment (12 Oct to 7 Dec 2026): can a £100,000 AI-transition portfolio beat the S&P 500 without losing more than 18% in a severe shock?**

> Paper portfolio for learning. Not investment advice. No real money is invested, and nothing here is a recommendation to buy or sell anything.

## In plain terms (for anyone reading)
- **The bet:** own the companies that supply AI (chips, power equipment, nuclear and grid power) rather than the ones spending the most on it, plus South Korea and Brazil, with cash and gold as a cushion.
- **The test:** beat the S&P 500 over eight weeks, with a hard rule that the modelled worst case stays inside an 18% loss.
- **How it is run:** an AI portfolio manager (Claude) writes a note every weekday morning and says HOLD, WATCH or ACT. It is meant to do nothing most days and act only when a pre-written rule is hit. A second AI (OpenAI Codex) reviews the work on Fridays and whenever a trade is proposed, and the portfolio manager must either concede or argue back, in public.
- **What I will learn:** whether the reasoning holds up, written down before the result is known. Week 4 and week 8 reflections are scored against the S&P 500.

## Where things are
| | |
|---|---|
| `portfolio.json` | The positions and the rules |
| `status.json` | Latest value, return vs the S&P 500, drawdown |
| `notes/` | Morning notes |
| `journal/` | Decision log, Codex challenges and replies, reflections |
| `REVIEWER.md` | The brief the reviewer works to |
| `SCHEMA.md` | File formats (the Dispatch's Journal tab reads these) |

Read it in context on **The Dispatch**'s Journal tab (UMushroom view).

## Working rules
- Daily notes and status are committed straight to `main` by the portfolio manager.
- Any change to `portfolio.json` (a trade, a new rule) goes through a pull request tagged `@codex review`.
- Codex can overturn a verdict only by showing a factual error. Otherwise the portfolio manager holds its view; overrides are recorded with the reason.
- At most two portfolio changes a week.
- Figures that could not be verified are published marked **unverified**.

## Limits of this experiment
Eight weeks is a short window; a good or bad result is mostly luck. The point is the quality of the reasoning and the record, not the return. Prices come from free or low-cost sources and some are delayed.
