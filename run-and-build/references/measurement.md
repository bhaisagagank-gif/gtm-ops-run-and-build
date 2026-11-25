# Measurement

Report business outcomes, not activity.

## Function health

| Metric | Calculation |
|---|---|
| SLA attainment | Resolved items closed within their original priority's target ÷ all resolved items that have an SLA |
| Cycle time | Average business days from Raised to Resolved, by original priority |
| Breaching now | Open P0/P1/P2 items past target, excluding items waiting on others, on hold or blocked |
| Due today | Open items whose target falls today |
| RUN vs BUILD share | Share of open items in each, tracked weekly |
| New vs resolved | Items raised vs resolved within the week |
| Intake via official route | Share of requests not arriving by direct message |
| Self-serve conversions | Recurring requests turned into reports, forms or automation, per month |

### Business-day calculation
Count each weekday after the raised date up to and including the resolved date (or today for open items). Weekends don't count. Use the user's time zone for "today".

Keep each item's **original priority** when it's resolved so a P1 is still judged against the P1 target.

## Business outcomes (examples)

- Lead routing: leads falling back to a non-seller owner (target 0).
- Data quality: share of records with required fields complete.
- Follow-up health: prospects past their follow-up window.
- Conversion: demo no-show rate; signal-to-meeting rate.
- Cost: platform cost per 1,000 contacts.

## Before → after format

Capture a baseline before every change. When a problem is solved, record one line:

> [Metric]: [before] → [after] ([how])

Examples:
- "Leads routed to the fallback owner: all → 0 (owner assigned for two regions)."
- "Records missing region: [baseline] → [after] (automated mapping plus backfill)."

Never estimate a before value that wasn't measured. If no baseline exists, say so and recommend capturing one now.
