# Check for Gemini CLI

Check verifies an AI's actions before they run. Your own machine checks them: does the program, file, folder, script, package or image an action names exist, and does the code parse? When the machine proves the action wrong, Check stops it and tells the AI what the machine said, so it can fix it.

In Gemini CLI, Check checks file writes everywhere, and commands on Linux. (On Windows, Gemini CLI's commands aren't checked.)

## Install

```
gemini extensions install https://github.com/golproductions/check-gemini
```

## What it needs

A GOL API Key from https://golproductions.com/console (100 free blocks, then A$0.10 only when Check stops something; no card). Gemini CLI asks for it when you install the extension and keeps it in your system keychain. Or set it once in your own terminal with `npx @golproductions/check@latest --key` (saved in `~/.check/key`). The extension reads only those two places. Your AI is never shown it.

## What it runs

- `check-hook.mjs`, the plugin's only code, runs before each action the tool lets it see, and on each message. It is plain, readable JavaScript. It never downloads or replaces code: updates come as new versions of this plugin.
- It runs read-only checks on your machine: it looks up programs and paths, asks tools such as `git`, `node --check`, `bash -n`, `ruby -c`, `php -l`, `docker image inspect` and PowerShell's parser, and parses files your AI writes. It does not run your command.

## What it sends

To https://triage.golproductions.com: the command your AI is about to run (credential patterns removed), the working folder (username masked), the results of the machine's checks, and, for a file write, the file's name, size and whether it exists (never its contents). For each message, only its identifier, never its text. It never sends your prompts or your files. The server decides; the plugin reports. The server may look up package and image names on public registries (npm, PyPI, Docker Hub and others). Full details: https://golproductions.com/privacy

## If anything fails

Check never blocks because of its own failure: with no key or no network, actions go ahead unchecked and Check says so.

## Licence

Proprietary. See https://golproductions.com/terms
