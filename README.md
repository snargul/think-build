# Think → Build

Turn an idea into tested, working code with AI, while you make the decisions.

```
/clarify → you read the spec → /build → you check the report
```

## How to use

1. **Describe your idea:** `/clarify a habit tracker where I log my daily study hours`
   Answer the questions, then read the spec in `specs/`.
2. **Build it:** `/build`
   It writes the code with tests, checks the app in a browser, and tells you what to look at.

New project? Click **Use this template** on GitHub. Existing project? Copy `PROJECT.md`, `.claude/` and `.vscode/` into it.

## What's inside

| | |
|---|---|
| `PROJECT.md` | Your project and your rules. Fill in the `<...>` parts. |
| `/clarify` | Asks questions until your idea is a clear spec. |
| `/build` | Builds the spec test-first and reports what's done. |
| `clicker` | Clicks through your app in a browser after `/build` and saves screenshots. |

## Good to know

- You need **Node.js 18+** and **Google Chrome** for the browser check.
- Nothing is committed for you. Review the changes, then commit yourself.
- Works in Claude Code and GitHub Copilot (VS Code).
