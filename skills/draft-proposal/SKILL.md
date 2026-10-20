---
name: draft-proposal
description: Writes a short, friendly, human-sounding proposal comment for a LinkedIn post where someone needs what the owner offers (as read from their own profile), in the owner's voice, with two options per post. Use when the owner says "draft a proposal", "write a comment for this post", "reply to this requirement", "offer my services on this post", or picks posts from a shortlist.
---

# Draft Proposal

Write a comment a real person would write, short enough to read in five seconds and specific enough that the poster replies.

## Inputs
- A post (URL or pasted text) from the shortlist or from the owner
- `config/profile.md` (offer map with evidence levels, proof points, availability, rate stance, do-not-mention list, voice notes). If it has no offer map yet, run `profile-reader` first.
- `references/proposal-examples.md` for register only; never copy lines

## Process
1. Read the post. Pull out: what they need, one concrete detail (stack, goal, deadline, pain), and the poster's tone.
2. Check honest fit. Compare the need with the offer map: lead only with `strong` capabilities, mention `light` ones briefly if at all, never offer `none`. If the owner covers only part, plan to say exactly which part. If it is not a fit, say so and skip.
3. Draft two options, each a different angle:
   - **A, direct offer**: one line showing you understood their need, one line of relevant experience, one clear next step
   - **B, question-led**: a sharp clarifying question that shows expertise, then a light offer
4. Check each draft against the quality bar in `AGENTS.md`: 40 to 80 words, specific detail from the post, no banned phrases, no em dashes, no hashtags, no bullet lists, no price unless config allows, no link unless `allow_link_in_comment` is true, nothing from the do-not-mention list.
5. Fact check: every claim must come from `config/profile.md` (built from the owner's profile) or the owner's chat. Use proof points only if marked safe to say publicly. If a draft needs a fact you lack, replace it with a placeholder like [one real project] and tell the owner, or use the question angle.
6. Add a DM follow-up line (1 or 2 sentences) the owner can send if the poster replies or if comments are closed. Mark it as draft only.

## Output format
For each post:
- Poster, company, and one-line summary of the need
- Fit note: full, partial (what is covered), or skip with reason
- **Option A** (with word count)
- **Option B** (with word count)
- Recommended pick and why, in one line
- Suggested DM follow-up
- Best time to post (as soon as approved is best for fresh posts)

## Approval
Present the drafts and stop. Update the pipeline log entry to `drafted`. Do not post. Hand off to `approve-and-post` once the owner names the exact option and any edits.

## Tone
Warm, plain, confident without bragging, never negative. Never compare the owner to other applicants or criticise the poster's current setup.
