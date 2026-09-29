# Skills

A skill is a guide for one recurring job: **when it kicks in, what to do, and what shape the result takes.** Once you've done a job well with the AI, you write it up as a skill — and next time it goes the same way, without you having to explain it again.

Each skill has its own folder here:

```
skills/
  risk-assessment/
    SKILL.md
```

`SKILL.md` is an ordinary text file. **It works with any AI** — Claude, ChatGPT, Codex, Manus — because `AGENTS.md` has a table that tells every AI which skills you have and when to use them.

---

## How a new skill comes about

First do the job once with the AI, on real work. If the result is good, say:

> *Turn what we just did into a skill. Put it in the `skills/` folder and add it to the table in `AGENTS.md`.*

## What goes into a skill

```markdown
---
name: skill-name
description: What it does and when to use it — in the words you'd say yourself.
---

# Skill name

## When
## What to do, step by step
## What shape the result takes
## What not to do
```

The top part (`name`, `description`) is the same format Claude and other AIs use. That way you can later add the skill to a tool's own set of skills too, if you ever need to.

## Two rules

- **One skill, one copy.** The skill lives here. Don't copy it anywhere else — two copies drift apart.
- **A ready-made skill is a start, not the finish.** If you use a skill someone else made, do the first run on your own real work and let the AI ask what's different in your situation. Then fix the skill.
