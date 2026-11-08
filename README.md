# Luca

An agent skill for Claude Code and Codex that gets you a working understanding of a topic,
a question or a codebase fast, then goes deeper only where the work needs it.

Named after Luca Pacioli, who taught Leonardo da Vinci mathematics in his forties, when his
work finally called for it. Luca works the same way: theory arrives when the work needs it.

## Install

```sh
git clone https://github.com/Ak-prog-50/luca.git ~/.claude/skills/luca   # Claude Code
git clone https://github.com/Ak-prog-50/luca.git ~/.codex/skills/luca    # Codex
```

## Use

Just ask to understand something; the skill triggers on its own:

- "Help me understand how this codebase handles auth"
- "I want a working feel for consistent hashing"
- "Does Rust discourage learning electronics?"
- "Resume bottega"

Luca checks what you already know, maps the area with the questions worth asking, then
takes you through small hands-on stops: predict, run, compare. Progress lives in a
`bottega/` folder in your repo, so any new session can pick up where you left off.

## The ladder

Each rung means something slightly different depending on what you're learning:

| Rung | Learning a topic | Learning a codebase |
|---|---|---|
| **Scout** *aka Orient* | Say what it's for and what it assumes | Say what each part does and how data moves between them |
| **Wield** *aka Apply* | Solve a real problem with it yourself | Make a change through every layer yourself |
| **Reforge** *aka Rebuild* | Write it from a blank file | Trace one request's full path from memory, then confirm it by running it |
| **Vouch** *aka Own* | Judge someone else's or an AI's version, and know how it fails | Debug it under pressure, review AI-written changes, be on call for it |

Your goal (for a topic) or the stakes (for a codebase) decide how high to climb.

## License

[MIT](LICENSE)
