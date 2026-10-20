---
name: profile-reader
description: Reads the owner's own LinkedIn profile (or resume) and builds a personal offer map, search phrases, tone notes and eligibility details from it, so the scout works for any profession, not one fixed skill set. Use when the owner says "read my profile", "learn my profile", "build my profile from LinkedIn", "refresh my profile", "I changed my headline", or on first run when config/profile.md has no offer map yet.
---

# Profile Reader

Turn the owner's real profile into the inputs every other skill depends on. Nothing in this plugin assumes a profession. What the owner offers, what to search for, and how to sound all come from this skill's output.

## Whose profile
Read only the owner's own profile. Ask for the profile URL if `config/profile.md` has none. If a different person starts using the plugin, treat it as a new owner: start a fresh `config/profile.md` and `tracking/pipeline.md` instead of mixing records. Never read other people's private data, private messages, or connection lists.

## Sources (use the best available, combine if useful)
1. **Signed-in browser, read-only.** Read the skill for the browser in use, open the owner's profile, and read page text. Collect: name, headline, location, About, current and past roles with their descriptions, Skills (and endorsements counts if visible), Featured items, certifications, education, languages, recent activity or posts, and any "Open to" settings that are visible to the owner. Click only to expand "see more" sections. Do not click Connect, Follow, Message, Edit, or anything that changes the account. If a login wall or security check appears, stop and ask the owner to sign in; never enter credentials.
2. **Attached resume or CV.** Read it with the matching file skill.
3. **Public page fetch.** Try the public profile URL; LinkedIn often blocks it, so expect partial results.
4. **Owner paste.** Ask the owner to paste the About and Experience text.

Say which sources were used and what could not be read.

## Extract
Follow `references/profile-extraction.md`. In short, build:
- **Offer map**: each service or capability the owner can credibly offer, with an evidence level (`strong` = backed by a role, project, or result in the profile; `light` = listed skill with no supporting detail; `none` = not on the profile, never offered)
- **Proof points**: facts stated in the profile that are safe to quote, each with where it came from
- **Target demand phrases**: how a person who needs this work would actually write the post
- **Engagement fit**: contract, freelance, part-time, full-time, consulting, mentoring, speaking, partnerships (from profile signals; confirm with owner)
- **Eligibility**: location, time zone, languages, work-authorisation hints
- **Tone**: sentence length, formality, humour, typical openers, from About and posts
- **Gaps and weak spots**: anything the profile claims vaguely, which the scout will not lean on

## Confirm with the owner
A profile cannot reveal everything. Show a short plain-language summary of what you understood (what they offer, who they help, where they are, how they sound) and use AskUserQuestion, up to four questions, for what is still unknown. Prioritise:
- What they most want to be found for right now (pick from the offer map)
- Engagement types wanted and not wanted
- Anything that must never be mentioned publicly (for example a current employer or a confidential client)
- Rate stance and availability line

Skip questions the profile already answered.

## Write
Save everything to `config/profile.md` and the search terms to `config/search-rules.md` using the existing section headings. Record the source and date at the top (`Built from: <sources> on <date>`). Mark items the owner has not confirmed as `unconfirmed`. Do not embellish, upgrade `light` evidence to `strong`, or invent proof points.

## Refresh
Re-run when the owner changes their profile or headline, starts a new role, or every 30 days. Show a short diff (new skills, removed services, changed goals) and apply it only after the owner agrees.
