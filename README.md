# Browser Control MCP (Chrome Extension)

**Browser Control MCP** is a Chrome extension that connects AI assistants running on your own computer (such as Claude Code, Antigravity, Gemini CLI, Codex, and other MCP clients) to your real Google Chrome browser through a local Model Context Protocol (MCP) server.

## What it does

When your local MCP server requests an action, the extension can:

- **Work in isolated background tabs:** Opens, switches, and closes tabs inside its own labelled tab group without taking over your other tabs or stealing window focus.
- **Read and interact with pages:** Extracts accessibility trees and readable page text, locates elements, fills forms, uploads files, clicks, types, and scrolls.
- **Record and replay workflows ("Recipes"):** Captures repeatable multi-step flows and replays them with natural pacing, rich text, file uploads, and rate-limit back-off.
- **Capture visuals and diagnostics:** Takes screenshots, records short GIFs, and reads console messages and network requests from agent-controlled tabs for debugging.

## Security & control

- **Local-only connection:** The extension communicates exclusively with a local MCP server on your own machine (`ws://127.0.0.1`). It never contacts any remote server and sends zero telemetry or user data to the developer or third parties.
- **Shared bridge token:** The extension does not open a connection or accept commands until paired with a local bridge token configured in the extension's Options page.
- **Ask-first site permissions:** Chrome Web Store installs default to **Ask me for each new site**, with configurable allowlists, denylists, and per-tool disable switches.
- **Prompt-injection protections:** Page content is marked as untrusted data, and hidden text invisible to human readers is filtered out by default.
- **Visible live controls:** Agent-controlled tabs display a visible border and floating control bar with **Pause**, **Point & note**, **Input Lock** (prevents accidental clicks, keys, or scrolling while an agent runs), and **Stop AI agent**.
- **Protected pages stay off-limits:** Browser settings (`chrome://`), other extensions, and the Chrome Web Store are never scripted.

## Requirements

This extension is a local companion client and does nothing on its own. It requires the Browser Control MCP local server running on your computer.

## Privacy Policy

See [PRIVACY-POLICY.md](./PRIVACY-POLICY.md).

## Support

Questions or issues: open an issue in this repository or email the developer listed on the Chrome Web Store page.
