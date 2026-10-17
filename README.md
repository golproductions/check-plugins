# Check plugins

Check by GOLProductions: before your AI acts, your own machine checks the action, and what it proves wrong is stopped. What each tool lets Check see is in its package's README and at https://golproductions.com/guide

| Tool | Package |
|---|---|
| Claude Code | [golproductions/gol-check](https://github.com/golproductions/gol-check) |
| Codex | [plugins/codex](plugins/codex) |
| GitHub Copilot CLI | [plugins/copilot](plugins/copilot) |
| Cursor | [plugins/cursor](plugins/cursor) |
| Gemini CLI | [golproductions/check-gemini](https://github.com/golproductions/check-gemini) (the same files as [plugins/gemini](plugins/gemini)) |

Each package carries the Check client itself, plain readable JavaScript, and downloads nothing. A GOL API Key comes from https://golproductions.com/console (100 free blocks).

Any other agent, or all of them at once: `npx @golproductions/check@latest --install`. See https://golproductions.com/guide

Proprietary. See https://golproductions.com/terms
