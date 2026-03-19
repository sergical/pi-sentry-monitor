# Armin Ronacher (@mitsuhiko) — Activity Research: January–March 2026

> Researched: March 13, 2026  
> Sources: lucumr.pocoo.org (Atom feed + pages), hachyderm.io (Mastodon RSS), GitHub API, Syntax.fm RSS, earendil.com, mariozechner.at

---

## 1. Blog Posts on lucumr.pocoo.org (Jan–March 2026)

Seven posts published in this window:

| Date | Title | URL |
|------|-------|-----|
| **Jan 14, 2026** | Porting MiniJinja to Go With an Agent | /2026/1/14/minijinja-go-port/ |
| **Jan 18, 2026** | Agent Psychosis: Are We Going Insane? | /2026/1/18/agent-psychosis/ |
| **Jan 27, 2026** | Colin and Earendil | /2026/1/27/earendil/ |
| **Jan 31, 2026** | Pi: The Minimal Agent Within OpenClaw | /2026/1/31/pi/ |
| **Feb 09, 2026** | A Language For Agents | /2026/2/9/a-language-for-agents/ |
| **Feb 13, 2026** | The Final Bottleneck | /2026/2/13/the-final-bottleneck/ |
| **Mar 05, 2026** | AI And The Ship of Theseus | /2026/3/5/theseus/ |

### Summaries

**Jan 14 — "Porting MiniJinja to Go With an Agent"**  
Armin used an agent (Pi, starting with Opus 4.5 then switching to GPT-5.2 Codex) to port MiniJinja (his Rust Jinja2 template engine) to native Go. He spent ~45 minutes guiding it; the agent worked ~3 hours while he watched, then 7 hours autonomously. The Go port passes the full Rust test suite.

**Jan 18 — "Agent Psychosis: Are We Going Insane?"**  
Explores the overwhelming flood of AI-generated PRs hitting open source projects. References Steve Yegge's "Gas Town" metaphor. Argues that agentic productivity is outpacing maintainers' ability to review and merge, creating unsustainable queues (OpenClaw: 2,500+ open PRs).

**Jan 27 — "Colin and Earendil"**  
Personal announcement of founding Earendil Inc. with Colin Daymond Hanna, a Vienna-based PBC (Public Benefit Corporation). Charter: "Craft software and open protocols, strengthen human agency, bridge division and ignorance, cultivate lasting joy and understanding."

**Jan 31 — "Pi: The Minimal Agent Within OpenClaw"**  
Armin's major endorsement of Mario Zechner's Pi coding agent. Explains Pi's philosophy: minimal core (4 tools: Read, Write, Edit, Bash), short system prompt, powerful extension system. Describes his own extensions, how Pi powers OpenClaw, and why its architecture (code writing and running code) is the future.

**Feb 9 — "A Language For Agents"**  
Argues that new programming languages will emerge designed specifically for agentic coding. Explores what properties such a language would need: minimal boilerplate, excellent tooling, agent-trainable patterns. Changed his earlier view that existing language corpus would cement them in place.

**Feb 13 — "The Final Bottleneck"**  
Reflects on code review becoming the new bottleneck as AI writes code faster than humans can review it. Draws analogy to the Industrial Revolution's textile machinery chains. Notes Pi's approach (throttle inflow, auto-close PRs from untrusted contributors) as one solution. Linked to: [Mario's tweet about Pi OSS vacations](https://x.com/badlogicgames/status/2021164603506368693) and Steve Yegge's "AI Vampire" post.

**Mar 5 — "AI And The Ship of Theseus"** *(the GPL/AI reimplementation post)*  
See Section 2 below.

---

## 2. GPL/AI Reimplementation Post

**Title:** AI And The Ship of Theseus  
**Date:** March 5, 2026  
**URL:** https://lucumr.pocoo.org/2026/3/5/theseus/

**Context:** Triggered by the [chardet GitHub controversy](https://github.com/chardet/chardet/issues/327) where maintainer @benoit-pierre reimplemented chardet from scratch using an AI agent (only using the API and test suite), then released it as MIT to escape the LGPL license. Original author Mark Pilgrim objected, claiming it is a derived work.

**Armin's position:** He supports the reimplementation, arguing it is a legitimate clean-room implementation. Key points:
- "I personally have a horse in the race because I too wanted chardet to be under a non-GPL license for many years."
- He has been planning clean-room AI-assisted reimplementations of other GPL libraries (started one for readline).
- Copyleft enforcement depends on copyright and friction — both are eroded when an agent can rewrite from test suites alone.
- References Vercel's "just-bash.dev" reimplementation of bash, and how Vercel got upset when Next.js was reimplemented the same way.
- Courts may even rule AI-generated code is public domain (insufficient human authorship).
- Concludes: copyleft licenses may need to lean on trademarks rather than license enforcement.
- Term used: "slopforks" for AI-assisted relicensing rewrites.

**Mastodon post (Mar 5, 2026):** "chardet was vipeforked to MIT and I have thoughts about it. Spoiler: I like it."

---

## 3. Mastodon Posts @mitsuhiko@hachyderm.io (Jan–March 2026)

(Armin cross-posts to X/@mitsuhiko; Mastodon is confirmed active. Direct X scraping not available.)

| Date | Content |
|------|---------|
| **Jan 14** | Summary of MiniJinja Go port experience, links to blog post. References narrated coding session video. |
| **Jan 15** | Ukraine war commentary: "I don't think the situation in Ukraine has been this dire since the beginning of the war" |
| **Jan 16** | Follow-up: "All the messaging around this issue right now is really, really bad." |
| **Jan 18** | Agent Psychosis post: "Weekend thoughts on Gas Town, Beads, slop AI browsers, and AI-generated PRs flooding overwhelmed maintainers." |
| **Jan 25** | Demo of his shitty todos extension for Pi (modeled after Claude Code's task system with UI integration). YouTube video linked: youtu.be/uP... |
| **Jan 26** | "MiniJinja is now available with Go. It's all Codex and Opus built, but it passes the Rust tests and comes with docs and examples." (github.com/mitsuhiko/minijinja/tree/main/minijinja-go) |
| **Jan 27** | Earendil company announcement: links to Colin and Earendil post |
| **Jan 31** | "The future is software writing its own software. Which is why I'm so in love with Pi: a coding agent that can extend itself :)" |
| **Feb 5** | "An agent now builds a 200,000 lines of code C compiler from scratch that can compile the Linux kernel. In two weeks." |
| **Feb 6** | Links to dark.ronacher.eu/2026/2/6/war-in-numbers/ ("Cold Numbers: Some numbers against the backdrop of a war against civilization") |
| **Feb 7** | Re: viral tweet "Nearly every ambitious person I know who has dived into AI is working harder than ever." Response: "I'm in this Tweet." |
| **Feb 7** | "If you wanna critique our Gondolin sandbox approach, I wrote some docs for the security architecture and networking stack: earendil-works.github.io/gondolin/security/" |
| **Feb 9** | "This weekend I was thinking about programming languages. Programming languages for agents. Will we see them?" |
| **Feb 13** | "Today Thorsten Ball said he's the bottleneck. I too am the bottleneck and it made me think." Links to The Final Bottleneck post. |
| **Mar 5** | chardet/theseus post: "chardet was vipeforked to MIT and I have thoughts about it. Spoiler: I like it." |

---

## 4. Earendil Project — Recent Updates

### The Company

**Earendil Inc.** (earendil.com) — announced publicly January 27, 2026  
- Co-founders: **Armin Ronacher** + **Colin Daymond Hanna**  
- Structure: Public Benefit Corporation (PBC)  
- Location: Vienna, Austria  
- Mission: "Craft software and open protocols, strengthen human agency, bridge division and ignorance, cultivate lasting joy and understanding."

### Earendil Blog Posts (earendil.com/posts/)

| Date | Title |
|------|-------|
| **Jan 18, 2026** | An Invitation to Begin a Correspondence |
| **Feb 12, 2026** | The High Ground |

### earendil-works GitHub Organization

Repos active Jan–March 2026:

| Repo | Created | Stars | Description |
|------|---------|-------|-------------|
| **gondolin** | Feb 3, 2026 | **756** | Experimental Linux microvm setup with TypeScript Control Plane as Agent Sandbox |
| **absurd** | active | — | An experiment in durability |
| **pi-mono** | active | — | Fork of badlogic/pi-mono |
| **waves** | Jan 24, 2026 | — | (no description) |
| **website** | active | — | earendil.com site |

### Gondolin — Primary Technical Project

**gondolin** is Earendil's main open-source project: a Linux microVM sandbox for running AI agent code safely. Armin is the primary committer.

**Release timeline (Jan–March 2026):**

| Version | Date | Notable Changes |
|---------|------|----------------|
| v0.1.0–v0.1.3 | Early Feb | Initial releases |
| **v0.2.0–v0.2.1** | ~Feb 10 | First open-source release |
| **v0.3.0** | mid-Feb | — |
| **v0.4.0** | Feb 18, 2026 | — |
| **v0.5.0** | Feb 19, 2026 | Snapshot command, bash --resume, rootfs modes |
| **v0.6.0** | Mar 1, 2026 | Tagged builds, TCP support, OCI containers |
| **Post-0.6.0** | Mar 2–10 | Libkrun support (Mar 6), TCP fixes, build improvements |

**Key features built by Armin (Feb–Mar 2026):**
- Experimental libkrun support (Mar 6)
- Mapped TCP Support (Feb 28)
- OCI container support (Feb 22)
- VFS improvements and caching
- Snapshot and resume functionality
- CI/CD pipeline and image releases

**First commit:** Feb 10, 2026 ("feat(build): bake default env into custom images")

---

## 5. Pi Extensions / Contributions

Armin is one of Pi's most vocal advocates and active external contributors.

### pi-codemode-mcp (NEW REPO)
- **Created:** February 22, 2026
- **URL:** https://github.com/mitsuhiko/pi-codemode-mcp
- **Description:** "An experimental way to connect MCPs to Pi using Code"
- **What it does:** Pi extension exposing two tools: `list_mcp_tools` (enumerates MCP tools) and `call_mcp` (runs JavaScript in a sandbox calling MCP servers). Also adds `/mcp` command for status, enable/disable, reconnect, and auth setup.
- **Finding:** Armin concluded MCP composition via code doesn't add much efficiency at this stage; more useful is an MCP server that uses code internally (e.g., his google-workspace-mcp example).

### pi-mono Fork
- **mitsuhiko/pi-mono** — fork of badlogic/pi-mono, created Dec 8, 2025, actively updated through March 2026.

### PR to badlogic/pi-mono
- **PR #2135** — "Raise SOTA anthropic context length to 1M"  
  Submitted: March 13, 2026 | Merged: **March 14, 2026**  
  Updated context window limits for Anthropic models.

### Blog Post Advocacy
- **Jan 31, 2026:** "Pi: The Minimal Agent Within OpenClaw" — comprehensive Pi endorsement, explains Pi's architecture, extensions, and why it's the future of coding agents. Describes his own custom extensions including a Telegram bot.

### Custom Extensions (mentioned in blog)
- Personal Telegram bot built on Pi SDK
- Todos extension for Pi (demoed Jan 25 on Mastodon)

---

## 6. Collaboration with Mario Zechner (@badlogicgames)

### Syntax.fm Episode 976 — **February 4, 2026**

**Title:** "Pi - The AI Harness That Powers OpenClaw W/ Armin Ronacher & Mario Zechner"  
**Published:** Wednesday, February 4, 2026  
**Hosts:** Wes Bos & Scott Tolinski  
**Guests:** Armin Ronacher + Mario Zechner  
**URL:** https://syntax.fm (Episode 976)

**Show notes outline:**
- 00:00 Welcome to Syntax!
- 03:28 What is Pi, and why does it matter? / OpenClaw
- 05:54 What do we actually mean by "agents"?
- 11:04 Prompt injection: how LLMs get tricked
- 14:19 Is Claude Cowork actually secure?
- 22:01 How Armin and Mario use agents day to day
- 26:37 Sponsored by Sentry.io
- 27:25 Memory and search: teaching agents to remember
- 33:04 Do coding agents even need memory?
- 34:36 "Bash is all you need"
- 37:21 Adding power: how agents learn new tricks
- 47:02 Tools and models Armin and Mario are using right now
- 54:15 Sick picks + shameless plugs
  - **Mario's pick:** Cards for Ukraine
  - **Armin's pick:** Pro-Ject Audio Turntable
  - **Armin's plugs:** Thorsten Ball Newsletter, Simon Willison

### Other Collaboration Points
- Armin's "The Final Bottleneck" (Feb 13) explicitly links to [Mario's tweet about Pi OSS vacation policy](https://x.com/badlogicgames/status/2021164603506368693)
- Armin's Pi blog post (Jan 31) prominently features Mario: "Pi is written by Mario Zechner... Despite the differences in approach, both OpenClaw and Pi follow the same idea: LLMs are really good at writing and running code, so embrace this."
- earendil-works maintains its own **pi-mono fork** (earendil-works/pi-mono, created Feb 20, 2026)
- Armin frequently references Mario's work in talks and blog posts

### Pre-2026 Context: "Armin is Wrong" Debate
Mario's Nov 22, 2025 blog post: **"Armin is wrong and here's why"** (mariozechner.at)  
A friendly technical debate about Armin's claim that LLM APIs are secretly a state-synchronization problem (prefix caching hides state). Mario argued the message abstraction is baked into model weights, not hiding a simpler underlying reality. Mario concluded "I consider Armin a friend, so the following is me just rambling at him like I would over a coffee in real life."

---

## 7. Notable Debates and Controversies in 2026

### The chardet GPL Relicensing Controversy (March 2026)
**The issue:** chardet maintainer (who maintained the project for 12 years) used an AI agent to rewrite chardet from scratch — using only the public API and test suite — and released it as MIT, bypassing the LGPL license. Original author **Mark Pilgrim** opened [GitHub issue #327](https://github.com/chardet/chardet/issues/327) on March 4, 2026, arguing this is an illegal derived work.

**Armin's involvement:** 
- Commented extensively on the GitHub issue on **March 5, 2026** (5 separate comments)
- Defended the reimplementation as a legitimate clean-room implementation
- "So far at least it looks to me that this is a clean room implementation that neither shares algorithm nor code with the existing implementation."
- "I for one really appreciate you doing this. I was hoping for a license change for many years."
- Blogged about it the same day in "AI And The Ship of Theseus"

**Why notable:** Combines two heated topics — AI and software licensing — in a high-profile open source project. The issue had 244 comments as of March 13, 2026.

### Broader "Slopfork" Debate
Armin coined / popularized the term **"slopfork"** in the Ship of Theseus post for AI-assisted rewrites of copyleft software to permissive licenses. This triggered broader HN and tech-Twitter discussion about:
- Whether copyleft can survive in an AI-assisted world
- Vercel's contradictory position (reimplemented bash, got upset about Next.js reimplementation)
- Whether AI-generated code can even be copyrighted

### The OpenClaw/Pi PR Flood Problem
Armin's "Agent Psychosis" (Jan 18) and "The Final Bottleneck" (Feb 13) posts contributed to a broader industry conversation about AI-generated PR floods overwhelming open source maintainers. OpenClaw had 2,500+ open PRs. Steve Yegge's "AI Vampire" post was cross-referenced.

---

## Secondary Blog — dark.ronacher.eu

Armin maintains a second, more personal/political blog:

| Date | Title | Note |
|------|-------|------|
| Jan 11, 2026 | "I Have Thus I Deserve" | On startup conditions and merit |
| **Feb 6, 2026** | "Cold Numbers" | Ukraine war statistics ("numbers against the backdrop of a war against civilization") |

He has been vocal about the Ukraine war throughout January–February 2026 (Mastodon posts Jan 15–16, Feb 6).

---

## GitHub Activity Summary (Jan–March 2026)

Most active repos:

| Repo | Role | Activity |
|------|------|----------|
| **earendil-works/gondolin** | Primary author | 60+ commits, v0.1–v0.6, 756 stars |
| **mitsuhiko/insta** | Maintainer | Updated Mar 14 |
| **mitsuhiko/minijinja** | Maintainer | Updated Mar 13 (Go port merged) |
| **mitsuhiko/pi-codemode-mcp** | Author | Created Feb 22 |
| **mitsuhiko/agent-stuff** | Author | Updated Mar 14 |
| **badlogic/pi-mono** | Contributor | PR #2135 merged Mar 14 |
| **chardet/chardet** | Commenter | 5 comments on issue #327, Mar 5 |
| **earendil-works/gondolin** | Author | Active |

---

## Key People Referenced

- **Colin Daymond Hanna** — Earendil co-founder, from San Francisco, now Vienna
- **Mario Zechner** (@badlogicgames) — Pi author, close collaborator, Syntax.fm co-guest
- **Peter** (unnamed) — friend who created OpenClaw, "sci-fi with a touch of madness"
- **Mark Pilgrim** — original chardet author, objected to AI reimplementation
- **Thorsten Ball** — referenced in Final Bottleneck ("I too am the bottleneck")
- **Steve Yegge** — "AI Vampire" post referenced; "Gas Town" metaphor
