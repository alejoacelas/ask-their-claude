# Alejo's work over the last six weeks, and where AI fits

Over the six weeks to 9 November 2026, Alejo's work falls into four responsibilities. Ranked by active days, they are: the agent workspace and tooling (14 days), AI-uplift coaching and client calls (12), a consulting client's AI-adoption assessment (9) and the AI-uplift community (4). The record shows AI use in all four. It is heaviest in the workspace and tooling, at 27 sessions and 4,941 typed words, and lightest in the community work, at 5 sessions and 1,792 words. The community sessions are the longest per session, though. In every area Alejo gives the assistant a goal and then corrects its output, rather than accepting a first draft.

**Note.** This report covers 28 September to 9 November, but the AI history I could read only starts on 4 October and mostly runs from 9 October to 5 November. I could not reach a calendar, email, documents, Slack or meeting notes, so there are no calendar hours. The ranking uses active days, and an active day here is a day with at least one message Alejo typed to an assistant (dates are UTC). Words typed exclude pasted text, continued-session summaries and prompts written by an assistant. I left out personal matters, test sessions and a few sessions I could not attribute.

## Overview

| Responsibility | Calendar hours | Active days | AI sessions | Words typed |
|---|---|---|---|---|
| Agent workspace and tooling | not available | 14 | 27 | 4,941 |
| AI-uplift coaching and client calls | not available | 12 | 22 | 3,115 |
| Consulting-client AI-adoption assessment | not available | 9 | 21 | 2,731 |
| AI-uplift community | not available | 4 | 5 | 1,792 |

All figures were counted by code from the session history.

## 1. Agent workspace and tooling

Alejo maintains their own working setup: a `proj` command for creating and opening project folders (in a dotfiles repo), an agent server with automations, a terminal app called Umi, and the folder and AGENTS.md conventions the assistants work under.

**Worked example: the `proj` command, 29 October to 3 November.** The command changed over five sessions. On 29 October Alejo first asked for a `--cd` flag.

*Alejo, 29 Oct, 11:38 and 11:39:*
> can we edit the proj bash command so that I can pass a flag to cd into the creted folder?
>
> actually, is there a better way? maybe I can just do a pipe?

*Assistant reply:*
> Not a pipe exactly: `cd` ignores stdin, and `proj x | xargs cd` changes the directory of a child process that exits right away. **Command substitution** does what you want, though:

The assistant had already half-built the flag. Alejo then learned the command already had a `--claude` flag, wrote "I had forgotten, let's leave things as it is", and the assistant reverted its edits. Two hours later Alejo asked for a no-argument `proj` that jumps to the latest project, then added "latest should only be for projects in projects/". On 2 November Alejo moved the same command towards a picker.

*Alejo, 2 Nov, 10:46 and 10:56:*
> let's do proj --list to show a tui with projects from newest to oldest and if I type a name it should fuzzy filter for that name
>
> would it conflict if we made proj --list the behavior when typing just proj

*Assistant, 10:56:*
> No conflict: nothing else calls plain `proj` and depends on its output. Making the change.

The next day Alejo asked the assistant to "make proj stop copying github to clipboard", undoing a behaviour added on 2 November.

**How AI is used here**
- Iterating on the `proj` command across five sessions, each a small change with a test run by the assistant.
- Reorganising folders and conventions, including renaming `clients/` to `uplift/` (31 October) and pruning AGENTS.md files.
- Server automations: changing when call emails appear and drafting proposals for the next "docket" run.
- Building apps: a daily-plans editor (11–12 October), the Umi terminal app and a Chrome-extension experiment (26–27 October).
- Housekeeping: switching the Google Docs tool and auditing installed hooks.

**Corrections**
- "actually, is there a better way? maybe I can just do a pipe?" (interrupted a half-built flag)
- "I had forgotten, let's leave things as it is" (dropped the flag work)
- "latest should only be for projects in projects/"
- "not blue dot, grey is fine. don't want it to be attention grabbing." (daily-plans editor)

**In my words**
- "the idea is to make things readable, separate ideas should be separate in the page and layout should indicate structure."

## 2. AI-uplift coaching and client calls

Alejo coaches and advises organisations on AI adoption. The evidence is a stream of recorded calls (a `/summarize-call` routine files each one), call reviews, mentoring calls and work with a prospective client.

**Worked example: reviewing a prospect call, 30 October.** Alejo asked the assistant to walk through their call with a contact at a prospective client.

*Alejo, 30 Oct, 10:36:*
> look at my call with [the contact]. open the gdoc on my browser and let's walk through the call to notice opportunities for improvement. let's start with the call opening. my read is I proposed a couple questions and [they] deflected to offer context on [their org]. what happened there?

Claude replied that the transcript did not support that reading.

The assistant went on to say the opening had no frame: no introductions, agenda or time check. Alejo interrupted the next request and sent it again with a clearer aim.

*Alejo, 30 Oct, 10:41:*
> this is very useful. could you to an alternative history version of the call where I correct many of the things you point out? feel free to fill in some of the gaps with your guesses if needed to keep narrative coherence? mostly I want to have a vivid picture of what I could have done better and what diffrence that would have made to the call

The assistant wrote a replay of the call in which Alejo opens with introductions, an agenda and a time check.

Later that day Alejo had the assistant compare the call with a second prospect call.

**How AI is used here**
- Summarising and filing call recordings with `/summarize-call`: typed eight times between 16 and 30 October, plus five headless runs the assistant launched.
- Reviewing Alejo's own calls: opening review, replay and a comparison across two calls (30 October).
- Preparing calls: drafting questions and closing asks from a contact's emails (28 October).
- Researching prospective clients (28 and 30 October).
- Cross-call analysis: a ranked list of people to introduce a contact to, a list of people to point another contact to, and a document built from coaching-call transcripts (29–31 October).
- Designing the practice: finding clients' pressing problems and choosing mentors (26 October).

**Corrections**
- "[Request interrupted by user]" (then re-asked the replay with a clearer aim)
- "1, as presented at least, doesn't sound particularly surprising."
- "don't necessarily focus on giving me specific takes."

**In my words**
- "this is very useful."
- "I'm not too fond of the snippets we have here."
- "this is much better, but don't give role titles."

## 3. Consulting-client AI-adoption assessment

Alejo ran an October 2026 AI-adoption assessment for a consulting client. It consisted of 25-minute interviews with staff about how they use AI, a capture sheet of extracted fields, and a findings report and coaching plan. The evidence is the project files, the interview transcripts and the Fathom and Granola recordings.

**Worked example: designing the capture sheet, 14–15 October.** Alejo had a batch of interview transcripts and no agreed structure for what to pull from them.

*Alejo, 14 Oct, 13:02:*
> Look through the last calls that I've had with [the consulting client's] employees, and and help me think of. So I'm trying to think of which structure fields or quotes or items we can extract from them. And so I guess one of some some of the fields are about kind of like how do they break down their time. Uh, kind of like what are what are the main tasks? Ideally, with like a concrete description we can get for each.

The assistant read five transcripts and drafted a schema with one record per person, each item carrying a label, a short description and a verbatim quote.

Alejo left comments on the draft fields in a throwaway picker. The assistant then proposed 19 final fields and a script to fill them.

*Alejo, 15 Oct, 09:35:*
> not sure we need a deterministic script. just documenting steps might be good enough (it fails more gracefully to changes). no need to call apis. and I say yes to your proposed fields including the adoption scale

*Assistant, 15 Oct, 09:43:*
> **The steps** are at the end of `capture-fields.md`:
> 1. Find interview calls that aren't in the sheet yet.
> 2. Read the transcript and your people-tab notes.
> 3. Fill each field, citing the transcript lines it draws on.
> 4. Add the person to the sheet and run the quote check.
> 5. When someone has a second call, change only the cells you haven't edited. For cells you have edited, the new draft appears next to your entry.
>
> To test the steps, I gave each person's record to a separate agent working only from the doc. They each reported where it was unclear, and I added rules for those cases:

Two hours later Alejo cut those added rules.

*Alejo, 15 Oct, 11:38:*
> no need to add the rule. it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations. some guidance for consistency is good, otherwise intent might sufice. not sure if there's other very specific rules incldue there

*Assistant:*
> I've trimmed `capture-fields.md` from 157 to 135 lines, and committed and pushed it. Each field now says what it captures, and edge cases are left to judgement.

**How AI is used here**
- Summarising each interview with `/summarize-call` and filing it: typed 12 times between 12 October and 3 November, plus 8 headless runs the assistant launched.
- Designing and filling the capture sheet from transcripts, with separate agents filling one person's record each.
- Checking questions: pulling the most detail-rich snippets from the interviews and suggesting how to sharpen later questions (14 October).
- Setting up Fathom to join the interview calls (12–14 October).

**Corrections**
- "not sure we need a deterministic script."
- "no need to add the rule."
- "and let's remove the 'they said' so it's assumed as the default and keep only 'alejo raised it'"
- "where did you get this detail?" (questioning a claim in a summary)

**In my words**
- "it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations."
- "just documenting steps might be good enough (it fails more gracefully to changes)."

## 4. AI-uplift community

Alejo runs an AI-adoption community Slack, with a community channel in it. The evidence is the group call planning, the channel's moderation, and the bots Alejo built for it.

**Worked example: a moderation bot for the channel, 27–31 October.** Alejo asked for a bot to reply to posts that don't fit the channel.

*Alejo, 27 Oct, 09:52:*
> use the slack credentials for [the community Slack] we had gotten to make the slack clis and use them to make a bot with a separate identiy call it 'Moderation Bot' or similar, that is triggered whenever a new top-level message appears on a channel. I plan to use it to reply to messages that don't pass a moderation bar asking their users to delete them (see recent example in [the community channel]).

The assistant built and tested it in a private channel that day. The bot was left in test mode. Four days later a post slipped through.

*Alejo, 31 Oct, 11:10:*
> i remember having setup a moderation bot on the server for these kinds of posts. why did it not trigger here?

*Assistant:*
> 1. **The channel is set to `off`.** In [the bot's config file], [the community channel] has `mode = "off"`. On Oct 27 you only set it to `live` in [a private test channel]. The project's notes say a main channel goes `live` only once you approve it.
> 2. **The bot process isn't running.** It was a test run on [his Mac] with no hosting. The last entry in its decision log is from Oct 27, and no `modbot` process is running now. So even with the channel set to `live`, nothing would have replied.

Alejo had it set live on the server within two minutes and tightened the rule soon after.

*Alejo, 31 Oct, 11:19:*
> thanks, can we change the moderation rules to trigger on every template message (ie., not specifically drafted for this channel) and then list for me the things it would have flagged retroactively? the new policy is no template message without asking me first

*Assistant:*
> - **The rule:** a post is flagged if it wasn't written specifically for this channel, whatever its topic. A one-line personal note on top of a pasted announcement still counts as a template. When the model is unsure, it still leans toward not flagging.

**How AI is used here**
- Building, deploying and revising the moderation bot over two sessions, including a check of Alejo's own DMs for prior approval and a public repo with setup steps.
- Requesting an anonymous-feedback bot and a showcase bot in one message (31 October).
- Planning a community group call (1 November): reading the Slack channel for demand signals, proposing topics, setting up a scheduling poll.
- Drafting "TVTropes-style" pages of AI-usage lessons (29 October).

**Corrections**
- "the classification looks correct, the close calls you mentioned should pass, and the message should be more like:"
- "remove this: and Alejo will take a look."
- "shorter"
- "if the deployment costs us anythign kill it. it was a fun experimetn" (dropped the AI-lessons site)

**In my words**
- "the classification looks correct, the close calls you mentioned should pass"
- "many of the titles are great, and very relevant."
