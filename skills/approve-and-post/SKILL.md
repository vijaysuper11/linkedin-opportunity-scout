---
name: approve-and-post
description: Posts an owner-approved proposal comment on a specific LinkedIn post through the owner's signed-in browser, one comment at a time, then logs it. Use when the owner says "post this comment", "go with option A", "approved, post it", "send that proposal on LinkedIn", or confirms a specific draft for a specific post.
---

# Approve and Post

This skill is the only place a comment is ever posted. It runs only after the owner approves one exact comment for one exact post in the current chat.

## Preconditions (check all, otherwise stop and say what is missing)
1. The owner's message names the post (or it is unambiguous from the shortlist) and the exact comment text, including any edits. A bare "yes" or "looks good" to a batch is not enough; confirm which option for which post.
2. Today's posted count in `tracking/pipeline.md` is below `max_comments_per_day` (default 8).
3. At least `min_minutes_between_posts` (default 10) have passed since the last comment posted today. If not, tell the owner when the next slot opens and offer to post then, with a fresh confirmation.
4. The post is still live and still looks legitimate. Re-open it and re-check red flags (poster still hiring, not filled, no new warnings in comments).
5. The comment text still passes the `AGENTS.md` quality bar and contains nothing from the do-not-mention list.

## Posting
1. Read the skill for whichever browser is being used (the owner's preferred browser first) before the first step.
2. Open the post URL. If a login wall, CAPTCHA, or security prompt appears, stop and ask the owner to handle it. Never enter credentials.
3. Show the owner a final one-line confirmation of what is about to be posted (post, comment text) if the text was edited after the last approval.
4. Click the comment box, type the approved text exactly, and submit. Do not change wording, add hashtags, tag people, or attach links unless the approved text includes them.
5. Verify the comment appears under the owner's name on the post. If it does not, report that plainly and do not retry more than once.

## After posting
- Update `tracking/pipeline.md`: status `posted`, time, final comment text, follow-up due in 3 days.
- Tell the owner in one or two sentences that it is posted, and when to expect replies.
- Offer the DM follow-up draft only if the poster has engaged or comments are limited. Sending a DM needs its own separate approval.

## Never
- Post a second comment without a new approval
- Post to several posts in one go
- React, connect, follow, or message as a side effect
- Edit or delete an already posted comment unless the owner asks
