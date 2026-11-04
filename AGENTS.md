# Documentation project instructions

## About this project

- This is the documentation site for Slowave, built on [Mintlify](https://mintlify.com).
- Pages are MDX files with YAML frontmatter. Configuration, navigation and redirects live in `docs.json`.
- Pushing to `main` deploys the live site. Work on a branch and preview with `npx mint dev`.
- Before you push, run `npx mint validate` and `npx mint broken-links`.
- Slowave's code and the source of truth for product facts live in the `slowave-ai/slowave` repository.

## What this site is

The site presents the product to AI engineers. It is not a technical manual. Explain what Slowave does for the reader. Link to GitHub for deep reference.

## Terminology

- **Slowave** is the product. It is a local MCP memory server.
- **Memory** is what Slowave stores. Don't call it a "database" or "store" in prose.
- **Procedure** is a saved method that worked: ordered steps, context and warnings. Procedures are a key feature, so keep them prominent.
- **Agent** or **coding agent** is the tool that uses Slowave. Avoid "client" in prose.
- **Scope** is the project a memory belongs to.
- **Session** is one task from start to finish.
- **Dashboard** is the local web view started with `slowave dashboard`.
- Slowave is not classic RAG, and it is not a search index with an LLM on top. It is a living memory that learns from agent feedback.

## Supported clients and their order

Always list clients in this order: Claude Code, Copilot CLI, Codex, Cursor, OpenCode, Windsurf (Devin Desktop), Cline, Antigravity, Claude Desktop.

## Style preferences

- Use plain, human language. One idea per sentence, around 20 words or fewer.
- Use second person ("you") and active voice.
- Use sentence case for headings.
- Bold for UI elements: Click **Settings**. Code formatting for commands, file names and paths.
- Keep pages short, around 600 words. Use cards, steps, tabs and diagrams over long prose.
- Use coding-related examples. Mark example data as illustrative.
- Every page needs `title`, a `description` of about 150 characters and `sidebarTitle`. Don't add a `#` heading, because the title is the H1.
- Every image needs alt text. Every diagram needs readable text on a phone.
- MDX comments use `{/* */}`.

## Content boundaries

Document:
- What Slowave does, how to install it, connect an agent, back up, restore and uninstall.
- Commands and settings a user needs day to day.

Don't document:
- Internal algorithms, schema IDs, ranking constants or database layout.
- Unreleased features or invented numbers.
- Claims that setup installs hooks. No source supports it.

Always keep these honest caveats visible:
- Slowave is public beta software.
- The local database is plaintext. Protect it with file permissions or disk encryption.
- Benchmarks are preliminary. They measure evidence retrieval, not end-to-end accuracy, and aren't ranked against other systems.
- Slowave makes no LLM calls for its own work, but your agent keeps its own LLM account.
- Copilot CLI support is partly validated.
