# Alejo Acelas: work map and AI use, 28 September to 9 November 2026

Alejo Acelas's work in this period falls into five responsibilities. Ranked by active days, they are: AI-uplift community, content and call-capture tooling; own workspace and admin; AI-uplift client and mentoring work; the consulting client engagement; and the former employer bot handover. AI use is heaviest in workspace and admin, which has the most sessions and typed words, and lightest in the former employer bot handover, which was two sessions on a single day.

**Note.** This report covers the six weeks to 9 November 2026. I could open only Alejo's Claude Code and Claude desktop session history. I could not reach a calendar, email, Drive, Slack or meeting-notes source, so calendar hours are not available and the ranking uses active days, meaning distinct days with a typed AI message. Excerpts come from those sessions. Words typed exclude pasted text and skill or system text. Sessions launched by automation rather than typed by Alejo are not counted, and personal matters are left out. Dates are UTC, and a session that covered two responsibilities is counted in each.

| Responsibility | Calendar hours | Active days | AI sessions | Words typed |
|---|---|---|---|---|
| AI-uplift community, content and call-capture tooling | not available | 17 | 28 | 4,736 |
| Own workspace and admin | not available | 12 | 30 | 6,786 |
| AI-uplift client and mentoring work | not available | 7 | 13 | 2,489 |
| Consulting client engagement | not available | 6 | 10 | 1,934 |
| Former employer bot handover | not available | 1 | 2 | 1,428 |

All figures were counted by script over the session files.

## 1. AI-uplift community, content and call-capture tooling

Alejo takes part in an AI-adoption community Slack and plans its group call. They also build tools around it: bots, a Chrome extension and the `summarize-call` skill that files call transcripts. The evidence is the group call planning, two Slack bots and repeated `/summarize-call` runs.

**Worked example: planning the community group call (2026-11-01).** Alejo started by asking the assistant to mine the community's Slack channel for demand.

> **Alejo, 2026-11-01:** in the [community] slack, what concrete demonstrations do we have of demand signal for possible discussion areas? thinking of options for structuring a group call
>
Claude summarised which topics drew the most replies in the channel.

Alejo then asked what areas would suit the attendees' roles, and listed their own interests.

> **Alejo, 2026-11-01:** so far the topics that interest me most are:
> - how to foster repeated practice of AI uplift across staff, what does "good practice" look like?
> - what's the closest people have got to end-to-end automations? e.g,. things that run large processes with very little input from them
> - should we do anything with AI power users?
>
> **Assistant:** Here's how I'd frame each topic. Each one gets a short framing line and questions that pull out specific stories rather than general opinions.

In a second session that evening, the assistant proposed ten time slots for a scheduling poll and built it in Alejo's signed-in Chrome after they asked for "16 to 19, tuesday through monday, exlcuding the weekend" and 50-minute slots.

**How AI is used here**
- Filing call transcripts into tidied summaries with `/summarize-call`: 14 typed runs. At least 14 further sessions running the skill were started by automation, not typed.
- Planning the group call: reading the Slack channel, proposing topics, building a scheduling poll and a link roundup.
- Slack bots on the community workspace: a moderation bot and an anonymous-feedback bot.
- Drafting a set of short "AI trope" pages on using AI.
- Building a Chrome extension for comment threads on web pages, and a GitHub setup and public readings repository for sharing material.
- Editing Google Docs with a recurring `/loop` prompt (1 run), then turning it into a skill, plus finding an old doc by its argument.

**Corrections**
- Stopped a loop: “stop loop”.
- On the extension's remote setup: “I'm a little surprised that we'd need to run custom commands like the printf in additiona to tailscale.”
- On a set of test results: “2 should fail. other things ok and let's remove the google account from the agents frontmatter”.

**In my words**
- “good, one of core things I want to get right and we should invest effort on is on the title + opening quote combo.”
- Describing a belief behind the content: “the best way to get better at using ai is to use ai for projects”.

## 2. Own workspace and admin

Alejo maintains their own working setup: a folder system for work done for others (`desk/`), a server that records conversations and sends a daily digest, a `proj` shell command, and email and calendar triage. The evidence is a run of reorganisation sessions on 2026-10-31 and 2026-11-01.

**Worked example: redesigning `desk/` and the server pipeline (2026-10-31 to 2026-11-01).** The session began as a rename.

> **Alejo, 2026-10-31:** let's rename clients/ to uplift/ and move all the folders from projects/uplift to uplift/one-off except for a few that you select which I want to put in uplift/community which should contain [the community folders] inside it
>
> **Assistant:** I've renamed `clients/` to `uplift/` and split `projects/uplift/` into `uplift/community/` and `uplift/one-off/`. Both desk commits are pushed.

Over the next two hours Alejo cut instructions down and added a `sent/` folder. Then they restated the goal.

> **Alejo, 2026-10-31:** now that I think about it. here's what I want:
>
> I want to split work between generated by agents and not reviewed by me, triggered directly by my instruction and possibly reviewed in some form, and shared with others externally
>
> **Assistant:** I'd stop organising desk by person and make it a dated log. Each item is one file in one of three top-level folders, chosen by who started it: `generated/` (an agent on its own), `requested/` (you asked), and `comms/` (what was actually said or sent to people).

Alejo agreed to a fourth `sent/` folder and answered the assistant's five design questions with “record everything. on gmail skip the things that are obviously not about directly engaging with people (e.g, notices)”. Subagents then wrote a spec and migrated the files, and the pipeline went live that night. On 2026-11-01 Alejo asked: “let's rename the slack bot identity to clerk and the digest to docket”.

**How AI is used here**
- Reorganising folders and rewriting instruction files.
- Server automation: the docket and Slack bot, the email handler, permissions and a status check.
- Email and calendar triage, and Gmail labelling with a review page.
- Small tools and settings: the `proj` command, hooks, a Google Docs command-line tool, a clipboard recovery and a markdown editor for daily plans.

**Corrections**
- Rejected a review design: “let's remake the artifact. unit of review should not be each email.”
- Kept a rule the assistant planned to drop: “let's keep the desk agents.md instructions for now no to the lifecycle rule.”

**In my words**
- “I want zero redundancy or things that might get stale.”
- “I feel we have a lot of instructions that might get outdated as this folder evolves.”

## 3. AI-uplift client and mentoring work

Alejo offers AI-adoption coaching to organisations and individuals and designs engagements. The evidence is the engagement with a prospective client, a second prospect, coaching and mentoring calls, and a plan for engagements with organisations.

**Worked example: preparing for and debriefing the prospective client call (2026-10-28 to 2026-10-30).** Before a call with a contact at the prospective client, Alejo asked the assistant to read their email thread.

> **Alejo, 2026-10-28:** see my email exchanges with [the contact] from [the prospective client]. give me a sense of where they are in AI adoption and what they're looking for
>
> **Assistant:** [A summary of the email thread.]

The assistant drafted questions and tested them against *The Mom Test*, and Alejo asked for better wording and concrete asks.

After the call, Alejo asked for a review of the transcript with an eye to their own mistakes.

> **Alejo, 2026-10-30:** look at my call with [the contact]. open the gdoc on my browser and let's walk through the call to notice opportunities for improvement. let's start with the call opening. my read is I proposed a couple questions and [the contact] deflected to offer context on [their org]. what happened there?
>
Claude replied that the transcript did not support that reading.

Alejo then asked for a replay of the call with the fixes applied, and a comparison with a second prospect call.

**How AI is used here**
- Researching an organisation before a call: emails, public outputs and headcount, for the prospective client and a second prospect.
- Drafting and critiquing call questions.
- Reviewing recorded calls for mistakes and comparing two calls.
- Designing a mentoring-style engagement format, with research on how such engagements work.
- Summaries and short notes for coaching clients, an introductions list and an outreach draft.

**Corrections**
- On a set of questions: “hmmm, yeah. I guess, given that [they]'ve already expressed some pointers towards a need. what would be the wording of the questions you'd actually use?”
- On a proposed analysis: “1, as presented at least, doesn't sound particularly surprising.”
- On the snippets in a draft: “I'm not too fond of the snippets we have here.”

**In my words**
- “this is very useful.”
- “this is much better, but don't give role titles.”
- “I'm finding it hard to take seriously your "this is a good idea" judgement, maybe because off-the-cuff AI answers tend to be too agreeabel.”

## 4. Consulting client engagement

Alejo runs an AI-adoption assessment for a consulting client: 25-minute interviews with team members, a findings report and a coaching plan. The evidence is the interview calls, a project folder, and a capture sheet that holds one record per interview.

**Worked example: designing the capture fields from the interviews (2026-10-14 to 2026-10-15).** Alejo began with a spoken, rambling request, which the assistant restated before reading the transcripts.

> **Alejo, 2026-10-14:** Look through the last calls that I've had with [the consulting client's] employees, and and help me think of. So I'm trying to think of which structure fields or quotes or items we can extract from them. And so I guess one of some some of the fields are about kind of like how do they break down their time. Uh, kind of like what are what are the main tasks? Ideally, with like a concrete description we can get for each.
>
> **Assistant:** Here's what I understood.
>
> **Goal:** design an extraction schema for your [consulting client] calls. It should work on one person at a time and stay general enough to fit the calls you haven't done yet, which will mostly follow the format of the last two.

The assistant drafted a schema from five interviews, and Alejo picked from 33 candidate fields in a small web interface. They then asked for a final proposal, which listed 19 fields.

Alejo said a documented procedure was enough, and agents filled the sheet from each transcript. After the output came back, Alejo trimmed the rules.

> **Alejo, 2026-10-15:** no need to add the rule. it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations. some guidance for consistency is good, otherwise intent might sufice. not sure if there's other very specific rules incldue there
>
> **Assistant:** I've trimmed `capture-fields.md` from 157 to 135 lines, and committed and pushed it. Each field now says what it captures, and edge cases are left to judgement.

**How AI is used here**
- Designing the extraction fields from interview transcripts and filling one record per interview, with parallel agents (nine records by 2026-10-15).
- Setting up Fathom to join the client's calls (3 requests).
- Opening call transcripts, working out the Slack setup for the client's workspace, finding the capture sheet, and pulling out assessment themes.
- Reviewing the prompt of a service built for the client.

**Corrections**
- Dropped a proposed script: “not sure we need a deterministic script. just documenting steps might be good enough (it fails more gracefully to changes).”
- Removed an edge-case rule: “no need to add the rule.”
- Redid fields: “thanks, and let's redo role team and tenure to be straightforward (no clarification of source, just the value, in standard format eg. '3 months')”.

**In my words**
- “it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations.”
- “I don't want to kind of delegate this judgment to AI.”

## 5. Former employer bot handover

Alejo was handing a bot they had built for a former employer to a colleague. The evidence is a Slack request and the bot's setup notes.

**Worked example: debugging the bot before the handover (2026-10-15).** Alejo pasted the colleague's handover request into a session. The bot was not working. The assistant offered a cause, and Alejo asked whether it had checked.

> **Alejo, 2026-10-15:** did you check on the [admin panel] whether the [setting] is attached to the [channel]? feel free to have a headless codex check and inform you
>
> **Assistant:** You're right: I didn't verify that. It was a guess, and the [admin panel] contradicts it.

Alejo changed the setting, and the assistant ran tests. A subagent then reworked the bot's scripts, which Alejo had it test the same afternoon.

**How AI is used here**
- Diagnosing the failure and running about a dozen test threads.
- Reworking the bot's scripts, with a subagent.
- Writing the repository and setup notes for the handover.

**Corrections**
- Questioned the assistant's diagnosis: “did you check on the [admin panel] whether the [setting] is attached to the [channel]?”
- Asked for the reasoning behind a setting: “what's your account of why we still need [that setting]?” The assistant then wrote: “I was wrong to blame [that setting], and the setup doc I wrote overstates the case.” Its own handover advice had caused part of the problem.

**In my words**
- None stated.
