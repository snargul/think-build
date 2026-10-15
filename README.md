# Think → Build

A tiny starter kit for working with AI agents: two skills that turn an idea into tested code, with you deciding at every step.
From the talk *Beyond Coding: Engineering with AI Agents*.

```
idea → /clarify → specs/<name>.md → you read it → /build → report → you check it
```

## What's inside

| File | What it does |
|---|---|
| `AGENTS.md` | Tells the agent about your project and your rules. Fill in the `<...>` parts. |
| `.claude/skills/clarify/` | Asks you questions until your idea is a clear spec. Doesn't guess. |
| `.claude/skills/build/` | Builds the spec test-first, then reports what's done and what isn't. |

## Start in 3 steps

1. **New project:** click **Use this template** on GitHub. **Existing project:** copy `AGENTS.md` and the `.claude/` folder into its root.
2. In your agent's chat, type `/clarify` followed by your idea, e.g.
   `/clarify a habit tracker where I log my daily study hours`
   Answer the questions, then **read the spec** it writes to `specs/`.
3. When the spec looks right, run `/build habit-tracker`. Then go through the **"Check these yourself"** list at the end.

If the slash command doesn't show up, just ask: *"Use the clarify skill for: …"*

## Which tools?

- **GitHub Copilot** (agent mode in VS Code, Copilot CLI) and **Claude Code** both pick up skills from `.claude/skills/`. That's why the kit uses this folder: one copy works in both.
- **No agent tool?** Open a `SKILL.md`, paste it into ChatGPT, Claude or any AI chat, and add your idea. Same steps; you save the files yourself.
- **Claude Code tip:** to load `AGENTS.md` in every session, not only in these skills, create a `CLAUDE.md` with one line: `@AGENTS.md`

## Why not just chat?

A plain chat starts from zero, fills the gaps with guesses and tells you it's done. This kit adds four things:

- **Questions before code.** The agent asks; you decide. Gaps become questions, not assumptions.
- **A spec file.** Your decisions live in `specs/`, not in a chat you'll lose. The next session picks up where you left off.
- **Tests.** "Done" is checked, not claimed.
- **A report.** You learn what isn't done and where to look, not just what is.

## Ground rules

- **You own the result.** Read the spec before building. Read the code before shipping.
- **Mind what you share.** Don't paste company code, passwords or personal data into tools you're not allowed to use.
- **Make it yours.** These are plain text files. Change the questions, the spec format, the rules. That's how a real harness grows.
