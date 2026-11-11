# Alejo's work map, 28 September to 9 November 2026

Alejo's AI use falls into six areas. Ranked by active days: working setup and automations, a consulting client, coaching and audit call records, an AI-adoption community Slack, new-client development (two prospects), and Motif (engagement design and AI-lessons writing). AI use is heaviest in the working setup (the most sessions and words typed) and lightest in the call records, where most sessions were a one-command summary run with nothing typed. Motif has the fewest sessions but long messages.

**Note.** I could only read Alejo's Claude Code history for this period. I couldn't reach a calendar, email, documents, Slack, meeting notes or any claude.ai or ChatGPT history, so calendar hours are unavailable and the ranking uses active days, then AI sessions. Each session went to one responsibility by its working folder, and in shared folders by keywords in its first three typed messages. Counts cover sessions where Alejo typed, exclude pasted and automated text, and use UTC dates. Personal and household sessions are left out.

| Responsibility | Calendar hours | Active days | AI sessions | Words typed |
|---|---|---|---|---|
| Working setup and automations | not available | 17 | 42 | 7,241 |
| Consulting-client engagement | not available | 8 | 14 | 2,591 |
| Coaching and audit call records | not available | 6 | 6 | 441 |
| AI-adoption community Slack | not available | 4 | 5 | 1,120 |
| New-client development (two prospects) | not available | 3 | 7 | 1,100 |
| Motif: engagement design and AI-lessons writing | not available | 2 | 4 | 1,618 |

## 1. Working setup and automations

Alejo maintains the machinery around their work: how work folders and agent instructions are organised, an email-sorting and weekly-digest system on a home server, and small tools for their own use. 

**Worked example: sorting email.** On 24 Oct Alejo asked for a sorting scheme, then had it built and scheduled.

Alejo, 24 Oct:
> nice, now look at my email history and let's design a schema to classify emails into folders. some important folders are: calls (a frequent thing, not sure if having the call email adds anything over the calendar entry, but still) and receipts and deliveries, and personal communication (e.g., emails from actual people addressed to me) I don't want to have that many categories, just an easy way of scrolling for a recent thing + some rules of when each thing might be moved out of inbox or brought back in

Claude, 24 Oct:
> I read 200 threads from Aug 8 to Oct 24 (about 18 a week, not counting threads you only sent). They sort into five labels plus a delete pile. Your inbox stays the place for things that need you. Every kept email also gets one label, and the label stays on after you archive, so each label works as a list you can scroll by date.

Alejo then set rules, asked for a review page of paragraphs rather than one line per email, and had the sorter scheduled and run over the year's mail. Two days later Alejo changed one rule: "make the email automation in the server show up call emails 2 days in advance instead of 3."

**How AI is used here:**
- Email sorting and a weekly digest on the server: designed 24 Oct, adjusted 26 Oct and 1 Nov.
- Reorganising work folders and agent instruction files: 31 Oct and 1 Nov.
- Building small tools: a daily-plan editor (11 to 12 Oct), the umi terminal app (26 to 27 Oct), a `proj` folder command (29 Oct to 3 Nov).
- Debugging a bot Alejo had handed over to a former employer, with browser control and a headless Codex check (15 Oct).

**Corrections:**
- On the review page: “let's remake the artifact. unit of review should not be each email.”
- On the folder rules: “remove "Code that runs or gets deployed gets its own repository"”
- On autonomy: “"say a project Alejo uses regularly moves to stash/" this should be approved by me before its done”
- On an unchecked diagnosis of the handed-over bot: “did you check on the admin panel whether the [setting] is attached to the [channel]? feel free to have a headless codex check and inform you”.

**In my words:**
- “this is beautiful, I just installed as an app.”

## 2. Consulting-client engagement

Alejo does AI-uplift work for a consulting client: audit calls with its staff (18 between 13 and 23 Oct, per the sessions) and a sheet of what each person said.

**Worked example: the call-capture sheet.** From 14 Oct Alejo had Claude turn the audit-call transcripts into a structured sheet, dictating the first request.

Alejo, 14 Oct:
> Look through the last calls that I've had with [the client's] employees, and and help me think of. So I'm trying to think of which structure fields or quotes or items we can extract from them. And so I guess one of some some of the fields are about kind of like how do they break down their time. Uh, kind of like what are what are the main tasks? Ideally, with like a concrete description we can get for each.

Claude restated the goal as a schema for one person at a time, drafted it from five interviews, and next morning proposed a final field list after Alejo commented in the sheet.

> [Claude, 15 Oct] I've written the proposal to [a proposal file] in the project and committed and pushed it. It proposes 19 fields, a redefined adoption scale for us to agree on, and a script that fills the sheet from any new transcript.
> [Alejo, 15 Oct] not sure we need a deterministic script. just documenting steps might be good enough (it fails more gracefully to changes). no need to call apis. and I say yes to your proposed fields including the adoption scale

**How AI is used here:**
- Designing and filling the call-capture sheet, one subagent per interviewee (14 to 16 Oct, repeated as each new call arrived).
- Summarising single calls into the archive and adding them to the sheet (15 Oct onward).

**Corrections:**
- On an edge-case rule Claude added: “no need to add the rule. it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations.”

**In my words:**
- “just documenting steps might be good enough (it fails more gracefully to changes).”

## 3. Coaching and audit call records

Alejo records coaching and audit calls with organisations and individuals in a calls archive and writes follow-up documents from them. Many sessions were only a call-summary run, which the table doesn't count.

**Worked example: a guide for another consultant.** On 29 Oct, after a call with a contact about to start audit interviews at another organisation, Alejo asked what to send. Claude showed five sample highlights.

> [Alejo, 29 Oct, 20:39] let's do only audit calls, and let's select the questions that led to meaningful / surprising answers. define a maximum verbatim snippet lenght and feel free to use ellipsis in both questions and answers when that helps the interaction be clearer
> give me a few examples of highlights you'd put in the docs before doing the full thing
> [Alejo, 29 Oct, 20:46] 1, as presented at least, doesn't sound particularly surprising. maybe it's an update againt the work being completely rote, but it's not infromation rich
> I also don't feel too happy about 2.
> 3 is better

Claude redid the samples to follow a template document.

Claude, 29 Oct:
> Each highlight starts with the template question it serves. Questions are at most 40 words, each answer is at most 70 words, and an exchange has at most four turns. `…` marks a cut. The text comes from the archive transcripts. I've removed the quotation marks those files use to flag exact words inside lightly tidied speech. People appear by role.

Alejo asked for no role titles, and Claude built the full document (23 exchanges), shared as a Google Doc.

**How AI is used here:**
- Filing call transcripts into the archive with the summarize-call skill, many times from 12 to 30 Oct, mostly without typed input.
- Listing people to introduce someone to, from what calls revealed (23 and 31 Oct).

**Corrections:**
- “1, as presented at least, doesn't sound particularly surprising.”
- “I'm not too fond of the snippets we have here.”
- “skip the meta-advcie.”

**In my words:**
- “this is much better, but don't give role titles.”

## 4. AI-adoption community Slack

Alejo runs an AI-adoption community Slack workspace, including a community channel for posts about AI.

**Worked example: the moderation bot.** On 27 Oct Alejo asked for a bot to reply to off-topic template posts.

Alejo, 27 Oct:
> use the slack credentials for [the community Slack] we had gotten to make the slack clis and use them to make a bot with a separate identiy call it 'Moderation Bot' or similar, that is triggered whenever a new top-level message appears on a channel. I plan to use it to reply to messages that don't pass a moderation bar asking their users to delete them (see recent example in [a community channel]).

Claude built and tested it in a private channel. On 31 Oct a new template post went unflagged.

> [Alejo, 31 Oct] i remember having setup a moderation bot on the server for these kinds of posts. why did it not trigger here?
> [Claude, 31 Oct] The bot never saw this post. It was never switched on for [a community channel], and it isn't running anywhere.
> 1. **The channel is set to `off`.** In [the bot's channel settings], [a community channel] has `mode = "off"`. On Oct 27 you only set it to `live` in [a private test channel]. The project's notes say a main channel goes `live` only once you approve it.

Alejo had it switched on and moved to the server, then tightened the rule.

> [Alejo, 31 Oct] thanks, can we change the moderation rules to trigger on every template message (ie., not specifically drafted for this channel) and then list for me the things it would have flagged retroactively? the new policy is no template message without asking me first
> [Claude, 31 Oct] **The rule:** a post is flagged if it wasn't written specifically for this channel, whatever its topic.

**How AI is used here:**
- Building and operating the moderation bot (27 and 31 Oct), then a public repo and an anonymous-feedback bot (31 Oct).
- Mining the community's channels and calls for discussion topics and shared resources (23 Oct, 1 Nov).

**Corrections:**
- On the bot's reply text: “remove this:  and Alejo will take a look.”
- On the first classification: “the classification looks correct, the close calls you mentioned should pass, and the message should be more like:”

**In my words:** none stated.

## 5. New-client development (two prospects)

Alejo is trying to win independent AI-uplift clients, beginning with a prospective client and another prospect. The evidence is a folder of prospect research and call reviews.

**Worked example: reviewing a prospect call.** On 30 Oct Alejo asked Claude to review their 28 Oct call with a contact at the prospective client.

> [Alejo, 30 Oct] look at my call with [the contact]. open the gdoc on my browser and let's walk through the call to notice opportunities for improvement. let's start with the call opening. my read is I proposed a couple questions and [the contact] deflected to offer context on [their] org. what happened there?

Claude replied that the transcript did not support that reading.

Alejo then asked for an alternative-history version of the call with the mistakes corrected. Later that day Claude compared it with a call with a contact at the other prospect.

Claude, 30 Oct:
> You fixed most of the opening problems, and both calls still went wrong in the second half in the same ways. Your pitch came across as you thinking aloud. And each call ended with the client owning the next step.

**How AI is used here:**
- Researching both prospects, with a website version of the findings (28 and 30 Oct).
- Reviewing two recorded calls (30 Oct).

**Corrections:**
- On sharing a document: “and make the default in the skill sharing but without notifying”, interrupted, then “and make the default in the skill sharing and notifying”
- On a repository name: “rename repo to [name]”, then “rename repo to [new name]”

**In my words:**
- “this is very useful.”

## 6. Motif: engagement design and AI-lessons writing

Motif is Alejo's folder for open-ended projects. This area covers designing engagements that help people use AI, drawing on mentors' advice and consulting books, and a project to write TV Tropes-style pages about using AI.

**Worked example: the AI-lessons pages.** On 29 Oct Alejo described the idea and asked how to start.

> [Alejo, 29 Oct, 11:44] I want to encapsulate lessons about how to use AI in Tvtropes-like pages that open with a quote (often from fiction) that illustrates the concept, then give some examples and link it to other concepts there. the first step we need to resolve is where to get the lessons and patterns from, which we may start by doing a full sweep over all the docs/communication/relevant web content that could contain relevant insihgts
> how would you go about this idea?

Claude, 29 Oct:
> **Bottom line:** I'd start the sweep looking for concrete incidents, not lessons, and only after a cheap first pass gives us a draft list of tropes. Asking an agent for "lessons" across thousands of documents gets back generic advice like "be specific in your prompts." TV Tropes pages work because they're built from specific examples.

Claude produced twelve sample openings. Alejo's feedback:

Alejo, 29 Oct, 12:36:
> many of the titles are great, and very relevant. still, ocassionally the lesson/recommendation/narrative for how to deal with the pattern is not quite what I'd recommend, and often hides the complexity behind the thing. I think what I'd want is to create and extend a list of memorable titles, described by a direct quote if there's one or a short description that matches the original usage

Within about two and a half hours Claude had a live site of 192 pages.

**How AI is used here:**
- Planning consulting engagements and training formats, and learning from mentors and consulting books (26 Oct, three sessions).
- Building the AI-lessons site from calls, logs and Slack (29 Oct).

**Corrections:**
- On the line explaining each fit: “no need for the line on why it fits on the cases”
- On the deployment: “if the deployment costs us anythign kill it. it was a fun experimetn”

**In my words:**
- “many of the titles are great, and very relevant.”
- “this answer feels vague.”
