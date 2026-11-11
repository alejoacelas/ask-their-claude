---
name: ask-their-claude
description: Turn a question for a colleague into a prompt they paste into their own Claude or ChatGPT, so their assistant answers it from their chats, files and connected tools and hands them a short report to check and send back. Use when someone wants to ask a colleague's AI about their work, or says "ask their Claude".
---

# Ask their Claude

You help the asker get a question answered by a colleague's AI assistant. The
colleague pastes your prompt into their own Claude or ChatGPT. Their assistant
searches what it can reach, writes a short report, and hands it to the colleague,
who checks it and sends it back. The colleague's time and trust are the scarce
part: the prompt has to work the first time, with little from them.

## 1. Interview the asker briefly

Ask only what you can't work out. Usually that is:

1. **The question**, and what the answer is for: the decision or next step it
   feeds. "Which tasks could be delegated" means different things for hiring an
   assistant and for building a tool; settle that here, not in the colleague's
   run.
2. **Who the colleague is,** and what the asker already knows about their work, so
   the report can skip it.
3. **What the report shares.** Propose defaults from [privacy.md](privacy.md) fitted
   to the question, and ask the asker to approve or change them. Say plainly when
   the question needs other people named (for example "which pain points did each
   person raise").

Offer choices as numbered options. If the asker gives everything in one message,
skip straight to writing.

## 2. Decide what to ask of the colleague's assistant

Assistants are reliable at finding, quoting, counting, listing and ordering what's
in the record. They're unreliable at explaining why, judging what matters or
suggesting changes. So recast the asker's question into one of the kinds below, or
a combination of two, and let the asker draw the conclusions. Show the asker the
recast question before writing the prompt ("I'll ask for the last five times Alejo
prepared a call, not why he prepares that way"). If no kind fits, tell the asker the
question is better asked in person.

| Kind | Example | The prompt specifies |
|---|---|---|
| **Find and quote** | What has Alejo said about pricing? | Word-for-word excerpts of at most about 40 words, each with source and date, chosen to make sense on their own; a cap on how many; no paraphrase, and "none found" if nothing fits |
| **Inventory** | Which tools has Alejo built? | The unit ("a tool is a project with its own folder"), scope and time range; one line per item with one piece of evidence; how duplicates are merged |
| **Tally and group** | How does Alejo's time split across clients? | The counting unit; categories, given or fixed before counting; counts computed, not estimated; the counting rule in one line |
| **Factual lookup** | What did Alejo decide about the finance portal's hosting? | The answer and its source in one or two sentences, or "not found" and where it looked |
| **Timeline** | What happened in the finance-tools project? | Dated events, each with a source; no verdict on how it went beyond the colleague's own words, quoted |
| **Process from instances** | How does Alejo prepare for client calls? | The last three to five instances first, then the steps they share; differences between instances shown |
| **Side by side** | How have Claude Code and Codex compared for Alejo? | Each instance of X and of Y with what happened, in two columns; no verdict |
| **Stated views** | Why does Alejo build his own tools? | Reasons and opinions the colleague wrote down, quoted; "none stated" rather than inferred reasons |

Recast questions this way:
- "Why" becomes **stated views**.
- "What could be improved, delegated or automated" becomes an **inventory** or
  **tally** with attributes the asker can judge, such as how much of the
  colleague's own input each task took and what they corrected.
- "The most important or judgement-heavy X" becomes a **tally** ranked by a stated
  measure.

**Size items by a measure that fits the question.** Pick one or two from this
list and have the report name them:
- how often it happens;
- calendar hours;
- active days;
- words the colleague typed, excluding pasted text;
- distinct threads or sessions;
- corrections the colleague made to the assistant's work;
- days a thread spans;
- what the colleague's own documents, plans or priorities say matters.

Frequency overstates automated or repeated work: forty runs of a call-summary skill
are one task.

Also settle:
- **Scope:** which sources and what time range.
- **What "not found" looks like:** the report says so and where it looked.

## 3. Write the prompt

Write the prompt in the colleague's voice ("my", "me"), addressed to their assistant; the report it asks for is in the assistant's voice (below). Give
the asker the prompt in one copyable block, plus two lines they can send with it:
what it does and roughly how long it takes the colleague.

The prompt tells the assistant to:

1. **Say what will happen, before anything else.** One short message: it will search
   what it can reach, write a report, and hand it over for the colleague to check
   and share. Nothing is sent anywhere by the assistant.
2. **Work out its sources itself.** Chat history, files, connected tools: try each,
   and keep track of what it read, partly read or couldn't open. Don't ask the
   colleague for anything it can find. In Claude Code, past sessions are
   `~/.claude/projects/*/*.jsonl`. When the material is large, split the reading
   across subagents if the surface has them, and say so explicitly in the prompt:
   chat surfaces skip subagents unless told. Without subagents, read in batches and
   keep notes as it goes.
3. **Compute counts with code** where it can run code, and say "counted by hand"
   where it can't. Never estimate a count.
4. **Search before asking.** Ask the colleague only what the material can't settle,
   in one message, with numbered options where possible. If the answer would change
   the report's structure, ask before writing it. Otherwise make a sensible choice,
   write the report, and name the choice in the hand-off.
5. **Write one report** as a Markdown file (in claude.ai chat, a downloadable file),
   and change nothing else on the machine:
   - It's written by the assistant, about the colleague in the third person and by
     name ("Alejo rewrote the prompt twice"), with "they" rather than a gendered pronoun unless the colleague's own material says which they use. "I" means only the assistant ("I
     couldn't open the project folders"). The colleague's own voice appears only in
     quotes. Speaking as the colleague would put premises in their mouth; reporting
     on them keeps each claim tied to its evidence.
   - It opens with the answer, in a few sentences the asker could repeat. It
     writes the body first and the opening last, from the body.
   - Right after, a note of two or three lines on what it covers, how it's
     organised, and what it couldn't see. Describe what it left out in general
     terms ("personal matters unrelated to the question"): naming a left-out
     topic discloses it.
   - Each item carries its own evidence. Never point to another section ("see
     section 2", "quote above"); repeat the short fact instead.
   - It's grounded in the colleague's own material: specific projects, dates and
     short quotes copied word for word, each with where it came from (session or
     file and date). It leaves out a quote rather than rewording one.
   - It states facts and lets the reader judge, rather than labelling things as
     "key" or "strong".
   - It's written for what the asker already knows. It leaves out how the search
     was done: no paths, error messages, counts of files read, or earlier figures
     it later corrected.
   - It's short: set a word limit in the prompt that fits the question, about
     600–900 words for most, more only when the asker wants everything in a
     scope. Give fewer, better-evidenced items rather than many thin ones.
   - Before handing over, it checks that every count and claim in the opening
     matches the body, and that every quote is copied exactly from its source.
6. **Respect what the report shares**, using the defaults the asker approved (paste
   them into the prompt).
7. **Read back a Google Doc before handing it over.** When the report is saved as a
   Google Doc, the run reads it back and checks the title and heading styles,
   paragraph spacing, block quotes and stray Markdown symbols, then fixes them in
   the same doc.
8. **Hand it over briefly.** Give the file path, flag any borderline item with a
   suggested edit, and ask the colleague to check it and share it themselves. Don't
   repeat the report in the message.

Fit the prompt to the question; drop any instruction it doesn't need. Keep it under
about 600 words.
