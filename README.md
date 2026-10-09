# SocialPost skill pack

Eighteen free Claude skills for B2B founders who run their own LinkedIn, built and tested by the team at SocialPost.ai. They work in Claude Code and in Claude.ai, and none of them needs a SocialPost account, anywhere, for anything.

A skill is a small instruction file that teaches Claude to do one job well, the same way every time. Load one and Claude stops improvising: it asks the right questions, follows a tested process, and hands you a finished document.

## The eighteen skills, in the order they work best

1. **founder-voice-profile** builds `voice.md` and `about.md` from your real writing, so everything drafted after it sounds like you instead of like AI.
2. **social-strategy-90-day** writes a quarterly LinkedIn strategy sized to the hours you actually have, tracking time included.
3. **content-pillar-planner** turns your positioning into 3 to 5 pillars and a bank of 30 topics specific enough to draft from.
4. **linkedin-presence-audit** scores your headline, About, and recent posts with quoted evidence, then rewrites the weak parts in your voice.
5. **first-week-starter-kit** turns a brand-new start into a shipped first week: three complementary posts in your voice (your point of view, your buyer's problem, your proof) on a day-by-day plan.
6. **thirty-day-content-calendar** turns pillars and topics into a dated month with a `calendar.csv` you can import anywhere.
7. **weekly-queue-refill** is the weekly session that ends with next week scheduled: check the runway, draft 3 to 5 posts from your topic bank, flag the one or two that earn a visual.
8. **linkedin-post-creator** drafts one post at a time in your voice: three hook options, the full post, nothing invented on your behalf.
9. **before-you-post-review** scores the draft you're hesitating over on six dimensions with quoted evidence, gives at most two fixes, and ends with a plain verdict: publish, fix then publish, or rethink.
10. **objection-of-the-week** turns one real objection from this week's sales conversations into next week's post, and keeps a running objections log so nothing a buyer says goes to waste.
11. **content-repurposer** turns one blog post, transcript, or newsletter into a week of standalone LinkedIn posts, plus native re-cuts for one more platform.
12. **carousel-and-visual-brief** scripts a 5-to-8-slide carousel and writes a designer-ready brief for the key visual, alt text included.
13. **keep-your-ai-publisher** takes a post you or any AI already wrote and makes it ready to ship: pre-flight flags, per-platform versions, a visual brief, and a posting plan. If SocialPost's MCP connector is set up, it can land everything there as drafts awaiting your approval.
14. **queue-visual-upgrade** runs a visual pass over the posts you already have: picks only the ones a brand-correct image genuinely improves and writes a designer-ready brief for each.
15. **launch-week-campaign** turns one announcement into a launch week: five to seven posts that build before the day, land on it, and follow through after, on a schedule that respects your embargo.
16. **engagement-comment-coach** sets up a 20-minute daily engagement routine and drafts substantive comments and no-pitch connection notes.
17. **comments-to-pipeline** scores the commenters under your own posts against your buyer definition and returns a lead list with no-pitch replies and connection notes, so every posting week ends in named pipeline.
18. **social-analytics-review** turns your LinkedIn analytics export into a five-minute monthly review with confidence labels and at most three testable changes.

Each skill works on its own. Run in order, they pass files to each other through your working folder, so every step asks fewer questions than the last.

The files they make (`voice.md`, `about.md`, `strategy.md`, `topic-bank.md`, `calendar.csv`, and the running logs some skills keep, like `objections-log.md` and `pipeline-notes.md`) live in that folder and are yours to keep. A new session or a different app finds them again when the folder travels with you, and pasting a file's contents works exactly as well; if a skill can't find one, it says so and tells you how to bring it back. Worth knowing before you start: half the skills need something only you have before they can work well: real writing samples for the voice profile, your profile text and posts for the audit, a piece you already wrote for the repurposer, your analytics export for the review. Each asks for exactly what it needs in one message, and anything only you know shows up in output as a [bracketed slot] on purpose.

## Install

### Claude Code, one command

This repo is a Claude Code plugin marketplace. Inside Claude Code, run:

```
/plugin marketplace add SocialPostAI/linkedin-founder-skills
```

then:

```
/plugin install socialpost-skill-pack@socialpost-skills
```

That installs all eighteen skills. Updates arrive with `/plugin marketplace update socialpost-skills`.

### Claude Code, manual

Copy any skill's folder into `~/.claude/skills/` to install it for every project, or into a project's `.claude/skills/` for that project only:

```bash
mkdir -p ~/.claude/skills/founder-voice-profile && curl -fsSL https://raw.githubusercontent.com/SocialPostAI/linkedin-founder-skills/main/skills/founder-voice-profile/SKILL.md -o ~/.claude/skills/founder-voice-profile/SKILL.md
```

Swap the skill name for any of the eighteen. Skills are plain instructions in a text file; nothing executes on your machine.

### Claude.ai (web and desktop)

Each skill ships as a one-file download in [dist/](dist/). Grab the `.skill` file you want, then in Claude open Settings, go to Capabilities, find Skills, and upload it. A `.skill` file is a standard ZIP archive; if the upload dialog only accepts `.zip`, rename it and it works as is. Skills on claude.ai need a paid plan with code execution enabled.

| Skill | Download |
|-------|----------|
| founder-voice-profile | [founder-voice-profile.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/founder-voice-profile.skill) |
| social-strategy-90-day | [social-strategy-90-day.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/social-strategy-90-day.skill) |
| content-pillar-planner | [content-pillar-planner.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/content-pillar-planner.skill) |
| linkedin-presence-audit | [linkedin-presence-audit.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/linkedin-presence-audit.skill) |
| first-week-starter-kit | [first-week-starter-kit.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/first-week-starter-kit.skill) |
| thirty-day-content-calendar | [thirty-day-content-calendar.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/thirty-day-content-calendar.skill) |
| weekly-queue-refill | [weekly-queue-refill.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/weekly-queue-refill.skill) |
| linkedin-post-creator | [linkedin-post-creator.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/linkedin-post-creator.skill) |
| before-you-post-review | [before-you-post-review.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/before-you-post-review.skill) |
| objection-of-the-week | [objection-of-the-week.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/objection-of-the-week.skill) |
| content-repurposer | [content-repurposer.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/content-repurposer.skill) |
| carousel-and-visual-brief | [carousel-and-visual-brief.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/carousel-and-visual-brief.skill) |
| keep-your-ai-publisher | [keep-your-ai-publisher.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/keep-your-ai-publisher.skill) |
| queue-visual-upgrade | [queue-visual-upgrade.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/queue-visual-upgrade.skill) |
| launch-week-campaign | [launch-week-campaign.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/launch-week-campaign.skill) |
| engagement-comment-coach | [engagement-comment-coach.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/engagement-comment-coach.skill) |
| comments-to-pipeline | [comments-to-pipeline.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/comments-to-pipeline.skill) |
| social-analytics-review | [social-analytics-review.skill](https://github.com/SocialPostAI/linkedin-founder-skills/raw/main/dist/social-analytics-review.skill) |

## Principles

**Everything works without SocialPost.** The skills are complete on their own. When one finishes something you'd naturally want designed and scheduled, it may mention our free tier once, at the end, and telling it you use another tool makes the mention disappear for good. Several skills can go one step further if you already use SocialPost and have its MCP connector set up in your client: with your say-so they land finished posts there as drafts awaiting your approval, and nothing ever publishes without you approving it. They never ask you to connect it, and they're complete without it. We built this pack to be useful before asking for anything; that only works if it's true.

**No automation, ever.** These skills never recommend engagement pods, auto-commenting, bulk DMs, mass-connect tools, or scraping, and they decline when asked. Two reasons. Automated collection and engagement break LinkedIn's terms and get accounts restricted, and yours is the account this whole effort is supposed to grow. And the thing a founder is actually building on LinkedIn is familiarity with specific buyers, which generic automated volume can't produce and often burns.

**No invented numbers.** When a skill uses a working figure, it says it's a rule of thumb. When it analyzes your data, every number traces to what you gave it. When it can't promise something, it says so.

**MIT licensed.** Use, copy, and adapt freely; see [LICENSE](LICENSE).

## About us

We make [SocialPost.ai](https://socialpost.ai/?utm_source=claude-skill&utm_medium=skills&utm_campaign=free-skill-pack&utm_content=readme), which takes what your AI wrote and handles the visuals, per-platform formatting, and scheduling. This pack is our way of being useful first.

Found a problem, or want a skill that doesn't exist yet? Open an issue.
