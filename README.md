# 🤖 Jarvis Control Panel

This repo is the control panel for **Jarvis**, an autonomous agent that finds and fixes small,
well-scoped bugs across my GitHub repos and opens PRs for review.

### 🚀 [Launch the Jarvis Dashboard →](https://mansigidugu.github.io/jarvis-control/)

Also linked as this repo's **website** (top-right of the repo page, next to About).

## How to use it

Open a new issue here using one of the templates:

- **🔍 Scan a repo now** — tell Jarvis to immediately scan `owner/repo` for fixable issues / failing PR checks.
- **🛠 Fix a specific issue or PR** — point Jarvis at one exact issue/PR number to work on right away.

A Hermes watcher polls this repo's open issues labeled `jarvis-trigger`. When it sees a new one,
it dispatches Jarvis to act on it, then:

- Comments on the trigger issue with a summary + links to any PR(s) opened
- Closes the trigger issue when done

## Standing behavior

Independent of manual triggers, Jarvis also runs automatically every 4 hours across all my
non-fork repos, looking for small, clearly-scoped, safe fixes (typos, broken links, simple logic
bugs, lint/test failures). It **never merges** — every fix lands as an open PR for human review,
branch-named `jarvis/fix-issue-<n>` or `jarvis/fix-pr-<n>`.

## Board

See the [Project board](../../projects) for a live view of trigger issues (Todo → In Progress → Done).
