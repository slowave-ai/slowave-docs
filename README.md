# Slowave docs

Documentation for [Slowave](https://github.com/slowave-ai/slowave): local, persistent memory for AI coding agents (Claude Code, Copilot CLI, Codex, Cursor, OpenCode, Windsurf, Cline and Claude Desktop).

The site is built with [Mintlify](https://mintlify.com). Pushes to `main` deploy automatically.

## Preview locally

```bash
npx mint dev          # http://localhost:3000
npx mint validate
npx mint broken-links
```

Run `git pull` before you edit. Changes made in the Mintlify web editor are committed to this repo.

## How the docs are organized

- Pages are `.mdx` files with frontmatter. The frontmatter `title` is the page heading.
- Navigation, theme and redirects live in `docs.json`.
- Images are in `images/`. Diagrams are plain SVG in `images/diagrams/`.
- Writing rules are in [AGENTS.md](AGENTS.md).

## Contribute

Fixes and clarifications are welcome. Open an issue or a pull request. Run both checks above first.
