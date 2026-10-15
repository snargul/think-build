---
name: build
description: Implements a finished spec from specs/ task by task, test first, then verifies it and reports which acceptance criteria are done. Use this when the user asks to build, implement or code a feature that has a spec, typically after /clarify.
---

# Build

Implement a spec task by task, prove it with tests, and report honestly.
The spec is the source of truth. Reply in the user's language.

## Input
Optional: the spec name, e.g. `habit-tracker` for `specs/habit-tracker.md`.
No name given? Use the spec in `specs/` that still has unticked tasks. If there are several, ask which one; if there are none, suggest `/clarify`.

## Before you start
- If the spec doesn't exist, still has open questions, or is below 90% confidence: stop and suggest `/clarify <name>`.
- Read `PROJECT.md` and the spec. Follow the project's rules and commands.
- New project? Set up the stack from the spec's Decisions with one command to run the app and one to run the tests, and write both into Stack and Commands in `PROJECT.md`.

## For each task, in order
1. Write tests for the acceptance criteria this task covers. Run them and see them fail.
2. Write the simplest code that makes them pass.
3. Run the tests for this task and fix until they pass.
4. Tick the task in the spec: `- [x]`.

## Rules
- If the spec is unclear or looks wrong, stop and ask. Don't change scope silently.
- Never weaken, skip or delete a test to make it pass.
- Never commit, push or create branches/PRs, even if the user asks during this skill. Leave all changes uncommitted so the user can review them first.
- Ask before adding a dependency or doing anything destructive (deleting files, resetting data, force-pushing).
- No secrets in code. Use environment variables and a `.env.example`.
- Stuck on the same failure after 3 attempts? Stop and explain what you tried.

## Finish
Run the full test suite. If the app has a user interface and a `clicker` agent is available, ask it to check the spec in a browser and include its results. If the app has a user interface but clicker isn't available, say so in the report. Then reply with:
1. **Acceptance criteria**: a table with each AC, its status (done / partly / not done) and the evidence (test name or reason).
2. **How to try it**: the commands to run it, and 2–3 things to click or type to see it work.
3. **Check these yourself**: 3–5 specific places a human should look, such as assumptions you made, untested edge cases, security-sensitive code, or the parts you're least sure about.

Don't call the work done while any AC is only partly done.

## Why it works this way
- Tests first turn acceptance criteria into something checkable, so "done" means more than "the AI says it's done".
- There is always more generated code than time to read it. The last list points the user's attention where it matters most.
