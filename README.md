# Pre Founder OS (Claude Skill)

An opinionated operating system for early-stage startup founders, running as a Claude skill.

This is the open-source successor to [Pre](https://www.buildwithpre.com), a YC-backed founder execution tool that ran from 2024 to 2026. When we shut down the hosted product, we didn't want the methodology to disappear. So we ported it to a Claude skill and released it for free.

The methodology is unchanged. 10-week sprints. One North Star. Milestones every two weeks. Weekly goals audited for measurability. Honest retros. Accountability partners who see the work. Show don't tell.

If it helped you, credit goes to Darius Monsef and the Pre team.

## What this gives you

- A **Claude skill** (`pre-founder-os`) that acts as your execution advisor. It knows the full Pre handbook and follows the original Pre agent's behaviors — goal audits, weekly retros, pushing back on vague goals, refusing to cheerlead.
- A **folder structure** on your machine (`~/pre/`) that holds your sprint, goals, retros, metrics, and customer interview log. Your data stays with you. No hosted service, no database, no subscription.
- Four **scheduled task prompts** you paste into Claude's scheduler for a recurring rhythm:
  - Monday morning planning
  - Wednesday mid-week check-in
  - Friday retro
  - Monthly investor update
- The full **Pre handbook** as reference material the skill reads on demand.

## Install (5 minutes)

### 1. Install the skill

You need the `.skill` file (`pre-founder-os.skill`, downloadable from [releases]).

**Option A — Claude Desktop (easiest):**

1. Open Claude Desktop
2. Go to Settings → Capabilities → Skills
3. Click "Install skill from file" and select `pre-founder-os.skill`
4. Done

**Option B — Claude.ai web:**

1. Go to claude.ai, open Settings → Capabilities → Skills
2. Upload `pre-founder-os.skill`
3. Done

### 2. Run onboarding

Start a new Claude conversation and say:

> "Set me up with the Pre Founder OS."

The skill walks you through a 15-minute onboarding: your context, your North Star, milestones, this week's goals, your accountability partners, and then helps you set up the recurring scheduled tasks.

### 3. Connect the tools you want (optional but recommended)

The skill gets a lot more useful when it can pull real data instead of asking you. Connect whichever of these apply to your business:

- **Stripe** for revenue / MRR
- **GitHub** for shipped code
- **Linear** for closed tickets
- **PostHog** or **Supabase** for product analytics
- **Slack** for team comms context
- **Gmail** for sending weekly updates to accountability partners
- **Google Calendar** for calendar context

Go to Claude Settings → Connectors to add any of these.

### 4. Schedule the recurring tasks

During onboarding, the skill gives you the exact prompts to paste into Claude's scheduler. Two places you can put them:

- **Cloud scheduled tasks** (recommended): claude.ai/code/scheduled. These run on Anthropic's servers, so they fire even when your laptop is closed.
- **Desktop Cowork scheduled tasks**: in the Claude Desktop app, the Scheduled section of Cowork. These only run while the app is open, but they have direct access to your local files.

Most founders use all four tasks. Some start with just Monday and Friday and add the others later. Your call.

## How it works day-to-day

Once set up, the rhythm is:

- **Monday morning:** Claude pings you with last week's state, your position in the sprint, and drafts 3-5 weekly goals for you to confirm.
- **Wednesday 2pm:** Quick mid-week check-in. Pulls real data from your connectors, tells you which goals are on pace and which aren't. If you're behind, invokes the falling-behind protocol.
- **Friday 4pm:** Two-minute retro. What got done, what didn't, what worked, what didn't, what got in the way. Drafts the weekly update email for your accountability partners.
- **First of the month:** Drafts your monthly investor update from the last four retros plus real metric data. You review and send.

Between those, you can talk to Claude anytime. "Help me write this week's goals." "What should I focus on today?" "Audit my one-liner." "I'm thinking about going to this conference — should I?" The skill is loaded and ready.

## What's in the skill

```
pre-founder-os/
├── SKILL.md                              # Main instructions and behaviors
├── references/                           # The full Pre handbook
│   ├── onboarding.md                     # First-time setup flow
│   ├── sprints.md
│   ├── weekly-goals.md                   # Includes the goal audit
│   ├── accountability.md
│   ├── daily-execution.md
│   ├── validation.md
│   ├── interviews.md
│   ├── mvp.md
│   ├── sales.md
│   ├── one-liner.md
│   ├── premature-optimization.md
│   ├── metrics.md
│   └── events.md
└── assets/
    ├── scheduled-tasks/                  # Prompts to paste into Claude's scheduler
    │   ├── monday-planning.md
    │   ├── wednesday-check-in.md
    │   ├── friday-retro.md
    │   └── monthly-investor-update.md
    └── templates/                        # File skeletons the skill writes
        ├── founder-template.md
        ├── sprint-template.md
        ├── week-template.md
        └── retro-template.md
```

## Philosophy

A few things that were true of Pre and are true of this skill:

- **Pre is not for startup tourists.** This skill will push you. If you want a cheerleader, go elsewhere.
- **Show don't tell.** The skill prefers data from your connected tools over what you say you did.
- **Some red weeks are healthy.** A sprint with all-green weeks usually means goals weren't ambitious enough.
- **Stay in phase.** The skill will redirect you if you're working on problems you haven't earned yet (fundraising strategy pre-PMF, scale planning pre-revenue, etc.).
- **Your data is yours.** Everything lives in `~/pre/` on your machine. No hosted service, no login, no sync, no lock-in. Back it up however you back up the rest of your work.

## Limitations (honest version)

- **No scheduled-task reminders outside Claude.** If you want SMS reminders at 8am Monday, the skill can't do that. The scheduler runs inside Claude.
- **Paid Claude plan required for scheduled tasks.** Scheduled tasks are a Pro/Max/Team/Enterprise feature. The skill itself works on any plan; the scheduled rhythm does not.
- **Connector setup is a one-time friction.** Connecting Stripe, GitHub, etc. takes 10-20 minutes total. Worth it, but not zero friction.
- **No multi-founder sync.** The original Pre had co-founder collaboration. This skill is single-founder by design; each co-founder runs their own folder. You can share retros manually if you want.
- **The methodology has opinions.** If you hate 10-week sprints, North Stars, or the idea of accountability partners, this isn't for you. Most of the value comes from the opinionated parts.

## License

MIT. Fork it, remix it, share it, build something better with it. Credit Pre and Darius Monsef if you use the handbook content.

## Credit

The Pre handbook and methodology are the work of Darius Monsef (founder, Pre / YC W10, S19, S24). The skill port and packaging were built as part of Pre's shutdown in 2026.

If this skill helps you build a real thing, that's enough. Darius doesn't need anything back. Go build.
