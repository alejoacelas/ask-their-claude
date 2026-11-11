# Work map: Alejo Acelas, 28 Sep to 8 Nov 2026

Over the six weeks to 8 November 2026, the record I could read shows Alejo Acelas working in five areas. Ranked by active days (the calendar was not readable) they are: Personal agent server and workspace tooling; Independent AI-uplift consulting and coaching; Consulting client AI-adoption assessment, which ties on days with the AI-adoption community Slack and ranks above it on sessions; AI-adoption community Slack; and the former-employer handover. AI use is heaviest in the tooling area (43 sessions, 6,993 typed words), where Claude does much of the building, and lightest in the former-employer handover (2 sessions, 436 words), which was one debugging session. The consulting client assessment also ran through 10 sessions started by automation with no typed prose.

**Note.** This covers 28 Sep to 8 Nov 2026. The only source I could read was Claude Code session history on this machine (typed messages run from 9 Oct to 4 Nov, UTC dates); I could not see calendar, email, Drive documents, Slack, meeting notes or ChatGPT history, so hours are not available and ranking is by active days, then AI sessions. Rule: each session goes to one responsibility by the subject of its opening request (client, organisation or system), and sessions that drifted keep their opening one. Active days are days with a typed message; words exclude pasted text and automated prompts; personal-life sessions and automated health-check pings are left out.

## Overview

| Responsibility | Calendar hours | Active days | AI sessions (typed) | Words typed | Sessions with no typed prose |
|---|---|---|---|---|---|
| Personal agent server and workspace tooling | not available | 17 | 43 | 6,993 | 4 |
| Independent AI-uplift consulting and coaching | not available | 7 | 15 | 2,359 | 4 |
| Consulting client AI-adoption assessment | not available | 6 | 11 | 2,202 | 10 |
| AI-adoption community Slack | not available | 6 | 8 | 1,923 | 0 |
| Former-employer handover | not available | 2 | 2 | 436 | 0 |

## 1. Personal agent server and workspace tooling

Alejo builds and runs the systems behind their other work: an agent server, scheduled email jobs, a Slack assistant, a `proj` shell command and the folder layout that holds client work. The evidence is sessions in their `inbox`, `desk` and `projects` folders and the server services they named "clerk" and "docket".

**Worked example: sorting email and producing a digest (24 Oct to 1 Nov 2026).** It began as a question about Gmail labels and ended inside the server's task assistant. Alejo set the brief and Claude drafted a label scheme from their mail history:

> **Alejo, 24 Oct:** nice, now look at my email history and let's design a schema to classify emails into folders. some important folders are: calls (a frequent thing, not sure if having the call email adds anything over the calendar entry, but still) and receipts and deliveries, and personal communication (e.g., emails from actual people addressed to me)

> **Claude, 24 Oct:** I read 200 threads from Aug 8 to Oct 24 (about 18 a week, not counting threads you only sent). They sort into five labels plus a delete pile. Your inbox stays the place for things that need you. Every kept email also gets one label, and the label stays on after you archive, so each label works as a list you can scroll by date.

Claude then built a review page; Alejo rejected its unit of review and asked to host it on the server. Over the next week the digest was adjusted in short instructions until it was absorbed into the server's task assistant:

> **Alejo, 24 Oct:** thanks! I'd like to make the digest now be updated daily and have 'space' for adding the requests (which enter does now) and enter for 'this is done, don't show it again'

> **Alejo, 31 Oct:** 3. yeah, let's have this thing eat the email digest.

> **Alejo, 1 Nov:** let's rename the slack bot identity to clerk and the digest to docket

**How AI is used here:**

- Building and deploying server services such as the email sorter, digest and bot hosting; 12 of the sessions had subagent results reported back.
- Reorganising the workspace folders and agent instruction files (two long sessions, 31 Oct and 1 Nov).
- Small tools: a daily-plan markdown editor, a reading app, a Chrome extension and the `proj` command.

**Corrections:**

- On the digest page: "let's remake the artifact. unit of review should not be each email." (24 Oct)
- On the file-filing instructions Claude drafted: "it's more a way of organizing substantial pieces of work." (31 Oct)

**In my words:**

- "I feel we have a lot of instructions that might get outdated as this folder evolves." (31 Oct)
- "this is great tahnks" (24 Oct)

## 2. Independent AI-uplift consulting and coaching

Alejo coaches and consults on AI use for organisations and individuals. The evidence is a run of prospective-client calls and email threads (a prospective client and another prospect) and documents prepared after calls.

**Worked example: preparing for and reviewing the prospective client's discovery call (28 to 30 Oct 2026).** Alejo started from the email record:

> **Alejo, 28 Oct:** see my email exchanges with [the contact]. give me a sense of where they are in AI adoption and what they're looking for

Claude summarised the email threads, then drafted questions for the 30-minute call, tested them against "mom-test style advice" at Alejo's request, and suggested asks for the end. Two days after the call, Alejo asked for a walk-through of the transcript:

> **Alejo, 30 Oct:** look at my call with [the contact]. open the gdoc on my browser and let's walk through the call to notice opportunities for improvement. let's start with the call opening. my read is I proposed a couple questions and [they] deflected to offer context on [their org]. what happened there?

Claude replied that the transcript did not support that reading, and pointed to the setup instead:

> **Claude, 30 Oct:** 1. **There was no frame.** You went from "how about you guys?" straight to the question, with no introductions and no agenda or time check.

Alejo then asked for a replay with the fixes applied, and a comparison with a second prospect's call.

**How AI is used here:**

- Preparing for calls from email threads, and reviewing call transcripts afterwards (28 and 30 Oct).
- Filing call summaries: `/summarize-call` typed 5 times, plus 4 headless runs started by automation.
- Producing documents after calls: an introductions list and an audit-call highlights doc (29 to 31 Oct).
- Thinking through engagement design and researching prospective clients (26 to 30 Oct).

**Corrections:**

- On proposed highlights: "1, as presented at least, doesn't sound particularly surprising." (29 Oct) and "I'm not too fond of the snippets we have here." (29 Oct)
- On a strategy answer: "this answer feels vague." (26 Oct)

**In my words:**

- "I'm finding it hard to take seriously your "this is a good idea" judgement, maybe because off-the-cuff AI answers tend to be too agreeabel." (26 Oct)
- "this is very useful." (30 Oct)

## 3. Consulting client AI-adoption assessment

Alejo ran an AI-adoption assessment for a consulting client in October: a 25-minute interview with each team member about how they use AI, then a findings report and coaching plan for the client. The evidence is a project folder, a run of interview calls from 13 Oct, and a capture sheet of fields extracted from the transcripts.

**Worked example: deciding what to extract from the interviews (14 to 15 Oct 2026).** It ran through one long session. Alejo opened by dictating what they wanted:

> **Alejo, 14 Oct:** Look through the last calls that I've had with [the consulting client's] employees, and and help me think of. So I'm trying to think of which structure fields or quotes or items we can extract from them. And so I guess one of some some of the fields are about kind of like how do they break down their time. Uh, kind of like what are what are the main tasks?

Claude read the transcripts, drafted a schema and built a sheet; Alejo asked for a throwaway picker to keep or drop fields, then left comments. On 15 Oct Claude proposed final fields and Alejo answered:

> **Claude, 15 Oct:** I've written the proposal to `capture-fields.md` in the project and committed and pushed it. It proposes 19 fields, a redefined adoption scale for us to agree on, and a script that fills the sheet from any new transcript.

> **Alejo, 15 Oct:** not sure we need a deterministic script. just documenting steps might be good enough (it fails more gracefully to changes). no need to call apis. and I say yes to your proposed fields including the adoption scale

Later that day Alejo asked Claude to check two new field definitions against the full transcripts. Claude replied that "the checking definition is too broad", and three subagents then refilled both fields.

**How AI is used here:**

- Drafting and revising the extraction schema and field definitions from transcripts (14 to 15 Oct), and building a field picker and capture sheet.
- Running subagents to fill fields person by person (7 agents, then 3 for a re-fill).
- Filing interview summaries: `/summarize-call` typed 4 times, plus 9 headless runs started by automation between 15 and 22 Oct.
- Admin for the interviews (13 to 14 Oct).

**Corrections:**

- Dropped a proposed script: "not sure we need a deterministic script." (15 Oct)
- Redid field formats: "let's redo role team and tenure to be straightforward (no clarification of source, just the value, in standard format eg. '3 months')" (15 Oct)
- Questioned a detail in an answer: "where did you get this detail?" (14 Oct)

**In my words:**

- "just documenting steps might be good enough (it fails more gracefully to changes)." (15 Oct)
- "it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations." (15 Oct)

## 4. AI-adoption community Slack

Alejo runs channels in an AI-adoption community Slack workspace for people who do AI-adoption work. The evidence is bots built for it (moderation and anonymous feedback), planning for a community group call, a readings repository, and a set of pages on lessons for using AI.

**Worked example: a moderation bot for a community channel (27 to 31 Oct 2026).** Alejo asked for the bot and a test plan:

> **Alejo, 27 Oct:** use the slack credentials for [the community Slack] we had gotten to make the slack clis and use them to make a bot with a separate identiy call it 'Moderation Bot' or similar, that is triggered whenever a new top-level message appears on a channel. I plan to use it to reply to messages that don't pass a moderation bar asking their users to delete them (see recent example in [a community channel])

Claude created the Slack app, ran its classifier over the channel's history, and tested it in a private channel; Alejo reviewed the results and set the reply wording. The bot was left off. Four days later a template post appeared in the channel:

> **Alejo, 31 Oct:** i remember having setup a moderation bot on the server for these kinds of posts. why did it not trigger here?

> **Claude, 31 Oct:** The bot never saw this post. It was never switched on for [the community channel], and it isn't running anywhere.
>
> 1. **The channel is set to `off`.** In [the bot's channel config], [the community channel] has `mode = "off"`. On Oct 27 you only set it to `live` in [a private test channel]. The project's notes say a main channel goes `live` only once you approve it.

Alejo had it set live and hosted on the server, then tightened the rule to flag any template message, and asked for an anonymous feedback bot as a follow-on.

**How AI is used here:**

- Building and deploying Slack bots (moderation, 27 and 31 Oct; anonymous feedback, 31 Oct).
- Mining Slack history for demand signals and a resource roundup, and setting up a scheduling poll, for the group call (1 Nov, two sessions).
- Drafting short lesson pages on using AI (29 Oct) and publishing a readings repository (2 Nov).

**Corrections:**

- On the bot's message: "remove this:  and Alejo will take a look." (31 Oct)
- On its public intro: "shorter" (31 Oct) and "no continue with what you were doing" (31 Oct)
- On the lesson pages: "still, ocassionally the lesson/recommendation/narrative for how to deal with the pattern is not quite what I'd recommend, and often hides the complexity behind the thing." (29 Oct)

**In my words:**

- "many of the titles are great, and very relevant." (29 Oct)
- "the classification looks correct" (27 Oct)

## 5. Former-employer handover

Alejo had handed Claude automations he built for a former employer to a colleague. The evidence is the colleague's request for a handover, the handover docs Alejo sent, and the Slack threads where a bot from the handover was failing.

**Worked example: debugging a handed-over bot (15 Oct 2026).** Alejo pasted the colleague's messages into a session and asked Claude to find the cause. Claude's first diagnosis was a guess about a setting; Alejo checked it:

> **Alejo, 15 Oct:** did you check on the admin panel whether [the setting] is attached to the channel? feel free to have a headless codex check and inform you

Claude conceded it had not verified the claim and that the admin panel contradicted it. Alejo then changed a setting so Claude could test:

> **Alejo, 15 Oct:** I changed [the setting], try the channel for an edit and see what happens. do tests that might isolate the situation

The tests fixed part of the problem. Claude then found that its own handover advice had caused the rest:

> **Claude, 15 Oct:** Two of the three problems are fixed. The third is a missing capability, not a settings problem, and my handover advice caused it.

**How AI is used here:**

- Diagnosing the bot from the Slack threads, posting test threads and reading the bot's answers (one long session, 15 Oct).
- Auditing which capabilities the bots relied on, and having a subagent port and test the scripts (15 Oct).

**Corrections:**

- Challenged an unverified claim: "did you check on the admin panel whether [the setting] is attached to the channel?" (15 Oct)

**In my words:** none stated.
