# Monday Morning Planning

**Recommended cadence:** Every Monday at 8am local time
**Where to set it up:** Claude.ai cloud scheduled tasks (claude.ai/code/scheduled) or Claude Desktop Cowork scheduled tasks
**What it does:** Kicks off the week by reading sprint state, pulling real data, researching what needs researching, and showing up with 3-5 proposed weekly goals for the founder to pick from, swap, or override.

## The prompt

Paste this verbatim into the scheduled task prompt field. Replace `~/pre/` with the actual path if the folder is somewhere else.

---

Use the pre-founder-os skill. Read `references/acting-like-a-cofounder.md` first — this whole task operates in propose-first mode.

It's Monday morning and we're starting a new sprint week. Do this work silently before you come to me:

**1. Read all of `~/pre/` that's relevant:**
- `founder.md` for my context, phase, capacity
- `current-sprint/sprint.md` for the North Star and milestones
- The most recent `current-sprint/week-NN.md` to see how last week ended
- The most recent `current-sprint/retros/week-NN.md` for what worked, what didn't, what got in the way
- `metrics.md` for the primary metric and weekly target
- `customers/interviews.md` if we're in a validation-heavy phase

**2. Pull real data from connectors if available:**
- Stripe for MRR, new customers, churn delta
- GitHub for what shipped last week
- Linear for closed tickets
- PostHog for active user change
- Google Calendar for what's booked this week (realistic capacity)

**3. Research what you don't know:**
- If my company operates in a space you don't have strong context on, search for comparable early-stage companies at my phase and what they typically prioritize. Don't generalize — understand my specific domain.
- If a competitor or reference company is mentioned anywhere in my files, look them up to calibrate ambition.
- If a specific channel, tactic, or integration is in play that you're unsure about, search for it.

**4. Then come to me with a proposal.** Format:

> "Week [N] of 10. The Week [N+1 or N+2] milestone is [milestone]. Here's what I'm seeing:
>
> - **Primary metric:** [current] vs. target [$Y]. Weekly delta needed: [$Z]. Last week you moved it by [amount].
> - **Last week's retro signal:** [one sentence — what worked, what didn't, what's worth carrying]
> - **Capacity this week:** [N hours booked in meetings, so ~M hours of deep work available]
>
> Based on all of that, here are 4 goals I'd prioritize. Each is outcome-shaped and connected to the next milestone:
>
> 1. **[Specific goal with a number]** — closes the gap on [milestone component] and picks up [thing that slipped last week]
> 2. **[Specific goal with a number]** — directly moves the primary metric by [$amount] through [specific motion]
> 3. **[Specific goal with a number]** — [reason tied to retro or research]
> 4. **[Specific goal with a number]** — [reason]
>
> Which ones work? Swap, edit, or write your own. I'm confident on #1 and #2; #3 and #4 are my best guesses but you know the week better."

**Important:** Each goal you propose must already pass the goal audit — measurable, outcome-shaped, in my control, connected to the milestone. Don't propose "work on X" or "make progress on Y."

Once I confirm (possibly after editing or swapping), write the week to `current-sprint/week-NN.md`:

```
# Week N: [start date] to [end date]

## Goals
1. [goal] — status: pending
2. [goal] — status: pending
3. [goal] — status: pending

## Notes
[context about the plan, what you considered and discarded, what to watch for]
```

Be direct. Don't write a pep talk. If my primary metric slipped last week, lead with that. If I'm behind on the sprint, tell me what this week needs to do to get us back on pace. If two of the 3 goals you're proposing are things I pushed against last week, name that.

---

## What to expect

First Monday of a sprint takes 5-10 minutes because context is being built from scratch. After that, the skill has a growing understanding of the founder and most of the prep happens silently before the conversation even starts. A typical Monday is: proposal lands, founder swaps one goal, picks the others, confirms. 2-3 minutes.

If Gmail is connected and the founder wants to send a "kicking off week N" note to accountability partners, offer to draft it. Optional.

## Failure modes to avoid

- **Don't ask "what are your goals for this week?"** That's the nanny pattern. Read the files, do the research, and propose.
- **Don't propose vague goals that you'd later audit.** Pre-audit your own proposals.
- **Don't copy last week's unfinished goals forward without asking.** A goal that didn't finish is a signal, not a to-do.
- **Don't over-propose.** If you have 7 candidate goals, narrow to the best 4 before showing up. The founder's time isn't for sorting your thinking.
