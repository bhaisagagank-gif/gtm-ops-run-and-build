# Output formats

Keep outputs decision-oriented. Lead with what needs attention; keep resolved items brief. Use plain, confident language.

## Daily brief

```
Daily Ops Brief — [date]

Headline: [one sentence on what matters most today]

Needs you today
- [P0/P1] [item] — [requester] — [why it matters] — Next: [action]

Due today / breaching SLA
- [item] — [priority] — [days open vs target] — Next: [action]

New since last brief
- [P1/P2/S] [item] — [requester, source] — Next: [action]

Waiting on others
- [item] — waiting on [name] since [date]

Resolved since last brief
- [item] ([who resolved it])

Not mine (redirect)
- [item] → [suggested owner]

Top three today
1. ...
2. ...
3. ...

Pattern worth automating (only with real evidence)
- [pattern] — [evidence] — [suggested fix]
```

If a source couldn't be checked, add one line saying which and why.

## Weekly review

```
Weekly Review — [week start] to [week end]

Summary: [2–3 sentences: what moved, what's stuck, overall load]

Numbers
- New: [n] | Resolved: [n] | Resolved last week: [n]
- SLA attainment: [x%] | P1 cycle time: [d] days | P2 cycle time: [d] days
- Breaching now: [n]
- RUN vs BUILD: [x% / y%]

What went well
What's stuck (and the decision needed)
Recurring requests → automation or self-serve candidates
Strategic initiatives: progress, blockers, next decisions
Capacity: within / near / over — and what should move

Recommendations for next week
1. ...
2. ...
3. ...
```

## SLA report

```
SLA Report — [period]

Attainment: [met]/[total] ([x%])
Cycle time: P1 [d] days, P2 [d] days
Breaching now: [list with days open vs target]
Missed in period: [list with reason, e.g., waiting on vendor]
Note: clock paused for items waiting on others or on hold.
```

## Single-item classification

```
Classification: [P0/P1/P2/S/Not mine] — [RUN/BUILD]
Why: [1–2 sentences against the definitions]
SLA: [target]
Next action: [one step]
Trade-off: [what it displaces, if the plan is full]
```
