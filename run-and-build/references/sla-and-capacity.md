# Service levels and capacity

## Incident SLA (defaults — override in ops-config.md)

| Priority | Definition | Target response | Target resolution |
|---|---|---|---|
| P0 | Outage or critical failure | < 30 minutes | Workaround in 2–4 hours; root-cause fix within 1 business day (or vendor timeline) |
| P1 | Major failure or blocked launch | < 2 business hours | 1–3 business days; dated plan within 1 business day |
| P2 | Minor degradation with a workaround | < 1 business day | 5 business days, in a batch slot |

For SLA attainment, use these resolution targets: **P0 = 1, P1 = 3, P2 = 5 business days.**

## Request SLA

| Type | Examples | Response | Delivery |
|---|---|---|---|
| Priority request | Campaign with a launch date, leadership reporting | 1 business day | Agreed date, at least 3 business days' notice |
| Standard request | Field changes, list pulls, minor edits | 1 business day | 5–10 business days, batched |
| Strategic initiative | New capabilities and playbooks | Weekly review | Per milestone in the approved business case |

## Clock rules

1. The clock starts when the item is first raised through any tracked source.
2. Missing information pauses the clock until it's provided.
3. Waiting on another team or vendor pauses the clock — status must say "Waiting on…", "On hold" or "Blocked".
4. The ops owner sets priority, not the requester.
5. Escalate a P0 not contained within 4 hours or a P1 past 3 business days, with impact and blocker.
6. Track breaches monthly; repeated P1 breaches are evidence of a capacity constraint, not a reason to work longer hours.

Business days are Monday–Friday unless the config says otherwise.

## Capacity

Plan against real available hours (minus meetings, admin and interruptions), never 100%.

| Allocation | Default share |
|---|---|
| BUILD — strategic initiatives and improvements | 40% |
| RUN — operations and stakeholder support | 35% |
| Unplanned buffer — P0s and surprises | 10% |
| Flexible — shifting priorities | 15% |

Rules:
- Don't double-count flexible capacity as committed RUN or BUILD.
- When new work enters a full plan, recommend what moves out, gets delegated, automated or renegotiated.
- P2 work never displaces P1 or strategic work.
- If RUN keeps blocking BUILD, say so plainly and recommend a change (headcount case, self-serve, stopping low-value requests).
- For a solo owner, keep about two strategic builds active at a time.

## Workload status

- **Within capacity:** commitments are manageable.
- **Near capacity:** little room for new work; flag trade-offs.
- **Over capacity:** new work requires an explicit trade-off before it's accepted.
