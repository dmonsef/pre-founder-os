# Your Key Metrics

Doing a startup is like pushing a boulder up a hill. It's a ton of work. Getting that first movement is fricking hard and it might not move much. Likely it moves forward a bit and slips back a bit, but hopefully step by step it gets higher and higher, and if you're lucky it starts rolling down the other side and you have a whole new problem of keeping up with it.

If you don't measure what you're doing, you can't know if your boulder is moving. You don't know if the method you just tried to move it worked, how well, or how it could be improved.

## If the founder hasn't launched yet

Pre-launch, this article might not apply. The focus should be on validating the idea with customers and building the MVP.

Once launched, come back. The first metric is simple: **get 10 users who love it**.

How to know they love it? Not by asking. By watching:

- They come back without being reminded
- They use it multiple times per week
- They tell others about it unprompted
- They complain when it breaks

Track who signed up, when they last used it, and how often they come back. A spreadsheet is fine. Don't build fancy dashboards yet.

## Pick one number

Post-launch, pick one primary metric. Not five. One. The single number that tells you if you're winning.

For most startups, this is **revenue**. Revenue is proof people want what was built enough to pay for it.

- B2B SaaS: Monthly Recurring Revenue (MRR)
- Marketplace or e-commerce: monthly revenue
- Consumer: MRR or active users, depending on the model

### If not charging yet

Some products need scale before monetization. Social apps, open source projects, free tools building an audience.

In those cases, pick the metric that measures real usage. Not signups. Not downloads. Not page views. Usage.

- Daily use: Daily Active Users (DAU)
- Weekly use: Weekly Active Users (WAU)
- Developer tools: active integrations or API calls

The primary metric should answer: "Are people using this thing enough that they'd pay for it (or we can monetize them later)?"

## Track a few supporting metrics

The primary metric is how the founder judges themselves. But pick 2-3 supporting metrics that help understand what's driving it.

If the primary metric is MRR, track:

- **New customers** — are they growing the top of the funnel?
- **Churn** — are customers leaving?
- **Active usage** — are customers actually using it? (This predicts churn.)

Don't track ten things. Track the 2-3 that directly impact the primary metric. Everything else is noise.

## Build a simple dashboard

The founder needs to see their numbers every day. Not buried in analytics tools. Visible. In their face.

Start simple:

- **Google Sheets** for manual data
- **Stripe Dashboard** if they're already using Stripe
- **A simple SQL query** pinned to the browser if there's a database

Make the primary metric big. Make it the first thing seen. Supporting metrics go below.

Do not spend money on analytics tools until there are hundreds of users. Too early. Keep it simple.

If Stripe, Supabase, or PostHog are connected via MCP, Claude can pull these numbers live during planning and retros. That's the preferred approach — the numbers don't live in the founder's head, they come from the source.

## Check it every day

The dashboard should be the founder's homepage. Or a pinned tab. Or a bookmark they hit first thing every morning.

They should feel it when the number doesn't move. That discomfort is useful. It forces the question: "Why isn't this growing? What do I need to change?"

Airbnb founders wrote their weekly revenue goal on their bathroom mirror. They saw it every day. That pressure kept them moving.

Make the metric unavoidable. If the founder has to remember to check it, they won't.

## Set weekly goals around it

The metric isn't just for tracking. It's the foundation of weekly goals.

At $2K MRR today and wanting to hit $10K in 10 weeks? Work backward. $800/week in growth. Now they know what to hit each week.

Write it down. Track it. If behind in week 3, they know immediately. Adjust now, not in week 9 when it's too late.

Examples of good weekly goals tied to the metric:

- "Increase MRR from $2K to $2.8K"
- "Get 5 new paying customers"
- "Hit 1,000 WAU (up from 750)"
- "Close 3 pilots, move pipeline from 10 to 13 total"

Weekly goals prevent surprises. Without checkpoints, the founder doesn't realize they're off track until it's too late.

## The plan will change

The metric will get revised as the founder learns more. That's fine. The point is to have one, track it, and use it to drive decisions.

Without a metric, guessing. With a metric, knowing if winning or losing. And being able to adjust.

## How Claude tracks this

During onboarding (or later, when the founder launches), set up `~/pre/metrics.md`:

```markdown
# Metrics

## Primary Metric: [MRR / WAU / etc.]
- **Starting value:** [X on date]
- **Sprint target:** [Y by end of sprint]
- **Weekly target:** [delta per week]

## Supporting Metrics
- [metric 1]: [current]
- [metric 2]: [current]
- [metric 3]: [current]

## Weekly Snapshots
| Week | Primary | Supporting 1 | Supporting 2 | Supporting 3 |
|------|---------|--------------|--------------|--------------|
| 1    |         |              |              |              |
```

At the start of each week, fill in last week's snapshot. If connectors are available, pull the real numbers. If not, ask the founder to check their own dashboard and report.

During retros, if the primary metric didn't move this week, make that the first thing discussed. Not the goals. The number.
