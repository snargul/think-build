---
name: build
description: Implements a finished spec from specs/ task by task, test first, then verifies it and reports which acceptance criteria are done. Use this when the user asks to build, implement or code a feature that has a spec, typically after /clarify.
---

# Build

Implement a spec task by task, prove it with tests, and report honestly.
The spec is the source of truth. Reply in the user's language.

## Input
The spec name, e.g. `habit-tracker` for `specs/habit-tracker.md`.

## Before you start
- If the spec doesn't exist, still has open questions, or is below 90% confidence: stop and suggest `/clarify <name>`.
- Read `AGENTS.md` and the spec. Follow the project's rules and commands.
- New project? Set up the stack from the spec's Decisions with a working test command, and fill in Stack and Commands in `AGENTS.md`.

## For each task, in order
1. Write tests for the acceptance criteria this task covers. Run them and see them fail.
2. Write the simplest code that makes them pass.
3. Run the tests for this task and fix until they pass.
4. Tick the task in the spec: `- [x]`.

## Rules
- If the spec is unclear or looks wrong, stop and ask. Don't change scope silently.
- Never weaken, skip or delete a test to make it pass.
- Ask before adding a dependency or doing anything destructive (deleting files, resetting data, force-pushing).
- No secrets in code. Use environment variables and a `.env.example`.
- Stuck on the same failure after 3 attempts? Stop and explain what you tried.

## Finish
Run the full test suite, then reply with:
1. **Acceptance criteria**: a table with each AC, its status (done / partly / not done) and the evidence (test name or reason).
2. **How to try it**: the commands to run it, and 2–3 things to click or type to see it work.
3. **Check these yourself**: 3–5 specific places a human should look, such as assumptions you made, untested edge cases, security-sensitive code, or the parts you're least sure about.

Don't call the work done while any AC is only partly done.

## Why it works this way
- Tests first turn acceptance criteria into something checkable, so "done" means more than "the AI says it's done".
- There is always more generated code than time to read it. The last list points the user's attention where it matters most.
