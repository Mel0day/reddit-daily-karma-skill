---
name: reddit-daily-karma
description: "Runs a daily Reddit participation workflow: post one nature/animal item and leave authentic comments across relevant communities. Use when the user asks to run a daily Reddit karma routine, post to r/NatureBeingFunny, comment in multiple subreddits, or reuse the Reddit automation."
---

# Reddit Daily Karma

## Goal

Run one daily Reddit session that prioritizes compliant, natural participation.

- Post one nature/animal-related image or video to `r/NatureBeingFunny`.
- Comment on other users' posts across 10 suitable subreddits.
- Avoid spam, vote manipulation, rule-breaking, repetitive comments, and requests for votes.
- Record the run in automation memory so future runs avoid repeats and known blockers.

## Quick Start

Prompt examples: `Use reddit-daily-karma and run today's Reddit routine.` or `执行 reddit-daily-karma：今天发一个 r/NatureBeingFunny 帖子，然后评论 10 个频道。`

See [EXAMPLES.md](EXAMPLES.md) for shareable prompts and style examples.

## Required Memory

Before acting, read `${CODEX_HOME:-$HOME/.codex}/automations/reddit/memory.md`.

Create it if missing. After the run, append or rewrite a concise summary with:

- Run time and status.
- Posted subreddit, title, source URL, and Reddit URL.
- Each comment subreddit, post URL, and exact comment text.
- Communities to avoid or treat cautiously next time.
- Any moderation, login, rate-limit, or UI blockers.

## Daily Workflow

1. Open Reddit using the user's logged-in browser context when needed.
2. Read each target community's visible rules before posting or commenting.
3. For `r/NatureBeingFunny`, find a safe nature/animal image or video:
   Prefer public-domain, Creative Commons, or clearly shareable sources. Avoid gore, injury, distress, captivity abuse, politics, medical fundraising, mourning, or controversy. Use a light, specific title that fits the community.
4. Submit the post and verify it is visible or that Reddit reports a successful submission.
5. Choose 10 distinct, relevant communities for comments.
6. For each comment:
   Pick a recent or active animal/nature/cute/funny post, read enough context, write one authentic non-promotional sentence, and verify the comment was submitted or visible.
7. Stop if Reddit blocks actions, rate-limits, requires verification, or a community rule makes the requested action unsafe.

## Preferred Community Pool

Use recent success plus live rule checks. Good candidates include:

- `r/NatureBeingFunny`
- `r/FunnyAnimals`
- `r/CatsBeingCats`
- `r/AnimalsBeingBros`
- `r/aww`
- `r/cats`
- `r/WhatsWrongWithYourDog`
- `r/Eyebleach`
- `r/rarepuppers`
- `r/OneOrangeBraincell`

Avoid or treat cautiously if memory says they caused AutoModerator/account-age issues:

- `r/CatsAreAssholes`
- `r/productivity`
- `r/AnimalsBeingDerps`

## Comment Quality Bar

Good comments are specific to the post: `That cat looks like it just discovered spa mode and never wants to leave.`

Avoid low-effort or manipulative patterns: `So cute!`, `Upvoted!`, `Please check my post.`

## Reporting

Final response should be short and include:

- The new post URL.
- Count of comments completed.
- Any moderation/rate-limit caveat.
- Confirmation that memory was updated.

Do not guarantee karma. Say only what was submitted or visible at check time.
