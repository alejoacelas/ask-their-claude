# Work map for Alejo Acelas, 28 Sep – 9 Nov 2026

**Opening.** Over the six weeks, Alejo Acelas's AI-assisted work falls into four responsibilities. In ranked order they are other/admin, AI-uplift clients, AI-uplift community and mentors, and personal tool projects. Other/admin and AI-uplift clients tie on active days; other/admin ranks first because it has more AI sessions. AI use is heaviest in other/admin, with the most sessions and words typed. It is lightest in community and mentors, which has the fewest sessions and fewest words typed.

**Note.** This report covers 28 Sep to 9 Nov 2026 and rests on one source: Alejo's Claude Code session history. I could not reach their calendar, email, Slack, documents, meeting notes or any other AI chat history. Calendar hours are therefore not measured, and responsibilities are ranked by active days, then AI sessions. An active day here means a day with an AI session where Alejo typed. Automated headless runs, pasted text and skill text are not counted as typed words. Personal-life matters are left out.

| Responsibility | Calendar hours | Active days | AI sessions | Words typed |
|---|---|---|---|---|
| Other/admin | not available | 14 | 35 | 5,995 |
| AI-uplift clients | not available | 14 | 32 | 4,262 |
| AI-uplift community and mentors | not available | 9 | 12 | 2,896 |
| Personal tool projects | not available | 6 | 14 | 2,950 |

---

## 1. Other/admin

This covers Alejo's own working infrastructure: the folder structure and instruction files for their agents, an agent server with email automation, a `proj` shell command, Google Docs tooling, and the handover of automations built for a former employer. Evidence is the session history in their inbox, desk and stash folders.

### Worked example: sorting the Gmail inbox, 24 Oct

Alejo began by testing whether the Gmail connector could move one email, then asked for a scheme for the whole inbox.

> **Alejo, 24 Oct 14:33:** nice, now look at my email history and let's design a schema to classify emails into folders. some important folders are: calls (a frequent thing, not sure if having the call email adds anything over the calendar entry, but still) and receipts and deliveries, and personal communication (e.g., emails from actual people addressed to me) I don't want to have that many categories, just an easy way of scrolling for a recent thing + some rules of when each thing might be moved out of inbox or brought back in

The assistant sampled recent mail and proposed labels.

> **Assistant, 24 Oct 14:36:** I read 200 threads from Aug 8 to Oct 24 (about 18 a week, not counting threads you only sent). They sort into five labels plus a delete pile. Your inbox stays the place for things that need you. Every kept email also gets one label, and the label stays on after you archive, so each label works as a list you can scroll by date.

Alejo then set their own rules: call emails stay in the inbox until opened and return three days before the call, and other mail is summarised in a weekly email. The assistant built a keyboard-driven review page for those summaries. Alejo asked for it to be rebuilt.

> **Alejo, 24 Oct 15:02:** let's remake the artifact. unit of review should not be each email. the review artifact should be paragraphs of text, with brief hyperlinks showing emails. with enter I should be able to select the current item under focus and open a text input to send some instruction to a claude to address. actually, maybe we should host it in our server so it's easier to launch new claude code sessions to execute on stuff on-demand?

After the rebuild, Alejo asked for the scheduled sorting and report to be set up and for the existing mail to be sorted retroactively. Later that day they asked for the digest to update daily.

### How AI is used here

- Gmail sorting, a weekly summary and a review page.
- Reorganising the folder tree and trimming agent instruction files (about a dozen sessions, 31 Oct – 1 Nov).
- Agent-server work: docket, clerk, email automation, permissions, hooks, resuming closed sessions (nine sessions).
- Diagnosing and handing over the former employer's automations (two sessions, 15–16 Oct).
- A `proj` command for jumping between project folders (four sessions).
- Google Docs tooling: switching the default CLI to `gog`, and `/loop` as an editing partner on a document (three sessions).
- A markdown editor for daily plans (one session).
- One-off questions on a GitHub connector and a billing issue (three sessions).

### Corrections

- 24 Oct, on the review page: "let's remake the artifact. unit of review should not be each email."
- 31 Oct, on the proposed instruction file: "remove "Code that runs or gets deployed gets its own repository""
- 31 Oct, on two rules the assistant had pushed back on: "for 2 I'd narrow the rule to "never send communication on my behalf without my explicit confirmation""

### In my words

- "I feel we have a lot of instructions that might get outdated as this folder evolves."
- "I want zero redundancy or things that might get stale."
- "this is great tahnks" (24 Oct, after the rebuilt review page).

---

## 2. AI-uplift clients

Alejo works as an AI-uplift consultant. Evidence is a series of 25-minute calls with a consulting client's staff for an October AI-adoption assessment, a call archive filed by client, and email and call preparation for other client organisations.

### Worked example: a structure for the consulting client's interview data, 14–15 Oct

Alejo dictated a long request about what to extract from the consulting client's calls and asked the assistant to restate it in its own words. It replied:

> **Assistant, 14 Oct 13:02:** **Goal:** design an extraction schema for your [consulting client] calls. It should work on one person at a time and stay general enough to fit the calls you haven't done yet, which will mostly follow the format of the last two. Whether the result ends up as a flat table can wait. For now we're only deciding which data to pull out.

Alejo agreed. The assistant read the transcripts, drafted a schema and loaded it into a capture-sheet editor. Alejo then built a field picker with the assistant, marked fields to keep and left comments. On 15 Oct they asked for a final proposal.

> **Alejo, 15 Oct 09:27:** nice, I left comments on many fields, including some that were dropped. check them out and give me a proposal for the final extracted fields. don't harcdoe the detail of my commetns, but rather use them as pointers. read the transcripts again if helpful to inform how you want to define the fields. make the workflow easy to extend and reproduce once more transcritps come

The assistant proposed 19 fields plus a script that fills the sheet from any new transcript. Alejo answered:

> **Alejo, 15 Oct 09:35:** not sure we need a deterministic script. just documenting steps might be good enough (it fails more gracefully to changes). no need to call apis. and I say yes to your proposed fields including the adoption scale

The assistant wrote the steps, then had seven separate agents fill in one record each, following only the written steps. It used what they reported to tighten the document.

### How AI is used here

- Filing each call with the `/summarize-call` skill: run by hand 14 times, plus 16 automated headless runs in the period.
- Designing and filling the consulting client's extraction sheet (three sessions, 14–15 Oct).
- Research and question preparation for client organisations from email threads and public pages (three sessions, 28–30 Oct).
- A walk-through of one recorded client call to find improvements (one session, 30 Oct).
- Analysing coaching-call transcripts for a template (one session, 29 Oct).
- Contact and introduction lists drawn from the call archive (two sessions).
- Setting up call recording and Slack access for the consulting client's calls (five sessions, 12–14 Oct).

### Corrections

- 15 Oct, on a rule the assistant added to the field document: "no need to add the rule."
- 15 Oct, on field formats: "let's redo role team and tenure to be straightforward (no clarification of source, just the value, in standard format eg. '3 months')"

### In my words

- "it's better not to rules-lawyer prompt so that models know to use their judgment for unusual sitations."
- "this is very useful." (30 Oct, after the assistant's walk-through of a client call)

---

## 3. AI-uplift community and mentors

This covers Alejo's work in the AI-uplift community and on their own development: a channel in an AI-adoption community Slack, a community call, material on using AI well, and the search for mentors.

### Worked example: a moderation bot for a community channel, 27–31 Oct

Alejo asked for a bot to handle template posts in a Slack channel they run.

> **Alejo, 27 Oct 09:52:** use the slack credentials for [an AI-adoption community Slack] we had gotten to make the slack clis and use them to make a bot with a separate identiy call it 'Moderation Bot' or similar, that is triggered whenever a new top-level message appears on a channel. I plan to use it to reply to messages that don't pass a moderation bar asking their users to delete them (see recent example in [the community channel]).

The assistant wrote a classifier, ran it over the channel's 151 top-level posts, created the Slack app and tested it in a private channel. Alejo reviewed the results, said the flagged posts looked right and that the close calls should pass, and wrote the wording of the bot's reply.

Four days later a template post appeared, and Alejo asked why the bot had not acted.

> **Assistant, 31 Oct 11:11:** The bot never saw this post. It was never switched on for [the community channel], and it isn't running anywhere. 1. **The channel is set to `off`.** In [the bot's config file], [the community channel] has `mode = "off"`. On Oct 27 you only set it to `live` in [a private test channel]. The project's notes say a main channel goes `live` only once you approve it.

Alejo had it set live and moved to the server, then tightened the policy.

> **Alejo, 31 Oct 11:19:** thanks, can we change the moderation rules to trigger on every template message (ie., not specifically drafted for this channel) and then list for me the things it would have flagged retroactively? the new policy is no template message without asking me first

The assistant re-ran the whole channel history with the new rule. It reported one remaining post that would be flagged, plus two already-deleted posts that would have been.

### How AI is used here

- Building and running the Slack moderation bot (two sessions, 27 and 31 Oct).
- Researching how to get mentors to help with AI power use and client work (three sessions, 26 Oct).
- Drafting a library of AI-usage lessons as pages with a title and opening quote, mined from calls and Slack (one session, 29 Oct).
- Preparing a community call and summarising what people shared in the community Slack (two sessions, 1 Nov).
- Publishing a readings repository (one session, 2 Nov).
- Finding a document and listing recommendations from Slack (two sessions).
- Filing a mentoring call (one session).

### Corrections

- 27 Oct, when the assistant would not delete test messages: "why can't you delete things in the test channel?"
- 29 Oct, on the lesson pages: "still, ocassionally the lesson/recommendation/narrative for how to deal with the pattern is not quite what I'd recommend, and often hides the complexity behind the thing."
- 31 Oct, on the bot's reply text: "remove this: and Alejo will take a look."

### In my words

- "I'm finding it hard to take seriously your "this is a good idea" judgement, maybe because off-the-cuff AI answers tend to be too agreeabel."
- "don't necessarily focus on giving me specific takes."

---

## 4. Personal tool projects

Alejo builds tools for their own use and learning: a morning-reading Android app for a Boox e-reader, a language-learning companion, a Mandarin viewing tracker, screen recording and editing tools, and a terminal app. Evidence is their dated project folders.

### Worked example: editing a 55-minute screen recording, 3 Nov

Alejo had a 55-minute screen recording of their language-app work, with a transcript, and asked the assistant to cut it down.

> **Alejo, 3 Nov 17:15:** get the latest download video and the granola trnascript (language app). I want to cut it to keep only ~20 minutes of highlight, but without disrupting continuity too much let's discuss what to keep and how visual aids could play into this (in addition of using visual aids to complement what happens on the screen (often I mumble a bit and there's lots of text on the screen)

The assistant proposed a keep-list by timestamp and drafted a vtuber-style overlay Alejo had asked for in a separate session. Alejo asked for an editing interface with section titles and speed-ups instead. The assistant built a player with chapters, a synced transcript and an edit mode, then tested it in Chrome on a second Mac.

> **Assistant, 3 Nov 18:38:** The player and editor work on the other Mac: 41 of 42 Chrome checks passed. The one failure was a bug in the test, now fixed in the test. Two changes since that run haven't been tested yet: transcript line times now use highlight time in viewer mode, and the player video is being re-encoded.

Alejo then changed the plan.

> **Alejo, 3 Nov 20:05:** nice, let's keep the same format but let's split into two videos. one video should be only about the chinese tracker, the other about the language learning app. speed up the parts that are about the other app, and if there's something that's not worht keeping, speed it on from its own video (though we should have a higher bar for speeding up now, because I'll direct people to watch only one of the two videos, so we're not on such a tight time constraint)

### How AI is used here

- The morning reader app and its Boox e-reader fixes (four sessions, 10–27 Oct).
- Designing a language companion and comparing speaking-focused apps (two sessions, 3 Nov).
- Building a Mandarin viewing tracker, starting with a Chrome extension and ways to connect other apps (two sessions, 3 Nov).
- Recording, editing and avatar-overlay tools for screen videos (four sessions, 3 Nov).
- A terminal app run across two Macs, and a Chrome extension for comment threads on web pages (two sessions, 26–28 Oct).

### Corrections

- 3 Nov, dropping the overlay for the moment: "let's ignore the vtuber thing for now."
- 3 Nov, redoing the overlay character: "better. but make it from scratch, this time 3d and animate a couple short clips for me"
- 3 Nov, dropping the length target: "I made the calibration clip. let's skip the 20 min thing."
- 3 Nov, on a recording tool: "I don't see the app"

### In my words

- "zoom on active pane is good. speed up with a title over the speed up is good."
- "don't ask me for confirmation, just use adversarial review to test reliability"
