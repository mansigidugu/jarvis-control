# 🤖 Jarvis Control Panel

This repo is the control panel for **Jarvis**, an autonomous agent that finds and fixes small,
well-scoped bugs across my GitHub repos and opens PRs for review.

### 🚀 [Launch the Jarvis Dashboard →](https://mansigidugu.github.io/jarvis-control/)

Also linked as this repo's **website** (top-right of the repo page, next to About).

## How to use it

Type a message in the dashboard's chat box (e.g. "fix the broken build in coursify" or
"scan my-portfolio for issues") and hit **Send to Jarvis**. It opens a pre-filled GitHub issue —
click **Submit new issue** there and you're done.

A Hermes watcher polls this repo's open issues labeled `jarvis-trigger` every ~10 minutes. When it
sees a new one (or a new comment from you on an existing conversation), it dispatches Jarvis to
act, then comments back on the issue with a summary + links to any PR(s) opened. The conversation
stays open for follow-ups — just comment on the same issue (or reply from the dashboard once that
lands) and Jarvis will pick it up on its next pass.

Prefer raw GitHub? The old structured forms still work too: **🔍 Scan a repo** / **🛠 Fix a
specific issue or PR** under [New issue](../../issues/new/choose).

## Standing behavior

Independent of manual triggers, Jarvis also runs automatically every 4 hours across all my
non-fork repos, looking for small, clearly-scoped, safe fixes (typos, broken links, simple logic
bugs, lint/test failures). It **never merges** — every fix lands as an open PR for human review,
branch-named `jarvis/fix-issue-<n>` or `jarvis/fix-pr-<n>`.

## Board

See the [Project board](../../projects) for a live view of trigger issues (Todo → In Progress → Done).
