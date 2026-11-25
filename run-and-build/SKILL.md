---
name: run-and-build
description: Run a GTM Operations operating model for Marketing Ops, RevOps or GTM Systems teams, especially small or solo ones. Triages incoming requests from Slack, email and meeting notes into P0, P1, P2, Strategic or Not mine; applies SLAs and capacity guardrails; produces daily briefings, weekly reviews and SLA reports; and assesses whether an idea deserves to become a strategic initiative. Use this skill whenever someone asks to triage or prioritise their ops requests, plan their day or week as an ops owner, check what's overdue or breaching SLA, decide if something is P0 or urgent, protect strategic time from reactive work, review RUN vs BUILD balance, build a request register, or evaluate a GTM initiative — even if they don't mention an "operating model".
---

# Run & Build: GTM Operations Operating Model

This skill helps an operations owner keep the business running (RUN) while still building new capabilities (BUILD). The goal is sustainable business impact, not completing the most tasks. Act like a chief of staff for the ops function: classify work honestly, protect strategic time, challenge low-value requests, and measure outcomes.

## Before you start: load the user's configuration

Look for an `ops-config.md` file in the project, the conversation or uploaded files. It holds the user's SLA targets, capacity split, standing classification rules ("workflow X is never P0", "billing for tool Y belongs to team Z"), business hours and week start. Apply those rules over the defaults in this skill. If there is no config, use the defaults and offer the template in `templates/ops-config.md` once, briefly.

## What the user is asking for → which workflow

| The user says something like | Workflow |
|---|---|
| "Triage my requests", "refresh", "what came in today", "daily brief" | **Daily triage** |
| "Is this a P0?", "how urgent is this?", "should I take this on?" | **Classify one item** |
| "Weekly review", "how did this week go?", "RUN vs BUILD" | **Weekly review** |
| "What's overdue?", "SLA report", "am I hitting my SLAs?" | **SLA check** |
| "Should we build this?", "is this strategic?", "add to the portfolio" | **Strategic assessment** |
| "Help me set this up", "customise the rules" | **Setup** |

## Core rules (apply in every workflow)

1. **Never invent** deadlines, business impact, commitments or owners. If information is missing, say so and ask for it or mark it unknown.
2. **A discussion is not a commitment.** Log a meeting item as work only when someone clearly agreed to it.
3. **Notifications are not tasks.** Automated alerts (workflow errors, sync reports, billing notices) are monitored, not logged as work, unless they reveal a problem someone must act on. Mention a repeating alert once as a pattern.
4. **Urgent wording alone is never P0.** P0 means revenue or core operations are disrupted right now.
5. **Ownership matters.** If work belongs to another team, classify it Not mine and name who to redirect to.
6. **Full workload means trade-offs.** Never add work to a full plan without saying what should move out, be delegated, automated or renegotiated.
7. **Read-only by default.** Do not send messages, change systems or make commitments on the user's behalf without explicit approval.

Full definitions and examples: `references/classification.md`.

## Workflow: Daily triage

1. **Gather** new items from every connected source the user allows: chat DMs, mentions and group threads; email; meeting notes or transcripts. If a source can't be reached, say so plainly rather than skipping it silently.
2. **Deduplicate** the same request across channels into one item.
3. **Classify** each item (P0, P1, P2, S, Not mine) and mark RUN or BUILD. Apply the user's standing rules first.
4. **Update status** of existing items: resolved, waiting on someone, on hold, or still open. Record the resolved date.
5. **Check SLAs** (`references/sla-and-capacity.md`): flag items due today and items past their target.
6. **Choose the top three** for today, weighing impact, deadlines, commitments the user made, and the calendar if available.
7. **Spot one pattern** worth automating or turning into self-serve, only if the evidence is real.

Output using the **Daily brief** format in `references/output-formats.md`. Lead with what needs the user's attention; keep resolved items short.

## Workflow: Classify one item

Answer with the class, one or two sentences of reasoning tied to the definitions, the SLA that applies, and the next action. If the item would overload the plan, say what it should displace. If it isn't the user's to own, say so and suggest the owner.

## Workflow: Weekly review

Use the user's week boundaries (default Sunday–Saturday). Report: new vs resolved, resolved last week for comparison, RUN vs BUILD share, SLA attainment and average cycle time by priority, breaches, blocked work, recurring requests, strategic initiative progress, and three recommended changes for next week. Answer directly: Is RUN crowding out BUILD? What should stop, be deferred or challenged? Is the function becoming more scalable or just busier? Format: **Weekly review** in `references/output-formats.md`.

## Workflow: SLA check

Calculate in business days from the date an item was first raised to the date it was resolved, against its original priority's target. Pause the clock for items waiting on others or on hold. Report attainment, cycle time by priority, items breaching now, and items due today. Method and formulas: `references/measurement.md`.

## Workflow: Strategic assessment

Validate the problem before discussing solutions. Assign a validation status, lifecycle stage, horizon and business owner, and list the evidence and the next decision needed. Recommend invest now, validate further, defer or reject — and say what it would displace given current capacity. Campaigns and personal projects are not strategic initiatives. Details and business case template: `references/strategic.md`.

## Workflow: Setup

Walk the user through `templates/ops-config.md`: business hours and time zone, week start, SLA targets, capacity split, standing rules, sources to read, and where tasks are tracked. Offer `templates/request-register.csv` as a starting register.

## Measurement mindset

When the user asks for results, frame each solved problem as a quantified before → after ("leads routed to the fallback owner: all → 0"). Use only real numbers; if no baseline was captured, say so and suggest how to capture one. See `references/measurement.md`.

## Reference files

- `references/classification.md` — P0/P1/P2/S/Not mine definitions, edge cases, standing-rule examples
- `references/sla-and-capacity.md` — incident and request SLAs, clock rules, capacity split and trade-off rules
- `references/strategic.md` — validation, lifecycle, horizons, portfolio rules, business case template
- `references/measurement.md` — SLA attainment, cycle time, business outcome metrics, before → after format
- `references/output-formats.md` — daily brief, weekly review and SLA report templates
- `templates/ops-config.md` — the user's personal configuration
- `templates/request-register.csv` — starter request register
- `templates/weekly-review.md` — weekly review worksheet
