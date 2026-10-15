# Check plugins

Check by GOLProductions: before your AI runs a command or writes a file, your own machine checks it, and what it proves wrong is stopped.

| Tool | Package |
|---|---|
| Claude Code | [golproductions/gol-check](https://github.com/golproductions/gol-check) |
| Codex | [plugins/codex](plugins/codex) |
| GitHub Copilot CLI | [plugins/copilot](plugins/copilot) |
| Cursor | [plugins/cursor](plugins/cursor) |
| Gemini CLI | [golproductions/check-gemini](https://github.com/golproductions/check-gemini) (the same files as [plugins/gemini](plugins/gemini)) |

Each package carries the Check client itself, plain readable JavaScript, and downloads nothing. A GOL API Key comes from https://golproductions.com/console (14 days free).

Any other agent, or all of them at once: `npx @golproductions/check@latest --install`. See https://golproductions.com/guide

Proprietary. See https://golproductions.com/terms
