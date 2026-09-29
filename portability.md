# What works everywhere, and what is tied to one tool

Your brain is yours and works with any AI. This file is where that claim can be **checked**, not just promised.

The rule is in `AGENTS.md`: **when you add something that only works in one tool, add a row here in the same session.** The test takes five seconds — *if I opened this repo in a different tool tomorrow, would this still work?*

---

## Works everywhere

| What | Why |
|---|---|
| All `.md` files — your whole brain | Plain text. No tool owns this format. |
| `AGENTS.md` | Most AI tools look for this file on their own. |
| `skills/` | Every skill is a plain text file. Any AI can find them, because `AGENTS.md` says where they are and when to use them. |
| `.gitignore` | It belongs to the repo and git itself follows it. It keeps passwords and keys off GitHub, no matter who opens your brain. |
| Agent account Drive | Your files are in your account, not inside the AI tool. A new tool gets connected to the same account. |

## Only in one tool

| # | What | Where | What it does | What it costs to rebuild |
|---|---|---|---|---|
| 1 | Automatic reading of `CLAUDE.md` | `CLAUDE.md` | Claude Code reads it on its own at the start of every chat | A minute. In another tool, say in your first sentence: *"read AGENTS.md"*. |
| 2 | Connectors (Drive, GitHub) | In the AI tool's settings, **not in your repo** | Give the AI access to the agent account Drive and to your brain | A minute per tool. In the new tool, connect the same agent account and the same repo again. |

**Right now there are two rows here, and that is exactly right.** You are just starting. Every time you add an automation, a shortcut or a connection, a row gets added — and eight weeks from now you'll know exactly what you would need to rebuild if you switched tools.

---

## If you switch tools one day

1. Check whether the new tool reads `AGENTS.md`. If it doesn't, tell it yourself in every chat until it does.
2. Go through this list and rebuild only what you actually use.
3. Run one real piece of work from start to finish and **check the result, not the report.** An AI that can't follow an instruction will sometimes describe a success it didn't have.
