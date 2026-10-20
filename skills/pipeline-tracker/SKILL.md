---
name: pipeline-tracker
description: Tracks every LinkedIn opportunity from found to won or lost, drafts replies and follow-ups when someone responds, and runs a weekly review of what is converting. Use when the owner says "pipeline", "any replies", "follow up", "what happened with my proposals", "weekly review", "what is working", or "update the tracker".
---

# Pipeline Tracker

Keep the funnel honest and turn results into better searches and better drafts.

## Files
- `tracking/pipeline.md` is the source of truth. Statuses: found, drafted, approved, posted, replied, in-conversation, won, lost, skipped.

## Daily check (when asked)
1. Read the log. List items posted in the last 7 days.
2. If a browser tool is available and the owner asked, open each posted item read-only and note new replies, likes, or profile views from the poster. Do not click anything that acts on the owner's account.
3. For each reply, draft a short, friendly answer (under 60 words) that moves toward a call or a scope message. Show it and stop for approval; posting goes through `approve-and-post`.
4. For posts quiet for 3 days, suggest one soft follow-up (a useful tip, or a question) at most once. After that, mark as `lost` unless the owner says otherwise.

## Weekly review
1. Compute: posts found, drafted, posted, replies, conversations, wins; reply rate and conversation rate.
2. Compare by: score band, freshness at time of comment (under 2 hours vs later), option A vs B, poster type (founder vs recruiter), query that found it.
3. Report in plain language: what to do more of, what to stop, one change to try next week. Keep it to a short list the owner can act on.
4. Propose edits, but apply them only after the owner agrees:
   - New or removed search phrases in `config/search-rules.md`
   - Extra banned phrases in `AGENTS.md` if any draft felt stiff
   - New proof points the owner may want to add to `config/profile.md`
5. Note any soft or hard red flags that slipped through so `red-flags.md` can be updated.

## Reporting style
Lead with the result. Show numbers only when they change a decision. Do not pad.
