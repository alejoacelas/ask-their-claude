# Ask their Claude

A skill for asking a question of a colleague's AI assistant. It interviews you
briefly and writes a prompt. Your colleague pastes the prompt into their own Claude
or ChatGPT. Their assistant answers from what it can reach (chats, email,
calendar, documents, files), writes a short report, and hands it to them to check
before they send it back to you.

## Use the skill

Copy `skill/ask-their-claude/` into your skills folder, for example
`~/.claude/skills/ask-their-claude/` for Claude Code. Then say "ask their Claude"
and give your question.

- `SKILL.md`: how the skill interviews you, recasts your question into something
  an assistant answers reliably, and writes the prompt.
- `privacy.md`: the default rules for what a report shares and leaves out.

## Example: a work map

`work-map/prompts/` holds a prompt the skill helped write. It asks a colleague's
assistant to map their main work over six weeks and show where AI fits in it.
There are two versions. `v6-confirm` asks the colleague to confirm the list of
responsibilities once. `v6-noask` asks nothing.

`work-map/results/` holds six reports, three per version. Each run went through
Claude Code with only my own Claude Code session history to read: no calendar,
email or other connectors. Other people's names and client and employer details
have been replaced with roles or removed. Everything else is as the runs wrote it.
