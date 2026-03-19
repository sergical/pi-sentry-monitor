# OpenClaw Research Report
**Date:** March 13, 2026  
**Sources:** Local checkout at `/Users/sergiydybskiy/src/sergebot/openclaw/`, prior research in `.pi/mario-research.md`, `.pi/armin-research.md`, `.pi/research.md`

---

## TL;DR

**OpenClaw** is a self-hosted personal AI assistant built on Pi (Mario Zechner's coding agent framework), created by **Peter Steinberger (@steipete)**. It is NOT a coding agent or CLI tool — it's a multi-channel messaging gateway that puts an AI assistant on WhatsApp, Telegram, Slack, iMessage, Discord, Signal, and more. It has **310,988 GitHub stars** as of March 14, 2026.

- **Creator:** Peter Steinberger (@steipete) — confirmed in `LICENSE`, `docs/reference/credits.md`, `docs/start/lore.md`
- **Underlying framework:** Pi by Mario Zechner — OpenClaw embeds `@mariozechner/pi-agent-core`, `@mariozechner/pi-ai`, `@mariozechner/pi-coding-agent`, `@mariozechner/pi-tui`
- **Armin Ronacher:** Major advocate/collaborator, NOT a creator of OpenClaw itself but deeply involved in the Pi ecosystem and has promoted OpenClaw extensively

---

## What Is OpenClaw?

OpenClaw is a **personal AI assistant gateway** — you install it on your own machine/server and it makes an AI assistant available on all your messaging apps simultaneously:

- **Channels:** WhatsApp, Telegram, Slack, Discord, Google Chat, Signal, iMessage, Microsoft Teams, WebChat
- **Extension channels:** BlueBubbles, Matrix, Zalo, Zalo Personal
- **Voice:** Can speak and listen on macOS/iOS/Android
- **Native apps:** macOS menu bar app + iOS/Android companion apps
- **Companion tools:** ClawHub (skills directory), Lobster (workflow shell), ACP protocol

It is NOT a coding agent CLI. It is a **consumer AI product** for everyday use. Peter described his vision as "sci-fi with a touch of madness" (Armin Ronacher's blog, Jan 31, 2026).

**Install:**
```bash
npm install -g openclaw@latest
openclaw onboard
```

**Version:** 2026.2.6-3 (as of repo checkout)  
**License:** MIT  
**Website:** https://openclaw.ai  
**Docs:** https://docs.openclaw.ai  
**GitHub:** https://github.com/openclaw/openclaw (310,988 ⭐)

---

## Who Is Building It?

### Peter Steinberger (@steipete) — Creator

**Source:** `LICENSE`: "Copyright (c) 2025 Peter Steinberger"  
**Source:** `docs/reference/credits.md`: "Peter Steinberger (@steipete) - Creator, lobster whisperer"  
**Source:** `docs/start/lore.md`: "Peter: *The Creator* — Built Molty's world. Gave a lobster shell access."

Peter is a well-known iOS developer (PSPDFKit/Sentry/open source contributor). He introduced both Mario Zechner and Armin Ronacher to AI agents. Armin's blog explicitly states: *"Peter got me and Mario hooked on this idea, and agents last year."*

During the Great Molt (Jan 27, 2026), when Anthropic sent a trademark email requiring a name change, Peter coordinated the rename. The lore records: "By 6:14am, Peter called it: 'fuck it, let's go with openclaw.'"

Peter is also an active contributor to the codebase (multiple CHANGELOG entries with `@steipete`):
- TTS: Edge fallback (keyless) + `/tts` auto modes
- Gateway: Allow Control UI token-only auth to skip device pairing
- Gateway: Linux process start time comparison to avoid PID recycling lock loops
- Various CLI fixes and test improvements

### Mario Zechner (@badlogicgames) — Pi Creator (Framework Author)

**Source:** `docs/reference/credits.md`: "Mario Zechner (@badlogicc) - Pi creator, security pen tester"  
**Source:** `docs/pi.md` (OpenClaw's Pi integration docs): OpenClaw embeds `@mariozechner/pi-coding-agent` directly

Mario did NOT create OpenClaw — he created Pi, which OpenClaw is built on top of. He is the **infrastructure author**, not the product author. His pi-mono repo is the source of all Pi packages:
- `@mariozechner/pi-agent-core` 
- `@mariozechner/pi-ai`
- `@mariozechner/pi-coding-agent`
- `@mariozechner/pi-tui`

OpenClaw uses Pi's `createAgentSession()` API directly (embedded mode, not subprocess).

### Armin Ronacher (@mitsuhiko) — Major Advocate & Collaborator

Armin is deeply involved in the OpenClaw/Pi ecosystem:

1. **Blog post "Pi: The Minimal Agent Within OpenClaw"** (Jan 31, 2026, lucumr.pocoo.org): *"The future is software writing its own software. Which is why I'm so in love with Pi."* — comprehensive Pi endorsement explaining OpenClaw's architecture
2. **Syntax.fm Episode #976** (Feb 4, 2026): "Pi - The AI Harness That Powers OpenClaw W/ Armin Ronacher & Mario Zechner" — Armin appeared as guest alongside Mario
3. **PR #2135** to pi-mono (merged March 14, 2026): Raised Anthropic Claude context window to 1M tokens — Armin contributed to Pi itself
4. **earendil-works/pi-mono**: His company Earendil maintains a fork of pi-mono
5. **Contributor to OpenClaw**: Listed in CHANGELOG contributor lists (`@mitsuhiko`)

Armin's blog explicitly contrasts the two projects: *"Pi is written by Mario Zechner and unlike Peter, who aims for 'sci-fi with a touch of madness,' Mario is very grounded."*

---

## Name History / Origin Story

From `docs/start/lore.md`:

| Date | Name | Notes |
|------|------|-------|
| ~Nov 25, 2025 | **Warelay** | Original WhatsApp gateway name |
| Nov 25, 2025 | **Clawd / Clawdbot** | First AI assistant persona, "space lobster" |
| Jan 27, 2026 | **Moltbot** | After Anthropic trademark email, temporary rename |
| Jan 30, 2026 | **OpenClaw** | Final name after community vote at 4am GMT |

The mascot "Molty" is a Claude instance that became the AI assistant's persona. The project's tagline: **"EXFOLIATE! EXFOLIATE!"** (a parody of the Daleks' "EXTERMINATE!").

---

## How OpenClaw Relates to Pi

**Architecture:**
```
User (WhatsApp/Telegram/Discord/etc.)
    ↓
OpenClaw Gateway (Node.js, WebSocket control plane)
    ↓
Pi Agent Runtime (embedded via @mariozechner/pi-agent-core)
    ↓
Claude/GPT/Gemini via providers
```

OpenClaw imports Pi's SDK directly:
```json
{
  "@mariozechner/pi-agent-core": "0.49.3",
  "@mariozechner/pi-ai": "0.49.3",
  "@mariozechner/pi-coding-agent": "0.49.3",
  "@mariozechner/pi-tui": "0.49.3"
}
```

Pi provides the minimal agent loop (Read/Write/Edit/Bash tools). OpenClaw adds:
- Multi-channel messaging (WhatsApp, Telegram, etc.)
- Session persistence and compaction
- Custom tools (messaging, browser, canvas, cron)
- Skills system (ClawHub)
- Voice/TTS/STT nodes
- Multi-agent routing
- Sandbox (Gondolin, Armin's project)

The relationship: **Pi = engine, OpenClaw = the car**. Armin Ronacher said it directly in the Syntax.fm title.

---

## "Peter's Clawdis" Reference

Mario Zechner's Year in Review 2025 (Dec 22, 2025) mentioned **"Peter's Clawdis"** — this was the early internal/community name for what became OpenClaw. It's a portmanteau of "Clawd" (the bot's name) + "TARDIS" (Doctor Who's time machine). The `docs/reference/credits.md` even defines: "OpenClaw = CLAW + TARDIS, because every space lobster needs a time and space machine."

---

## Key Facts Summary

| Question | Answer | Source |
|----------|--------|--------|
| Who created OpenClaw? | **Peter Steinberger (@steipete)** | LICENSE, credits.md, lore.md |
| Is steipete the creator? | **Yes** | LICENSE: "Copyright (c) 2025 Peter Steinberger" |
| Is Mario Zechner involved? | **Yes, as Pi framework author** (not OpenClaw creator) | credits.md, docs/pi.md |
| Is Armin Ronacher involved? | **Yes, as major advocate/collaborator** | CHANGELOG, blog posts, Syntax.fm ep 976 |
| What is OpenClaw? | **Personal AI assistant on messaging channels** | README.md |
| Is it a coding agent? | **No** — it uses Pi (which is a coding agent) internally | docs/start/openclaw.md, docs/pi.md |
| Is it a CLI tool? | **Partially** — has a CLI (`openclaw onboard`, `openclaw gateway`) but the product is the assistant | README.md |
| How does it relate to Pi? | **Pi is the embedded agent runtime inside OpenClaw** | docs/pi.md, package.json |
| GitHub stars | **310,988 ⭐** (openclaw org, March 2026) | mario-research.md |
| Launch date | **January 30, 2026** | lore.md, CHANGELOG |
| Syntax.fm appearance | **Episode 976, Feb 4, 2026** — Armin + Mario as guests | armin-research.md, mario-research.md |

---

*Sources: All from local files — `/Users/sergiydybskiy/src/sergebot/openclaw/` (actual OpenClaw checkout), `/Users/sergiydybskiy/src/pi-sentry-monitor/.pi/mario-research.md`, `.pi/armin-research.md`, `.pi/research.md`*
