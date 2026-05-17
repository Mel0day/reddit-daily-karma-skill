# Reddit Daily Karma Skill

A reusable Codex skill for running a daily, rule-aware Reddit participation routine.

The skill is designed for a logged-in human-owned Reddit account. It helps an agent:

- post one nature or animal item to `r/NatureBeingFunny`;
- leave authentic comments across 10 suitable subreddits;
- read community rules before acting;
- avoid spam, vote manipulation, repeated comments, and known AutoModerator traps;
- update a local memory file after every run.

It does **not** guarantee karma, bypass moderation, coordinate votes, or automate spam.

## Install

Copy the skill folder into your Codex skill root:

```bash
mkdir -p ~/.codex/skills
cp -R reddit-daily-karma ~/.codex/skills/
```

The installed layout should look like this:

```text
~/.codex/skills/reddit-daily-karma/
├── SKILL.md
└── EXAMPLES.md
```

Restart or reload your Codex session if your environment only discovers skills at startup.

## Use

Ask Codex to invoke the skill:

```text
Use reddit-daily-karma and run today's Reddit routine.
```

Chinese prompt:

```text
执行 reddit-daily-karma：今天发一个 r/NatureBeingFunny 帖子，然后评论 10 个频道。
```

The skill expects the agent to use your already logged-in Reddit browser session when needed.

## Daily Workflow

Each run follows this pattern:

1. Read the automation memory.
2. Pick a safe nature or animal image/video for `r/NatureBeingFunny`.
3. Check visible subreddit rules before posting.
4. Submit the post and verify it is visible or accepted.
5. Find 10 suitable recent posts in relevant communities.
6. Write one specific, non-promotional comment per community.
7. Verify each comment was submitted or visible.
8. Update the memory file with links, comment text, and blockers.

## Memory

The skill uses this local memory path:

```text
${CODEX_HOME:-$HOME/.codex}/automations/reddit/memory.md
```

This memory prevents the agent from repeating recent work and records:

- posts already submitted;
- comment targets and exact comment text;
- communities that caused AutoModerator or account-age issues;
- rate-limit, login, verification, or moderation blockers.

## Recommended Guardrails

Use the skill as an assistant for authentic participation, not as a spam bot.

- Do not ask for upvotes.
- Do not mention karma farming in comments.
- Do not copy/paste the same comment across posts.
- Do not post distressing, political, medical, fundraising, or abuse-adjacent content.
- Stop when Reddit rate-limits, blocks, or requires verification.
- Respect each community's rules even if the high-level routine asks for 10 comments.

## Known Cautious Communities

The initial memory from the source workflow marks these as cautious or avoid:

- `r/CatsAreAssholes`
- `r/productivity`
- `r/AnimalsBeingDerps`

The skill still requires live rule checks because subreddit rules and account restrictions can change.

## Files

- [`reddit-daily-karma/SKILL.md`](reddit-daily-karma/SKILL.md): the actual skill loaded by Codex.
- [`reddit-daily-karma/EXAMPLES.md`](reddit-daily-karma/EXAMPLES.md): prompt and comment style examples.

## License

MIT. See [`LICENSE`](LICENSE).
