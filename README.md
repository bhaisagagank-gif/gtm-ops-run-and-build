# Run & Build: a GTM Operations Operating Model

An open operating model — and a ready-to-install Claude Skill — for running a Marketing Ops, RevOps or GTM Systems function, especially a small or solo one.

It helps you keep the business running (**RUN**) while still building new capabilities (**BUILD**): one intake view for every request, honest prioritisation, SLAs, capacity guardrails, a strategic portfolio, and outcome-based measurement.

---

## The problem

GTM Operations teams get pulled into reactive requests and one-off fixes with no clear way to decide what matters most:

- Requests arrive through chat, email, meetings and hallway asks.
- Whoever asks loudest gets served first.
- Urgent work keeps pushing out strategic work.
- Ops absorbs work that belongs to other teams.
- The team is judged by tickets closed, not business outcomes.

## What's in this repo

```
run-and-build/                ← the Claude Skill
├── SKILL.md                  ← when it activates and how it works
├── references/
│   ├── classification.md     ← P0, P1, P2, Strategic, Not mine
│   ├── sla-and-capacity.md   ← SLAs, clock rules, capacity split
│   ├── strategic.md          ← validation, lifecycle, horizons, business case
│   ├── measurement.md        ← SLA attainment, cycle time, before → after
│   └── output-formats.md     ← daily brief, weekly review, SLA report
└── templates/
    ├── ops-config.md         ← your rules, SLAs and capacity split
    ├── request-register.csv  ← starter register
    └── weekly-review.md      ← weekly review worksheet
```

The files work on their own as a framework you can read and adapt, with or without the skill.

---

## Install the skill

**Claude apps:** add the `run-and-build` folder (or the packaged `.skill` file from the Releases page) as a skill in your Claude settings.

**Claude Code:** copy the `run-and-build` folder into your skills directory, for example `~/.claude/skills/run-and-build/` for all projects or `.claude/skills/run-and-build/` inside one project.

For the best results, connect the tools you get requests through (for example Slack, email and your meeting-notes tool) so Claude can read them during triage.

## Set it up (5 minutes)

1. Copy `templates/ops-config.md` into your project or a Claude Project's knowledge.
2. Fill in your time zone, week start, SLA targets, capacity split and the sources to read.
3. Add standing rules as you go — every time you correct a classification, write the rule down.

## Use it

Just ask in plain language. The skill activates when the request matches:

| You say | What happens |
|---|---|
| "Triage my requests from today" | Reads your sources, deduplicates, classifies P0/P1/P2/S/Not mine, flags SLA breaches, sets your top three |
| "Is this a P0?" | Classifies one item against the rules and explains why |
| "What's overdue?" | SLA report: attainment, cycle time, items breaching now |
| "Weekly review" | New vs resolved, RUN vs BUILD, SLA trend, what to stop or challenge |
| "Should we build this?" | Validates the problem, then assigns status, horizon and owner, and recommends invest / validate / defer / reject |
| "Help me set this up" | Walks you through the config |

The skill is read-only by default: it never sends messages, changes systems or makes commitments without your approval.

---

## The model in brief

**Classification**
- **P0:** revenue or core operations disrupted right now (urgent wording alone doesn't count)
- **P1:** meaningful impact, near deadline or blocked launch
- **P2:** routine — batch, defer, redirect or automate
- **S:** capability-building projects and playbooks (never campaigns)
- **Not mine:** another team's work — redirect and keep on record

**Default SLAs (business days to resolve):** P0 1 · P1 3 · P2 5. The clock pauses while waiting on others or on hold.

**Capacity split:** 40% BUILD · 35% RUN · 10% buffer · 15% flexible. A full plan means something moves out before something new comes in.

**Strategic governance:** every initiative has a validation status, lifecycle stage, horizon, business owner, evidence and next decision. Nothing counts as delivered until its outcome is measured.

**Measurement:** SLA attainment, cycle time, RUN vs BUILD share, self-serve conversions — and every solved problem recorded as *before → after*.

**Cadence:** daily triage · weekly review · monthly impact review · quarterly portfolio reset.

## Reference implementation (anonymised)

Applied by a solo Marketing Ops owner at a B2B SaaS company over four weeks:

- About 90 work items captured and classified from chat, email and meetings
- 93% of requests resolved within SLA; P1s closed in 1.6 business days on average, P2s in 2.3
- A routing gap sending inbound leads to the ops owner as fallback was closed
- Region data now fills automatically on new leads, with older records backfilled
- A recurring weekly list request became a self-serve report

## Lessons learned

- Separate notifications from tasks early — alert volume hides the real work.
- Ownership calls matter as much as prioritisation.
- Record raised and resolved dates from day one; cycle time and SLA attainment come for free.
- Name your standing rules — each one is a judgement call you never repeat.

## Contributing

Adaptations and improvements are welcome. Open an issue or pull request describing the change and the context it worked in.
