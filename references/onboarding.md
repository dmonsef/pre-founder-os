# Onboarding

Run this flow when a founder uses the Pre Founder OS skill for the first time, or when they explicitly ask to "set up," "onboard," "start a sprint," or "start fresh." The goal: get them from zero to a working sprint with recurring scheduled tasks in about 15 minutes.

Do not rush. Do not dump all the questions at once. One step at a time. If they already know the framework, move faster; if they don't, pause and explain.

## Before you start

Check whether `~/pre/` already exists. If it does, this is not a first-time setup. Ask: "You already have a Pre folder set up. Are you starting a new sprint, continuing the current one, or resetting from scratch?" Route accordingly.

If `~/pre/` does not exist, proceed with the full flow below.

## Step 1: Frame the system (30 seconds)

Tell the founder, briefly, what they're about to set up. The framing matters — it sets expectations for how this skill is going to behave, which is different from most founder tools.

> "Pre is a 10-week sprint system. You pick one ambitious North Star, break it into milestones every couple weeks, and execute week by week.
>
> I'm going to act like a co-founder-quality operator, not a form to fill out. That means I'll read what's in your files, pull data from any tools you've connected, research your space when I need to, and show up with specific proposals — goals, milestones, drafts — for you to pick from, swap, or override. Your judgment always wins. But you shouldn't have to generate every first draft from a blank canvas. That's my job.
>
> Let's set up your first sprint. Ready?"

Wait for confirmation.

## Step 2: Get founder context

Ask, in one message, these three things (use an elicitation widget if available to make it tappable):

1. **What are you building?** (one or two sentences is fine)
2. **What phase are you in?** Options: pre-launch (no product yet), 0 to 1 (early users, figuring out PMF), 1 to 10 (PMF signal, growing), 10+ (scaling).
3. **How many hours per week can you realistically put into this?** Options: <10, 10-25, 25-40, 40+.

Write their answers to `~/pre/founder.md` in this format:

```markdown
# Founder Profile

- **Name:** [ask if not known]
- **Company:** [from answer 1]
- **What we're building:** [from answer 1]
- **Current phase:** [from answer 2]
- **Weekly capacity:** [from answer 3]
- **Created:** [today's date]
```

## Step 3: Set the North Star

**Do not open with "what's your North Star?"** That's the nanny pattern. Instead, research first and propose.

Before asking, do this silently:

1. Re-read the founder's answers from Step 2.
2. If you don't have strong context on their space, search for comparable early-stage companies at their phase. What do founders at this stage in this space typically focus on for a 10-week window?
3. If they named a competitor or reference company, search for their growth benchmarks.
4. Think about what would be ambitious-but-possible for their phase and capacity.

Then come to them with 2-3 candidate North Stars with different profiles. Format:

> "Based on your phase ([phase]) and what I'm seeing in the space, here are three ways we could frame the next 10 weeks:
>
> **a. Revenue-forward:** [specific number by week 10] — aggressive given your current state but achievable if [condition]. Forces you to solve [problem] fast.
>
> **b. Validation-forward:** [specific outcome — e.g., "10 users who love it and 3 willing to pay"] — conservative on revenue, ambitious on learning. Good if you're not yet sure [key assumption].
>
> **c. Distribution-forward:** [specific target — e.g., "one repeatable channel producing 5 qualified leads/week"] — bets on [channel]. Works if you think [channel signal].
>
> My hunch: [the one you'd pick, with reasoning]. Which resonates, or tell me where I'm off?"

Apply the ambition check after they pick: if they picked the safest option, ask "how sure are you that's ambitious enough?" The 3x rule from `sprints.md` applies. If they know exactly how they'd hit it, push harder.

Keep iterating until the North Star passes the "can you measure this?" test. Numbers with deadlines only.

## Step 4: Set milestones

**Do not ask "what should your milestones be?"** Work backward from the North Star yourself and propose. Milestones are every ~2 weeks, so 4-5 milestones for a 10-week sprint.

Format:

> "North Star is [their choice] by week 10. Working backward:
>
> - **Week 2:** [milestone] — feasibility check on [thing], validates [assumption]
> - **Week 4:** [milestone] — first hard signal: [specific proof]
> - **Week 6:** [milestone] — halfway gate, [specific metric threshold]
> - **Week 8:** [milestone] — should be [specific state] by here to finish on time
> - **Week 10:** [North Star restated]
>
> Two I'm less sure about: Week 4 might be aggressive if [X]; Week 6 assumes [Y]. Anything feel wrong, or should I tighten any of these?"

The explicit "I'm less sure about these" tells the founder where to push, instead of making them review every line.

If the founder isn't engaging with the milestones or wants a different shape, offer 2-3 alternative milestone arcs and let them pick. Don't make them generate from scratch.

Write the sprint to `~/pre/current-sprint/sprint.md`:

```markdown
# Sprint: [start date] to [end date]

## North Star
[their North Star]

## Milestones
- Week 2: [milestone]
- Week 4: [milestone]
- Week 6: [milestone]
- Week 8: [milestone]
- Week 10: [milestone]

## Notes
[anything worth capturing about why this sprint, what they're betting on, what you considered and discarded]
```

## Step 5: Set this week's goals

**Don't ask "what are your goals for this week?"** Propose them.

Using the milestones we just wrote plus everything you know about the founder from Steps 2-4, draft 3-5 goals for week 1 that push toward the week 2 milestone. Each one should already pass the goal audit — measurable, outcome-shaped, in the founder's control.

Format:

> "Week 1 goals I'd prioritize, all pointed at the Week 2 milestone ([milestone]):
>
> 1. **[Specific goal with a number]** — [why: tied to milestone component]
> 2. **[Specific goal with a number]** — [why]
> 3. **[Specific goal with a number]** — [why]
> 4. **[Specific goal with a number]** — [why]
>
> I'm most confident on #1 and #2. #3 and #4 are my best guesses — you know your week better than I do. Swap, edit, or add your own."

Write to `~/pre/current-sprint/week-01.md`:

```markdown
# Week 1: [start date] to [end date]

## Goals
1. [goal] — status: pending
2. [goal] — status: pending
3. [goal] — status: pending

## Notes
[context about the plan, what was considered and discarded]
```

## Step 6: Accountability partners

Ask: "Who's going to see your weekly progress? The point is pressure — people whose silence stings if you miss a week. Pick 2-3."

Guide them based on `references/accountability.md`. Good picks: investors, mentors, other founders, spouse. Bad picks: anyone who will just say "nice job" regardless.

Write to `~/pre/accountability-partners.md`:

```markdown
# Accountability Partners

- [name] — [email] — [role: investor / mentor / peer / spouse]
- [name] — [email] — [role]

## Cadence
Weekly report sent: [day, default Friday]
```

If Gmail is connected and they want weekly reports actually sent, note that the Friday retro scheduled task (Step 8) will handle that.

## Step 7: One-liner and metrics (optional, can skip on first pass)

If the founder is past initial launch, capture these. If they're pre-launch, skip until they have a product.

- **One-liner**: ask for their current version, then run the check in `references/one-liner.md`. Save to `~/pre/one-liner.md` with date and version history.
- **Primary metric**: which number tells them if they're winning? Write to `~/pre/metrics.md` with the target and starting value.

## Step 8: Set up scheduled tasks (the key to making this a system)

This is where the magic happens. Without scheduled tasks, the skill is a one-off conversation. With them, it's an operating rhythm.

Explain briefly:

> "The last step is setting up four recurring tasks so this runs on a rhythm instead of when you remember. I'll give you the prompts; you paste them into Claude's scheduled tasks. Two options for where:
>
> 1. **Cloud scheduled tasks** (recommended): run at claude.ai/code/scheduled. They run on Anthropic's servers so they fire even when your laptop's closed.
> 2. **Claude Desktop Cowork**: open the Cowork section of the desktop app and go to Scheduled. These only run when the app is open.
>
> Cloud is more reliable. Desktop has direct file access. Pick whichever fits; you can always add more later."

Then offer the four tasks from `assets/scheduled-tasks/`. For each, show:

1. A one-line description of what it does
2. The recommended cadence (Monday 8am, Wednesday 2pm, Friday 4pm, first of month 9am)
3. The prompt to paste

Let them opt in or out of each individually. Some founders will want all four; some will start with just Monday planning and Friday retro.

After they've set up the tasks, confirm with them what they've scheduled and note it in `~/pre/founder.md` under a "Scheduled tasks" section so future invocations can reference what's running.

## Step 9: Close out

Summarize what they just set up, in their own language:

> "Okay, here's what's live:
>
> - Sprint: [North Star] by [date], with [N] milestones
> - Week 1 goals: [list]
> - Accountability partners: [names]
> - Scheduled tasks: [which ones they set up]
>
> Your next move is [the first concrete thing from this week's goals]. Talk to you [next scheduled touchpoint]."

Do not add a pep talk. The system is the pep talk. Let them go do the work.

## If they resist any part

Some founders will push back on things. The handbook has opinions for a reason; most of them are right; hold the line on the ones that matter, flex on the ones that don't.

- **Refuse to name accountability partners.** That's their call. Note it in the file and move on. They can add partners later.
- **Want 8 weekly goals instead of 5.** Push back once, cite the handbook rule, then let them do what they want. They'll figure it out in week 2.
- **Want a 4-week sprint instead of 10.** Push back. The 10-week frame is load-bearing. If they really insist, let them, but note that the milestones and scheduled tasks assume 10 weeks.
- **Don't want scheduled tasks.** Push back. This is the part that makes the skill actually work over time. Without them, it's just another one-off chat. If they still refuse, offer to at least save the prompts to a local file they can run manually.
