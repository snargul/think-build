---
name: clarify
description: Turns a rough idea or feature request into a clear, testable spec by asking the user questions until the spec is about 90% complete. Use this whenever the user wants to start something new, add a feature, or says the idea isn't fully clear yet, before any code is written.
---

# Clarify

Turn a rough idea into a spec the user agrees with. You ask, the user decides.
Write no code in this skill. Ask and write in the user's language.

## Input
An idea in a few sentences, or the name of an existing spec in `specs/`.

## Steps
1. Read `AGENTS.md` if it exists. If the input names an existing spec, read it and continue where it stopped.
2. Create or update `specs/<short-name>.md` using the structure below. Fill in only what the user actually said.
3. Estimate your confidence (0–100%) that the spec captures what the user wants. Count only what the user said or confirmed, not what you could guess.
4. Below 90%: ask the 3–5 questions that would raise confidence the most.
   - Give each question 2–4 options. Mark one **(recommended)** with a one-line reason.
   - Show them in chat and also add them under `## Open questions`, each option starting with `- [ ]`, so the user can answer in chat or by ticking a box.
   - Ask product questions first (who, what, edge cases, what's out of scope), then high-impact technical choices (stack, data storage, how it runs).
5. Turn each answer into a requirement, acceptance criterion or decision. Remove the answered question and add a line to `## Decision log`. Go back to step 3.
6. Never fill a gap with your own assumption. If the user says "you decide", take the recommended option and log it as "proposed by AI, accepted by user".
7. At 90% or more with no open questions: write `## Tasks`, give a short summary and stop with:
   "Read the spec. If it matches what you want, run /build <short-name>."

## Spec structure
```markdown
# <Feature name>
**Confidence:** <n>%

## Goal                 <!-- who it is for and what problem it solves, 2–3 sentences -->
## Out of scope         <!-- what we deliberately won't do -->
## Requirements         <!-- R1, R2 … one testable sentence each -->
## Acceptance criteria  <!-- AC1, AC2 … Given / When / Then -->
## Decisions            <!-- important technical choices and why -->
## Tasks                <!-- small ordered steps, e.g. - [ ] T1: … (AC1, AC2) -->
## Open questions
## Decision log
```

## Why it works this way
- Questions with options are quick to answer. The recommendation shares what you know without taking the decision away from the user.
- The confidence number is a rough self-estimate, not a measurement. Its job is to keep you asking instead of guessing.
- Everything lives in one file, so the work survives a closed chat and /build has a single source of truth.
