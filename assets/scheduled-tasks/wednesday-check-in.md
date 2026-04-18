# Wednesday Mid-Week Check-in

**Recommended cadence:** Every Wednesday at 2pm local time
**Where to set it up:** Claude.ai cloud scheduled tasks or Claude Desktop Cowork
**What it does:** Catches a drifting week before it's lost. The "when falling behind" protocol from the handbook, run proactively.

## The prompt

---

Use the pre-founder-os skill. It's Wednesday afternoon and I'm halfway through the week.

Read `~/pre/current-sprint/week-NN.md` for this week's goals.

For each goal, check what real progress has been made:

- If Stripe, GitHub, Linear, or PostHog are connected, pull the relevant data
- If the goal isn't trackable through a connector, just list it and ask me directly

Then tell me:

1. Which goals are on pace and which are not
2. For any goal that's behind, what's the single next action that moves it forward by end of day today
3. If I'm clearly off pace for the week overall, invoke the falling-behind protocol: pick the one goal that matters most, recommend I clear the afternoon, work on nothing else until real progress is made

Ask me directly about the goals you couldn't check through connectors. Don't accept vague answers. "Making progress" is not an answer. "I got 4 out of the 10 interviews booked" is an answer.

Update the statuses in `week-NN.md` based on what I tell you and what the connectors show.

Be short. This is a 2-minute check, not a full conversation. If I'm on pace, keep it to one line. If I'm not, push hard.

---

## What to expect

This is the shortest of the four tasks. 1-3 minutes on a good week, maybe 5 if the founder is actually behind and needs to replan the second half.

The value of this task is asymmetric: on weeks where the founder is on track, it's a cheap confirmation. On weeks where they're drifting, it saves the week. Almost every founder using Pre in its original form found this was the task they'd skip for the first few weeks and then start running religiously once it saved a sprint.

## Optional variant

If the founder is very early-stage and doesn't have enough instrumentation for this to add much value, they can skip this task entirely and just do Monday + Friday. But most founders at any stage benefit from the mid-week gut-check.
