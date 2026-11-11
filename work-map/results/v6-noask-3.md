# Alejo's work map, 28 Sep – 8 Nov 2026, and where AI fits

**Opening.** Over the six weeks, Alejo's work falls into seven areas. Ranked by active days, they are: building and maintaining their own agent workspace and tools; independent AI-uplift consulting and coaching; a consulting client's AI-adoption assessment; personal software projects; the AI-uplift community; handing over automations to a former employer; and developing a mentoring practice (Motif). AI use is heaviest in the workspace tooling, with 38 sessions and 5,377 words typed on 18 active days; per session, the community work is heavy too (3,269 words in 6 sessions). It is lightest around the former-employer handover (2 sessions, 528 words) and the Motif mentoring work (3 sessions, one day). The consulting and client-assessment sessions centre on call summaries, preparation and review.

**Note.** This report covers 28 Sep – 8 Nov 2026. The only source I could open was Alejo's Claude Code session history, which holds activity from 4 Oct to 4 Nov (110 sessions with typed messages; 94 are counted below and 16 concern personal matters). I could not reach a calendar, email, documents, Slack, meeting notes, or any ChatGPT or claude.ai chat history, so responsibilities are ranked by active days (days with a typed message in an AI session; AI sessions break ties). I read every typed message, and assistant replies only for the worked examples. Each session went to one responsibility by the first matching keyword rule on its first message (former employer, then consulting client, consulting and coaching, community, the Motif folder, personal software, otherwise workspace tooling); personal-life matters were left out. Quotes are exact, typos included.

| Responsibility | Calendar hours | Active days | AI sessions | Words typed |
|---|---|---|---|---|
| Agent workspace and tooling | n/a | 18 | 38 | 5,377 |
| Independent consulting and coaching | n/a | 12 | 19 | 1,701 |
| Consulting client AI-adoption assessment | n/a | 8 | 14 | 2,142 |
| Personal software projects | n/a | 4 | 12 | 2,130 |
| AI-uplift community | n/a | 4 | 6 | 3,269 |
| Former-employer automation handover | n/a | 2 | 2 | 528 |
| Motif mentoring practice | n/a | 1 | 3 | 892 |

n/a: no calendar was reachable. Personal software projects and the AI-uplift community tie on active days; the one with more AI sessions ranks first.

## 1. Agent workspace and tooling

Alejo runs a personal system of folders, a home server, scheduled agents and small apps, and keeps reorganising it. Evidence: sessions in the inbox, desk and stash folders, 4 Oct – 4 Nov.

**Worked example: sorting and summarising email, 24–26 Oct.** Alejo asked for a filing scheme. *Claude Code, inbox folder, 24 Oct:*

> nice, now look at my email history and let's design a schema to classify emails into folders. some important folders are: calls (a frequent thing, not sure if having the call email adds anything over the calendar entry, but still) and receipts and deliveries, and personal communication (e.g., emails from actual people addressed to me)

The assistant read 200 threads and proposed labels. *Same session:*

> I read 200 threads from Aug 8 to Oct 24 (about 18 a week, not counting threads you only sent). They sort into five labels plus a delete pile. Your inbox stays the place for things that need you. Every kept email also gets one label, and the label stays on after you archive, so each label works as a list you can scroll by date.

Alejo then set the rules (calls leave the inbox once opened and return three days before the call; everything else is summarised in a weekly email) and had agents write three trial summaries.

**How AI is used here:**
- Reorganising folders and the instructions files (AGENTS.md): 11 sessions, counted by hand.
- Email sorting, digest and forwarding automation on the server: 3 sessions.
- The `proj` project-launcher command: 5 sessions.
- Building apps: a daily-plans markdown editor and a terminal app (Umi), plus filing issues for it: 3 sessions.
- Server and security upkeep (agent user, sudo, hooks, remote access, a security scan): 5 sessions.
- Google Docs tooling and a `/loop` editing partner: 4 sessions.

**Corrections:**
- Redid the review page: “let's remake the artifact. unit of review should not be each email.”
- Rejected part of a filing proposal: “"and list it for me" I don't want to review that”

**In my words:** “this is beautiful, I just installed as an app.”

## 2. Independent consulting and coaching

Alejo sells AI-uplift coaching and assessments to organisations and individuals. Evidence: calls summarised with `/summarize-call`, and a prospective client.

**Worked example: first call with the prospective client, 28–30 Oct.** Before the call, the assistant drafted questions and asks for Alejo. The day after, it assessed how the call went.

On 30 Oct Alejo went back through the recording with the assistant. *Claude Code, 30 Oct:*

> look at my call with [the prospect's contact]. open the gdoc on my browser and let's walk through the call to notice opportunities for improvement. let's start with the call opening. my read is I proposed a couple questions and [the prospect's contact] deflected to offer context on [their org]. what happened there?

Claude replied that the transcript did not support that reading.

**How AI is used here:**
- `/summarize-call`: 10 runs (counted by code), each making a transcript, summary and shared doc.
- Preparing for and reviewing prospect calls: 4 sessions.
- Documents for a contact (a ranked list of introductions, audit-call highlights): 2 sessions.

**Corrections:**
- “1, as presented at least, doesn't sound particularly surprising. maybe it's an update againt the work being completely rote, but it's not infromation rich”
- “this is much better, but don't give role titles.”

**In my words:** “this is very useful.”

## 3. Consulting client AI-adoption assessment

Alejo interviewed a consulting client's staff for 25 minutes each about how they use AI, for a findings report and coaching plan. Evidence: Fathom-recorded call series, a shared capture sheet, the client's Slack.

**Worked example: choosing what to capture from each interview, 14–15 Oct.** Alejo dictated the problem. *Claude Code, inbox folder, 14 Oct:*

> Look through the last calls that I've had with [the client's] employees, and and help me think of. So I'm trying to think of which structure fields or quotes or items we can extract from them. And so I guess one of some some of the fields are about kind of like how do they break down their time. Uh, kind of like what are what are the main tasks? Ideally, with like a concrete description we can get for each.

The assistant read five transcripts and drafted a schema. *Same session:*

> Each person gets one record with a short profile, a list of core activities, and three lists of items: patterns, growth opportunities and interventions. Every item has a structured label, a sentence or two of description, and a verbatim quote. Because the items share that shape, they flatten into one long table later, and the activities into a second.

After going through 33 candidate fields in a keyboard picker, Alejo asked for a final list. *Same session, 15 Oct:*

> nice, I left comments on many fields, including some that were dropped. check them out and give me a proposal for the final extracted fields. don't harcdoe the detail of my commetns, but rather use them as pointers. read the transcripts again if helpful to inform how you want to define the fields. make the workflow easy to extend and reproduce once more transcritps come 
>
> think well about the titles of the fields. I suggested some, but feel free to tweak change any title if you find something short that reflects the content of the field

The assistant then filled the sheet for seven people, using seven agents that each worked only from the written steps.

**How AI is used here:**
- `/summarize-call` on staff interviews: 7 runs.
- Designing and filling the capture sheet from transcripts: 2 sessions.
- Asking the assistant to add the Fathom recorder to the calls: 2 sessions.
- Slack and calendar lookups: 3 sessions.

**Corrections:**
- Dropped a proposed script: “not sure we need a deterministic script. just documenting steps might be good enough (it fails more gracefully to changes). no need to call apis.”
- Dropped a proposed rule: “no need to add the rule. it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations.”

**In my words:** “it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations.”

## 4. Personal software projects

Alejo builds apps for their own use: a reading app for a phone and an e-reader, language-learning and tracking tools, and screen-recording and avatar-animation experiments. Evidence: dated project folders, 10 Oct – 3 Nov.

**Worked example: the reading app, 10 Oct and 27 Oct.** Alejo asked where earlier improvement ideas were logged; the assistant found them only in an old transcript, then installed the latest build on the phone. *Claude Code, projects folder, 10 Oct:*

> Your phone now has the latest build, installed at 21:45. All 8 books, with their character notes, were pushed to it, and the app opens without crashing. A subagent is now checking the rest on the phone: the "Who's who" lists, videos opening at the end of a block, and notes saving and copying to the Mac.

Later Alejo extended the app to carry consulting books. *Claude Code, inbox folder, 27 Oct:*

> look for the morning reader / boox project and see how you could get the three consulting books I have in [a local folder]. ideally there would be a way to make it easy for you to send books and files for reading to the boox once I point them to you

**How AI is used here:**
- Reading app (building, phone installs, adding books): 4 sessions.
- Language-learning and tracking tools: 4 sessions.
- Screen recording and avatar animation: 4 sessions, with subagents doing parts.

**Corrections:**
- “better. but make it from scratch, this time 3d and animate a couple short clips for me”

**In my words:** none stated.

## 5. AI-uplift community

Alejo moderates and builds for an AI-adoption community Slack. Evidence: bot projects, a content project and group-call planning, 27 Oct – 1 Nov.

**Worked example: a moderation bot, 27–31 Oct.** Alejo asked why the bot built four days earlier had missed a post. *Claude Code, inbox folder, 31 Oct:*

> The bot never saw this post. It was never switched on for [a community channel], and it isn't running anywhere.
>
> 1. **The channel is set to `off`.** In [the bot's config file], [a community channel] has `mode = "off"`. On Oct 27 you only set it to `live` in [a private test channel].

Alejo had it deployed and widened its rule. *Same session:*

> thanks, can we change the moderation rules to trigger on every template message (ie., not specifically drafted for this channel) and then list for me the things it would have flagged retroactively? the new policy is no template message without asking me first

**How AI is used here:**
- Building Slack bots (a moderator, with a feedback bot started): 2 sessions.
- A collection of AI-use lessons for community readers: 1 session.
- Planning a community group call and summarising shared links: 2 sessions.
- Reorganising the work folders (a session the keyword rule placed here): 1 session.

**Corrections:**
- “many of the titles are great, and very relevant. still, ocassionally the lesson/recommendation/narrative for how to deal with the pattern is not quite what I'd recommend, and often hides the complexity behind the thing.”

**In my words:** none stated.

## 6. Former-employer automation handover

Alejo handed over automations they had built for a former employer and then helped debug one of them. Evidence: a handover request on 15 Oct.

**Worked example: debugging a handed-over bot, 15 Oct.** The assistant first offered an explanation it had not checked. Alejo challenged it. *Claude Code, inbox folder, 15 Oct:*

> did you check on the admin panel whether [the setting] is attached to [the channel]? feel free to have a headless codex check and inform you

The assistant admitted the claim had been a guess. *Same session:*

> You're right: I didn't verify that. [The claim] was a guess, and the admin panel contradicts it.

**How AI is used here:**
- Diagnosing and testing the bot through repeated test runs (1 session), and asking for the code to be linked in the handover docs (1 session).

**Corrections:**
- “did you check on the admin panel whether [the setting] is attached to [the channel]?”

**In my words:** none stated.

## 7. Motif mentoring practice

Motif is the folder where Alejo works out how to run engagements in which a client drives a project with Alejo as collaborator. Evidence: sessions in that folder on 26 Oct. This is close to the consulting area; I kept it separate because it concerns Alejo's own practice, not a client.

**Worked example: designing the engagement, 26 Oct.** Alejo described the format and asked how likely it was to work. *Claude Code, mentors folder:*

> I'm thinking of doing engagements where I try to get someone to go thorugh their list of very pressing problems, and pick something that looks enough like it can be solved by a dedicated expert team managed by them. then I offer myself as a collaborator on the proejc and we work on it together.

*Same session:*

> The prospects are good while the engagement runs and weaker after it ends. Paying clients who opted in, with you working alongside them on a schedule, will mostly keep going for 4–6 weeks almost regardless of which project they pick. Your recurring sessions are what keep them going, more than the project. Project choice decides whether the work keeps going once you leave.

**How AI is used here:**
- Stress-testing the engagement design and finding reading, in every session.
- Uploading three consulting books to a claude.ai project with chapter recommendations: 1 request.

**Corrections:**
- “fail 3. I actually kind of want them to drive the project. is that misguided?”
- “this answer feels vague.”

**In my words:** “I'm finding it hard to take seriously your "this is a good idea" judgement, maybe because off-the-cuff AI answers tend to be too agreeabel.”
