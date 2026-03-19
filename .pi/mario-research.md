# Mario Zechner (@badlogicgames) — Research Report
**Period: January–March 2026**  
**Research date: March 13–14, 2026**  
**Sources: mariozechner.at RSS, GitHub API, npm registry, Syntax.fm RSS feed, direct HTTP fetches**

---

## 1. Blog Posts on mariozechner.at (Jan–March 2026)

**NONE.** The last blog post published is from **December 22, 2025**.

| Date | Title | URL |
|------|-------|-----|
| 2025-12-22 | Year in Review 2025 | https://mariozechner.at/posts/2025-12-22-year-in-review-2025/ |
| 2025-11-30 | What I learned building an opinionated and minimal coding agent | https://mariozechner.at/posts/2025-11-30-pi-coding-agent/ |
| 2025-11-22 | Armin is wrong and here's why | https://mariozechner.at/posts/2025-11-22-armin-is-wrong/ |
| 2025-11-02 | What if you don't need MCP at all? | https://mariozechner.at/posts/2025-11-02-what-if-you-dont-need-mcp/ |

No new posts have been published in Jan–March 2026. The RSS feed confirms this — nothing newer than 2025-12-22.

---

## 2. GitHub Activity — pi-mono / pi-coding-agent

### Pi Version History (Jan–March 2026)

Pi shipped **at an extraordinary pace** — 10 major versions plus dozens of patches between Jan 1 and March 14, 2026. All releases on npm `@mariozechner/pi-coding-agent`.

**Latest version: v0.58.0 (March 14, 2026)**

#### Full release timeline (Jan–Mar 2026):

| Date | Version | Headline changes |
|------|---------|-----------------|
| 2026-01-17 | v0.49.0 | Extension API improvements (`pi.setLabel()`, keybinding helpers, `VERSION` export) |
| 2026-01-19 | v0.49.2 | Bug fixes |
| 2026-01-26 | **v0.50.0** | 🚀 **Pi packages** (bundle+install extensions/skills/themes via git/npm), **hot reload** (`/reload`) of all resources, **custom providers** via `pi.registerProvider()`, Azure OpenAI Responses provider |
| 2026-01-29–30 | v0.50.2–0.50.6 | Patch fixes |
| 2026-02-01 | **v0.51.0** | Tool signature breaking change (`signal` param reordered), new session controls |
| 2026-02-01–04 | v0.50.7–v0.51.6 | Rapid patches |
| 2026-02-05 | **v0.52.0** | **Claude Opus 4.6** model support, **GPT-5.3 Codex**, SSH URL for git packages, shell command/env var resolution in `auth.json`, model selector UI improvements |
| 2026-02-07–13 | v0.52.1–v0.52.12 | Patches (7 releases in 2 days on Feb 5!) |
| 2026-02-17 | **v0.53.0** | New features |
| 2026-02-19 | **v0.54.0** | **`.agents/skills` auto-discovery** — Pi now finds skills in `.agents/skills` dirs (cwd, ancestors, `~/.agents/skills`) in addition to `.pi` paths |
| 2026-02-22–23 | v0.54.1–v0.54.2 | Patches |
| 2026-02-24 | **v0.55.0** | 🔄 **Breaking**: Project-first resource precedence (`cwd/.pi` before `~/.pi/agent`). Extension conflict resolution redesigned — all extensions stay loaded, first-registered wins |
| 2026-02-26 | v0.55.1 | Hotfix |
| 2026-02-27 | **v0.55.2** | Dynamic provider unregistration (`pi.unregisterProvider()`), takes effect without `/reload` |
| 2026-02-27 | v0.55.3 | Windows: alt+v for image paste (fixes ctrl+v conflict) |
| 2026-03-02 | **v0.55.4** | **Runtime tool registration** — `pi.registerTool()` now applies immediately without `/reload`; tool `promptSnippet` for system prompt contribution |
| 2026-03-04 | **v0.56.0** | **OpenCode Go provider** (`opencode-go`), `branchSummary.skipPrompt` setting, Gemini 3.1 Flash Lite fallback |
| 2026-03-05 | v0.56.1 | Extension alias resolution fix |
| 2026-03-05 | **v0.56.2** | **GPT-5.4 support** (now default for openai/openai-codex), `treeFilterMode` setting for `/tree` |
| 2026-03-06 | v0.56.3 | `claude-sonnet-4-6` via google-antigravity provider, vim-mode extension support, Shift+Enter/Ctrl+Enter in tmux |
| 2026-03-07 | **v0.57.0** | **`before_provider_request` hook** (intercept/modify provider payloads), non-capturing overlays with explicit focus control, strict LF-only JSONL RPC framing (breaking) |
| 2026-03-07 | **v0.57.1** | **`/tree` branch folding** with Ctrl+←/→ and Alt+←/→, `session_directory` extension event, digit keybindings (0-9) |
| 2026-03-14 | **v0.58.0** | 🔥 **Claude Opus 4.6 + Sonnet 4.6 context window raised to 1M tokens** (up from 200K), extension tool calls execute **in parallel** by default, `GOOGLE_CLOUD_API_KEY` for google-vertex, deterministic session IDs |

### Key Themes in Pi Development (Jan–Mar 2026)

1. **Package system** — Pi can now install extensions from GitHub/npm
2. **Provider ecosystem** — OpenCode Go, Google Vertex API key, GPT-5.4, Codex 5.3, Claude Opus 4.6/Sonnet 4.6 with 1M context
3. **Extension API maturity** — provider interception hooks, dynamic tool/provider registration, parallel tool execution
4. **`/tree` TUI improvements** — branch folding, segment navigation
5. **Windows/tmux compatibility** improvements throughout

### Repository Statistics

- `pi-mono`: **23,387 ⭐** | Updated daily
- `pi-skills`: 801 ⭐
- `agent-tools`: 151 ⭐ — CLI tools for coding agents
- `claude-commands`: 494 ⭐
- `cchistory`: 213 ⭐ — Tracks Claude Code system prompt changes

---

## 3. New Projects Launched in 2026

### 🦞 OpenClaw (January 30, 2026) — THE BIG ONE

**Repo**: https://github.com/openclaw/openclaw  
**Stars**: **310,988 ⭐** (as of March 14, 2026) — this is MASSIVE  
**Description**: "Your own personal AI assistant. Any OS. Any Platform. The lobster way. 🦞"  
**Website**: https://openclaw.ai

OpenClaw is a personal AI assistant built on Pi. It answers you on:
- WhatsApp, Telegram, Slack, Discord, Google Chat, Signal, iMessage, Microsoft Teams, WebChat
- Extension channels: BlueBubbles, Matrix, Zalo, Zalo Personal
- Can speak and listen on macOS/iOS/Android

Mario Zechner has a `badlogic/openclaw` mirror repo but the main project lives at the `openclaw` org:
- `openclaw/openclaw` — 310,988 ⭐ (main app)
- `openclaw/clawhub` — 5,818 ⭐ (skills directory)
- `openclaw/skills` — 2,802 ⭐ (archived skills)
- `openclaw/acpx` — 950 ⭐ (CLI client for ACP protocol)
- `openclaw/lobster` — 819 ⭐ (workflow shell for OpenClaw)
- `openclaw/nix-openclaw` — 538 ⭐
- `openclaw/openclaw-windows-node` — 321 ⭐
- `openclaw/openclaw.ai` — 226 ⭐
- `openclaw/openclaw-ansible` — 500 ⭐

Install: `npm install -g openclaw@latest`  
Auth: Anthropic Claude Pro/Max or OpenAI  
Recommended: Claude Opus 4.5 on Claude Pro/Max

**Context**: Armin Ronacher referred to OpenClaw in the Syntax.fm podcast as what Pi powers. In the Year in Review 2025, Mario mentioned "Peter's Clawdis" (likely an early name/fork), a personal agent living in chat apps. OpenClaw appears to be the full public release of that concept.

### Other New Repos (January 2026)

| Created | Repo | Description | Stars |
|---------|------|-------------|-------|
| Jan 6, 2026 | `pi-doom` | Play DOOM in terminal with pi | 12 |
| Jan 8, 2026 | `clipboard` | Clipboard API (text+image read/write/watch) for macOS/Windows/Linux | 5 |
| Jan 13, 2026 | `jiti` | Runtime TypeScript and ESM support for Node.js (fork) | 3 |
| Jan 19, 2026 | `nazi-radio` | (description not available) | — |
| Jan 22, 2026 | `pi-dosbox` | DOSBox extension for pi — run DOS programs with agent interaction | 7 |
| Jan 24, 2026 | `pi-gitlab-duo` | GitLab Duo provider extension for pi | 7 |
| Jan 30, 2026 | `openclaw` | Mirror of OpenClaw | 5 (main org has 310K) |
| Jan 31, 2026 | `doppelgangers` | Find duplicate PRs through embedding visualization | 43 |
| Mar 13, 2026 | `pi-diff-review` | (description TBD) | 15 |

**pi-doom** details: DOOM runs as WebAssembly (from doomgeneric). Each frame rendered with half-block characters (▀) and 24-bit color. WASM + shareware WAD bundled — no external deps. Works as pi extension (`/doom` command) or standalone.

---

## 4. Syntax.fm Podcast Episode (February 4, 2026) ✅

**Episode**: #976  
**Date**: **Wednesday, February 4, 2026**  
**Title**: "Pi - The AI Harness That Powers OpenClaw W/ Armin Ronacher & Mario Zechner"  
**Hosts**: Wes Bos, Scott Tolinski  
**Guests**: Armin Ronacher (@mitsuhiko) + Mario Zechner (@badlogicgames)  
**Audio**: https://traffic.megaphone.fm/FSI4377406091.mp3  
**URL**: https://syntax.fm/show/976/pi-the-ai-harness-that-powers-openclaw-w-armin-ronacher-and-mario-zechner

### Show Notes Summary:
- **03:28** — What is Pi, and why does it matter? OpenClaw
- **05:54** — What do we actually mean by "agents"?
- **11:04** — Prompt injection: how LLMs get tricked
- **14:19** — Is Claude Code actually secure?
- **22:01** — How Armin and Mario use agents day to day
- **27:25** — Memory and search: teaching agents to remember
- **34:36** — "Bash is all you need"
- **37:21** — Adding power: how agents learn new tricks
- **47:02** — Tools and models Armin and Mario are using right now

**Themes**: Pi as a minimalist harness, OpenClaw as the consumer product built on it, prompt injection risks, why Bash is sufficient (no MCP), agent memory/search, model selection in 2026.

Note: Armin Ronacher appears to be actively involved/invested in OpenClaw based on his involvement with both Pi and OpenClaw, and the `@mitsuhiko` contributor credited in pi-mono PRs (including the 1M context window PR in v0.58.0).

---

## 5. The "Armin is Wrong" Debate (Context from 2025)

**Blog post**: "Armin is wrong and here's why" — November 22, 2025  
**Summary**: Mario pushed back on Armin Ronacher's claim that LLM APIs are secretly a state synchronization problem (due to prefix caching). Mario's counter-argument: the message abstraction IS the underlying reality baked into model weights; prefix caching is an implementation detail you can't control. Mario argued Armin's CRDT/local-first proposals don't address the actual problems practitioners face.

Key quote from Mario: *"He claims LLM APIs are secretly a state synchronization problem because providers support prefix caching and hide state from you, and proposes we look at local-first/CRDT-style solutions."*

Despite the debate, Mario called Armin a friend: *"I consider Armin a friend, so the following is me just rambling at him like I would over a coffee in real life."*

**Resolution**: By February 4, 2026, they were appearing together on Syntax.fm (episode 976). Armin also called Pi "the Hacker's Open Source choice" (quoted in Mario's Year in Review). They're clearly collaborating — Armin appears to be deeply involved with OpenClaw, which is built on Pi.

---

## 6. Twitter/X Activity (@badlogicgames)

Direct Twitter API access not available. Known facts:
- Mario's X handle is @badlogicgames, confirmed in Syntax.fm show notes
- The Year in Review mentions using social media posts to promote Cards for Ukraine
- The "Armin is wrong" blog post refers to an "offending post" from Armin as the trigger
- No direct tweet content available from this research

---

## 7. Recent Blog Posts About Claude Code, Anthropic, AI Agents

All from **2025** (no 2026 posts yet):

| Date | Post |
|------|------|
| 2025-11-30 | "What I learned building an opinionated and minimal coding agent" — core Pi philosophy post |
| 2025-11-22 | "Armin is wrong and here's why" — rebuts Armin's LLM state sync argument |
| 2025-11-02 | "What if you don't need MCP at all?" — advocates for Bash over MCP |
| 2025-08-15 | "MCP vs CLI: Benchmarking Tools for Coding Agents" — data-driven MCP vs CLI comparison |
| 2025-08-06 | "Patching Claude Code for debugging and /cost support for Max users" |
| 2025-08-03 | "cchistory: Tracking Claude Code System Prompt and Tool Changes" |
| 2025-06-02 | "Prompts are code, .json/.md files are state" |

**Mario's core philosophy on Claude Code/AI agents** (from Year in Review):
> "Anthropic kept adding features to Claude Code and would also mess with the toolset and system prompt constantly. This fucked with my workflows and I got more and more annoyed over the months. So I eventually set out to write my own little coding agent that works exactly the way I want it to work. That meant stripping away all the stuff I don't need and that I consider to be an anti-pattern. No MCP support, no built-in sub-agents, no plan mode, no to-do tool. I found that the models are really effective if you give them just a minimal set of tools: read, write, edit, bash."

---

## 8. Heisse Preise — Recent Updates

**Repo**: https://github.com/badlogic/heissepreise  
**Stars**: 1,014 ⭐  
**Website**: https://heisse-preise.io

### 2026 Activity:

| Date | Change |
|------|--------|
| Jan 18, 2026 | Fix default store selection; add Hofer to discontinued list |
| Jan 18, 2026 | Update docs: DM and DM Deutschland added to discontinued stores list |
| Jan 18, 2026 | Fix Billa: update category slugs after Billa API restructure |
| Feb 17, 2026 | Add filter for unavailable products |
| Feb 17, 2026 | Fix Billa: remove storeId parameter that breaks on non-Austrian servers |
| Feb 17, 2026 | Fix: handle out-of-bounds category codes gracefully |

**Context from Year in Review 2025**: SPAR changed their API on Christmas Eve 2024, causing a data gap for SPAR products from Dec 24, 2024 to May 14, 2025. Mario fixed it in May 2025. He continues to advocate for the Austrian government to legalize grocery price scraping. Cory Doctorow referenced him in The Verge as "the kid in Austria" who scraped grocery prices (Mario is 41).

The project still runs. Most stores still active; some (Hofer, DM, DM Deutschland, Lidl as of March 2025) are on a discontinued list.

---

## 9. Other Notable Active Repositories

| Repo | Stars | Description | Recent activity |
|------|-------|-------------|-----------------|
| `lemmy` | 1,484 | Lemmy community something | Updated Mar 13 |
| `cchistory` | 213 | Track Claude Code system prompt/tool changes | Updated Mar 13 |
| `gmcli` | 189 | Minimal Gmail CLI | Updated Mar 13 |
| `agent-tools` | 151 | CLI tools for coding agents | Updated Mar 14 |
| `claude-commands` | 494 | Reusable slash commands for Claude Code | Updated Mar 13 |
| `yakety` | 88 | Voice recording and transcription app | Updated Mar 12 |
| `skyview` | 83 | (unknown) | Updated Feb 28 |
| `terminalcp` | 112 | (unknown) | Updated Mar 5 |
| `genai-workshop` | 93 | GenAI workshop materials | Updated Mar 13 |
| `doppelgangers` | 43 | Find duplicate PRs via embedding visualization | Updated Mar 4 |
| `mini-lit` | 44 | (unknown) | Updated Mar 13 |
| `r96` | 147 | (unknown) | Updated Mar 4 |
| `gccli` | 105 | (unknown — Google Calendar CLI?) | Updated Mar 3 |
| `exa-search` | 2 | Exa search integration | Updated Mar 13 |

### pi-diff-review (March 13, 2026)
A brand new repo (`pi-diff-review`) was created just yesterday (March 13, 2026). Likely a diff/code review extension for Pi.

---

## 10. Summary / TL;DR

### What's been happening with Mario in Jan–March 2026:

1. **No new blog posts** — last one was Dec 22, 2025 (Year in Review)
2. **Pi is shipping insanely fast** — from v0.49 to v0.58 in ~2 months. Latest is v0.58.0 with 1M context for Claude Opus/Sonnet 4.6 and parallel tool execution
3. **OpenClaw is the big new project** — personal AI assistant built on Pi, launched Jan 30, 2026. Has 310K+ stars in the openclaw org. Armin Ronacher is deeply involved. They're building an ecosystem (clawhub for skills, lobster for workflows, ACP protocol, etc.)
4. **Syntax.fm Episode #976 (Feb 4, 2026)** — Mario + Armin appeared on Syntax with Wes Bos & Scott Tolinski talking about Pi and OpenClaw
5. **The "Armin is wrong" drama** (Nov 2025) has resolved into a collaboration — they're building OpenClaw together
6. **Heisse Preise** still active — Jan/Feb 2026 fixes for Billa API, discontinued stores, unavailable product filtering
7. **Fun projects**: pi-doom (DOOM in terminal via pi extension, Jan 6), pi-dosbox (DOSBox extension), doppelgangers (duplicate PR finder)
8. **Pi website**: shittycodingagent.ai (self-deprecating humor) with pi.dev domain donated by exe.dev
9. **Armin Ronacher (`@mitsuhiko`) contributed** the 1M token context window PR (v0.58.0) to pi-mono

---

*Research conducted March 13–14, 2026. Sources: mariozechner.at (direct HTTP), GitHub API (api.github.com), npm registry, Syntax.fm RSS feed (feed.syntax.fm).*
