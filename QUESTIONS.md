# Choosing what to ask

For whoever is helping someone (the asker) put a question to a colleague's AI assistant. The colleague pastes a prompt into their own Claude or ChatGPT; their assistant searches what it can reach, writes a report, and the colleague checks it before sending it back. The colleague's time and trust are the scarce part: the prompt has to work the first time, with little from them.

## Ask for the raw material, not the verdict

Assistants are reliable at pulling material out of the record: finding, quoting, collecting, counting, listing and ordering. They're unreliable at judgement: explaining why, deciding what matters, or suggesting changes. So ask for the raw material and let the asker draw the conclusions.

Settle with the asker first what the answer is for: the decision or next step it feeds. "Which tasks could be delegated" means different things for hiring an assistant and for building a tool.

Then recast the question into one of these kinds, or a combination of two. Show the asker the recast before writing the prompt ("I'll ask for the last five times Alejo prepared a call, not why he prepares that way"). If no kind fits, the question is better asked in person.

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
- "What could be improved, delegated or automated" becomes an **inventory** or **tally** with attributes the asker can judge, such as how much of the colleague's own input each task took and what they corrected.
- "The most important or judgement-heavy X" becomes a **tally** ranked by a stated measure.

## Size items by a measure that fits the question

Pick one or two and have the report name them:

- how often it happens;
- calendar hours;
- active days;
- words the colleague typed, excluding pasted text;
- distinct threads or sessions;
- corrections the colleague made to the assistant's work;
- days a thread spans;
- what the colleague's own documents, plans or priorities say matters.

Frequency overstates automated or repeated work: forty runs of a call-summary skill are one task.

Also settle the scope (which sources and what time range) and what "not found" looks like: the report says so and where it looked.

## Write the prompt

Fill in [TEMPLATE.md](TEMPLATE.md). It links the colleague's assistant to the shared guides ([SOURCES](SOURCES.md), [REPORT](REPORT.md), [PRIVACY](PRIVACY.md), [SAVE](SAVE.md)) and keeps in the prompt itself only what must hold even if the links fail: the check-in before searching, reading only, and the red lines. Write only the placeholders:

- `{intro}`: the question in the colleague's voice ("I'd like you to…"), addressed to their assistant, with what the answer is for and who reads it: "The result is a report I'll check and then share with …".
- `{looks_at}`: the sources this question needs. `{checkin_extra}`: one more line for the check-in, or empty.
- `{steps}`: what to find and how to measure it, from the recast: the unit, scope and time range, the sizing measures and the ranking. Bold run-in labels ("**Find the processes.**"), no step numbers.
- `{sections}`: the report's structure as a bullet list: what the opening and note cover, an overview table, a section per item with its excerpts. Section labels are in the third person ("In their words").
- `{length}`: about 1,500 to 2,500 words by default; about 600 to 900 for a narrow lookup.
- `{sharing}`: lines for this question on top of PRIVACY, such as who may be named. Agree them with the asker, and say plainly when the question needs other people named.
- `{base}`, `{doc}` and `{doc_edit}`: the guides' address for this version, the Google Doc that mirrors them as a plain page the assistant can read, and the same Doc's normal link for the person to copy from.

Give the asker the prompt in one copyable block, plus a short message to the colleague in plain sentences: what it reads, that it only reads, that they check the report before sharing it, and roughly how long it takes.
