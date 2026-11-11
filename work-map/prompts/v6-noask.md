I'd like you to map my main work over the last six weeks and show where my AI assistant (Claude, ChatGPT or similar) fits in it. The result is a report I'll check and then share with the person who sent me this prompt.

**First,** tell me in one short message what will happen: you'll search what you can reach, write the report, and hand it to me to check. You won't send or share anything.

**Sources.** Work them out yourself and try each one: my calendar, email, documents and files, Slack or other chat tools, meeting notes, and my AI chat history. In Claude Code, past sessions are in `~/.claude/projects/*/*.jsonl`. Keep track of what you read fully, read partly, or couldn't open. Don't ask me for anything you can find. There's likely a lot of material, so split the reading across subagents if you can start them, for example one per source or per two weeks. If you can't, read in batches and keep notes as you go.

**Step 1: find my responsibilities.** A responsibility is an ongoing area of my work, such as a client engagement, a programme I run, a tool I'm building, or my own admin. A single task is not a responsibility. Find them from my calendar, email, documents and chat tools first, then from my AI history. Expect about 4 to 7. Leave out personal matters.

Don't ask me about the list. Assign each piece of work to exactly one responsibility by a fixed rule you choose before counting (for example by client, project or calendar event title), apply it with code, and state the rule in one line in the report's note. If two areas are close, keep them separate and say so in the hand-off.

**Step 2: measure each one,** with code where you can run it ("counted by hand" where you can't; never estimate):
- **Calendar hours** on it, from events you can attribute to it.
- **Active days:** distinct days with a meeting, a sent email, an edited document, a chat-tool post, or an AI session where I typed.
- **AI use:** sessions or chats, and words I typed in my own messages, excluding pasted text.
Rank responsibilities by calendar hours where the calendar covers them, then by active days.

**Step 3: write the report.**

- **Voice.** Write in your own voice, about me in the third person by my name, using "they" rather than a gendered pronoun. "I" means only you ("I couldn't open the calendar"). My voice appears only in quotes.
- **Opening.** A few sentences: my responsibilities in ranked order, and where AI use is heaviest and lightest. Write it last, from the body.
- **Note.** Two or three lines: what the report covers, which sources you couldn't see, how the ranking works. Describe anything left out in general terms only.
- **Overview table.** One row per responsibility with its hours, active days, AI sessions and words typed. Keep these numbers in the table; don't repeat them in the sections.
- **One section per responsibility.** Each stands on its own and never refers to another section.
  - One or two lines on what the responsibility is, with its evidence (a meeting series, a document, a client).
  - **The core: one worked example.** Pick a specific task within it that recurred or ran over several days, preferably one where I used AI. Show it through 2 to 4 longer excerpts copied word for word from the record, each about 50 to 150 words, with source and date, joined by a sentence or two of your own on what happened between them. Include both what I wrote and what the assistant or other people replied, so a reader can follow how the work actually went. If there's no AI use in this responsibility, use the record of the task itself (emails, documents, messages) and say there was no AI use.
  - **How AI is used here:** the distinct things I used it for, as a short list. Repeated runs of the same workflow count as one item, with how often it ran.
  - **Corrections:** times I corrected the assistant, redid its work or dropped it, each with a short quote.
  - **In my words:** up to three one-sentence quotes of what I said works or doesn't, or "none stated". Never infer a reason.
- Copy every excerpt and quote exactly. If you can't, leave it out rather than reword it. State facts without labels like "key" or "strong". Don't describe how you searched.
- **Length:** about 2,000 to 2,500 words. Fewer, fuller examples beat many thin ones.
- **Before handing over,** check that every number in the opening and the table matches the body, and that every excerpt is exact.

**What the report shares.**
- Never include health, family, relationships or other personal life, credentials, account numbers or personal financial details.
- Other people's messages: only short excerpts that the worked example needs. Name colleagues and clients only where the example needs it, and list who is named in your hand-off.
- Leave out anything I tell you to.

**Save and hand over.** If you can create a Google Doc in my Google Drive, save the report there as a new doc, without sharing it with anyone. Otherwise save it as one Markdown file (in a chat app, a downloadable file). Change nothing else. Then hand it over in a short message: the link or file, any borderline item with a suggested edit, who is named, and a reminder to check it before sharing. Don't repeat the report in the message.
