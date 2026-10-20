# LinkedIn Opportunity Scout

Reads **your own** LinkedIn profile, finds recent posts where someone needs what you offer, scores the fit, drafts a short friendly proposal as a comment, and posts it only after you approve that exact comment. It works for any profession because everything is built from your profile, not from a fixed skill list.

## The flow

1. **Learn you**: `profile-reader` reads your profile (or resume) and builds your offer map, search phrases, tone notes and eligibility.
2. **Find**: searches recent LinkedIn posts using phrases built from your offer map, in read-only mode.
3. **Filter and score**: drops scams, unpaid work, stale posts and posts you cannot take, then scores fit from 0 to 100.
4. **Draft**: writes a short proposal comment (40 to 80 words) in your voice, two options per post.
5. **Approve and post**: you pick, edit or skip. After your explicit yes, one comment is posted from your account, then logged.
6. **Follow up**: drafts replies and nudges, and a weekly review improves searches and drafts.

## Skills

| Skill | What it does |
|---|---|
| `profile-reader` | Reads your profile and builds the offer map, search phrases, tone and eligibility |
| `scout-setup` | First run and settings: goals, never-mention list, rate stance, availability |
| `find-opportunities` | Daily search, red-flag filter, fit scoring, ranked shortlist |
| `draft-proposal` | Short, human-sounding proposal comments, two options each |
| `approve-and-post` | Posts only approved comments, with limits and spacing, then logs them |
| `pipeline-tracker` | Log, follow-up drafts, weekly review |

## Safety rules built in

- Nothing is posted or sent without your approval of that specific comment in chat.
- Scheduled runs may only find and draft. No bulk auto-posting.
- Daily cap of 8 comments, at least 10 minutes apart.
- No passwords, CAPTCHAs or account creation.
- Never invents experience, clients, rates or availability. Skills with no evidence on your profile are never offered.
- Positive and friendly tone only.

## First run

Say "read my profile" (give your LinkedIn URL if asked), answer the few questions, then say "find opportunities".
