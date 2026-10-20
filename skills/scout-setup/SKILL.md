---
name: scout-setup
description: First-run and settings flow for the LinkedIn Opportunity Scout. Use when the owner says "set up the scout", "configure the LinkedIn scout", "change my rate stance", "update my availability", or when a find or draft request comes in and config/profile.md has no offer map yet.
---

# Scout Setup

Get the scout ready with the least effort from the owner. Reading the profile does most of the work; this skill covers what a profile cannot show.

## Steps
1. Read `config/profile.md`. If it has no offer map or says `Built from: not yet`, run the `profile-reader` skill first. Ask for the LinkedIn profile URL if it is not on file.
2. After the profile is read, check which settings are still unconfirmed or empty: engagement types, never-mention list, rate stance, availability line, link-in-comment switch, daily limits.
3. Ask only about the gaps, in one AskUserQuestion call of at most four questions. Offer concrete choices, for example rate stance: "never state a price in public" / "share by message" / "state a range when the post asks".
4. Write the answers into `config/profile.md`, keeping the owner's words.
5. Confirm in two or three plain sentences what the scout will look for and what it will never do, then offer to run `find-opportunities`.

## Notes
- Do not assume a profession, tool, or industry. Everything comes from the profile.
- Never fill a proof point from imagination. A blank is better than an invented claim.
- To change one setting later, edit only that line.
