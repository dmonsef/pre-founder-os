# Friday Retro

**Recommended cadence:** Every Friday at 4pm local time
**Where to set it up:** Claude.ai cloud scheduled tasks or Claude Desktop Cowork
**What it does:** Runs the weekly retro as a 2-minute conversation, saves it, and (if configured) drafts the weekly update email to accountability partners.

## The prompt

---

Use the pre-founder-os skill. It's Friday and we're closing the week.

Read these files in `~/pre/`:

- `current-sprint/week-NN.md` — this week's goals and statuses
- `current-sprint/sprint.md` — the North Star and milestones
- `accountability-partners.md` — who receives the update
- `metrics.md` — primary metric

If connectors are available, pull this week's real data before we start:

- Stripe for any change in MRR, new customers, churn
- GitHub for what actually shipped
- Linear for closed tickets
- PostHog for active user change
- Any other connector relevant to this sprint's goals

Then run the retro conversation. Follow the protocol in the skill's `SKILL.md` under "The weekly retro":

1. For each goal, ask: done, partial, or not done? If partial, what's the number actually hit? Use connector data where available — don't ask me about MRR if you can check Stripe.
2. Ask these three questions, one at a time, and wait for my answer to each:
   - What worked this week?
   - What didn't?
   - What got in the way?
3. Update `week-NN.md` with final statuses.
4. Save the retro to `current-sprint/retros/week-NN.md` using this format:

```
# Week N Retro — [date]

## Goals
1. [goal] — [done/partial/not done] [— actual number if partial]
2. ...

## What worked
[my answer]

## What didn't
[my answer]

## What got in the way
[my answer]

## Primary metric snapshot
[where I was at the end of this week — pull from connectors if available]
```

Finally, if Gmail is connected and I have accountability partners configured, draft the weekly update email using the format in `references/accountability.md`. Show me the draft. Do not send without my explicit confirmation.

Push back if I try to spin a narrative about why something didn't get done. The retro is for honest self-reflection, not for spin. If a goal didn't get done because "the buyer was slow," ask what I did to push it forward.

Don't add a pep talk at the end. Let me go enjoy the weekend.

---

## What to expect

5-10 minutes, depending on how many goals and how much the founder wants to talk through what didn't work.

This is the most important of the four tasks. Even founders who skip Monday and Wednesday tend to keep Friday, because it's the one that creates the accountability loop.

## Failure modes to avoid

- **Don't let the founder mark everything "done" without proof.** If there's connector data that says otherwise, bring it up.
- **Don't accept spin.** "The buyer was slow" is not a retro answer. "I didn't push the buyer hard enough on Monday and Tuesday" is.
- **Don't send the weekly update email without explicit confirmation.** Always show the draft, always wait for approval.
- **Don't cheerlead a bad week.** A founder who missed 3 of 5 goals doesn't need encouragement. They need to look at what happened and plan better for next week.
