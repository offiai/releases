# OffiAI releases

OffiAI is a free macOS app (Apple silicon) that shows your AI coding agent sessions as desks in a 3D office. Claude Code CLI, Claude Cowork and Codex CLI sessions each get their own desk, so you can see at a glance which agents are working and on what.

This repository holds the **notarized app builds, the integration packages and the release notes**. It contains no source code: OffiAI is proprietary software, published here as binaries only.

Website: https://offiai.app

## Download

**[Latest release (beta 24, 23 October 2026)](https://github.com/offiai/releases/releases/latest)**

| File | What it is |
|---|---|
| `OffiAI-<version>-arm64-<build>.dmg` | The app. Open the DMG and move OffiAI to Applications. |
| `....dmg.sha256` | SHA-256 checksum of the DMG (`shasum -a 256 -c <file>.sha256`). |
| `offiai.plugin` | Plugin for the Claude desktop app (Cowork). |
| `offiai-codex.zip` | Hooks installer for the Codex CLI. |
| `offiai-antigravity.zip` | Early, read-only Gemini (Antigravity CLI) integration. |

Requirements: a Mac with Apple silicon and a current macOS. The app is notarized by Apple. OffiAI is a public beta: expect rough edges, and check the release notes for what changed in each build.

## What works today

- **Claude Code CLI**: sessions show up at desks on their own, with no plugin and no hooks. Desks show the session status and what it is working on.
- **Reception**: describe a task, pick a folder, and OffiAI starts a Claude Code session at a free desk.
- **Claude Cowork** (Claude desktop app): connects through the OffiAI plugin. Ask Claude to report a conversation and it gets a desk with Claude's progress notes.
- **Codex CLI**: connects through a small hooks installer. Codex desks are view-only: they show the step Codex is on and its latest answer; you reply in Codex itself.
- **Gemini (Antigravity CLI)**: early, read-only.
- No phone app is public yet.

Install guides:

- Claude Code: https://offiai.app/install/claude-code/
- Claude Cowork: https://offiai.app/install/claude-cowork/
- Codex CLI: https://offiai.app/install/codex/

## Privacy

OffiAI is local-first. It reads the session files your agents already keep on your Mac (for example under `~/.claude` and `~/.codex`), and the Cowork plugin and Codex hooks talk to the app over `127.0.0.1` only. OffiAI runs no AI model of its own, has no server that receives your sessions, and does not upload your prompts, transcripts or file contents. It writes to an agent only when you send a message or a brief from OffiAI.

Each install guide has a privacy section with the exact details. Legal privacy policy: https://offiai.app/app-data/

## Licence

Proprietary. Copyright Delicatino GmbH. The builds here are free to download and use; the source code is not published. The Claude plugin's code is visible at https://github.com/offiai/claude-plugins under the same proprietary licence.

## Contact

OffiAI is made by Delicatino GmbH, Bremen, Germany ([legal notice](https://offiai.app/en/legal-notice.html)).

- Bugs and questions: [open an issue](https://github.com/offiai/releases/issues) in this repository.
- E-mail: preview@offiai.app
- Changelog: https://offiai.app/changelog/
