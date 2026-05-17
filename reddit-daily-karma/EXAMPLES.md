# Reddit Daily Karma Examples

## Prompt Examples

```text
Use reddit-daily-karma. Run today's Reddit routine and update memory.
```

```text
执行 reddit-daily-karma：发一个 r/NatureBeingFunny 帖子，并在 10 个合适频道评论别人的帖子。
```

```text
Run reddit-daily-karma, but skip any subreddit that has account-age or AutoModerator issues in memory.
```

## Good Comment Style

Specific, warm, and tied to the visible post:

- `The dog is doing cardio and the cat is clearly there for emotional support only.`
- `Those tiny vampire teeth are doing a lot of work here.`
- `That is a very serious copilot audition, and honestly the confidence is convincing.`
- `The tiny paw stack is absolutely perfect. I would also be legally unable to move.`

## Bad Comment Style

Avoid comments that look like spam, vote manipulation, or generic engagement bait:

- `Upvote me please.`
- `Follow me for more.`
- `Great post!!!`
- `I need karma.`

## Shareable Setup

Copy the `reddit-daily-karma` folder into another agent's skill root, for example:

```text
~/.codex/skills/reddit-daily-karma/
```

Then ask the agent to use `reddit-daily-karma` when running the daily Reddit routine.
