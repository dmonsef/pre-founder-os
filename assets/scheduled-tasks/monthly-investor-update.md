# Monthly Investor Update

**Recommended cadence:** First of every month at 9am local time
**Where to set it up:** Claude.ai cloud scheduled tasks or Claude Desktop Cowork
**What it does:** Drafts a short monthly investor update based on the last 4 weeks of retros and real metric data. The founder reviews and sends.

## The prompt

---

Use the pre-founder-os skill. It's the first of the month — time for the monthly investor update.

Read these files in `~/pre/`:

- `founder.md` for my company and context
- `current-sprint/sprint.md` for the North Star and milestones
- All four `current-sprint/retros/week-NN.md` files from the last 4 weeks
- `metrics.md` for the primary metric
- `accountability-partners.md` for the recipient list

If connectors are available, pull the current state and the month-over-month change for:

- Stripe (MRR, new customers, churn, ARPU)
- Any other primary-metric source

Then draft a monthly update in this format. Keep it short. Investors skim.

```
Subject: [Company] — [Month] update

**TL;DR:** [one sentence: biggest win, biggest challenge, what I'm focused on]

**Metrics:**
- [Primary metric]: [current] (was [last month], [% change])
- [Supporting metric]: [current] (change)
- [Supporting metric]: [current] (change)

**Progress this month:**
- [win 1 — one line]
- [win 2 — one line]
- [win 3 — one line]

**Challenges:**
- [honest challenge — one line]
- [honest challenge — one line]

**What I'm focused on next month:**
- [priority 1]
- [priority 2]

**Asks:**
- [specific ask — intro, feedback, hire, nothing]

Thanks,
[Name]
```

Rules:

1. Pull the wins and challenges from the actual retros. Don't invent. If a win isn't in the retros, don't put it in the update.
2. Don't sugarcoat challenges. Investors respect honesty more than polish.
3. "Asks" should be specific — an intro to a named persona, feedback on a specific question, help with a specific hire. "Any thoughts welcome" is not an ask.
4. If there's nothing to ask for this month, write "Nothing this month — will follow up when I need something." That's also fine.

Show me the draft. If Gmail is connected, offer to send it to everyone in `accountability-partners.md` once I approve. Do not send without explicit confirmation.

---

## What to expect

Takes about 5 minutes once the retros are populated. Most of the work is already done — the retros contain the wins, the challenges, and the honest assessment. This task just consolidates them into a format investors can read in 60 seconds.

## Why this matters

The monthly investor update is the single most valuable founder deliverable outside the product itself. Investors who see honest, consistent updates are 10x more likely to follow on, make intros, and advocate for the company when it matters. Missing months is the #1 signal that a company is struggling.

Having this task automated means the founder never misses a month. The draft is ready; all they have to do is review and send.

## Failure modes to avoid

- **Don't inflate the wins.** If the retros say the week was mixed, the month probably was too. Write it honestly.
- **Don't hide challenges.** Investors have seen every challenge in the book. They invest in founders who can name problems, not founders who pretend problems don't exist.
- **Don't send without the founder reading it.** This is the most public piece of writing this skill produces. The founder has to own every word.
