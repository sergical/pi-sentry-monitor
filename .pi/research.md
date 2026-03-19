# Deep Research: Armin Ronacher (@mitsuhiko)
> Pi Day AMA Co-Host Research | Compiled March 13, 2026

---

## TL;DR

Armin Ronacher is **one of Pi's most prominent advocates in the world**, Mario Zechner's **personal friend from Vienna**, the person whose viral blog post (435K views) and tweet put Pi on the map publicly, and a former Sentry architect of 10 years. He gave a talk called "Ubertool MCPs" at a meetup literally named **Claude Code Anonymous** in London. He has a npm package (`mitsupi`) of 14 custom Pi extensions. He calls Pi "the coding agent I use almost exclusively." This is not a casual user — he's practically co-marketing the tool.

---

## 1. His Relationship with Pi & Mario Zechner

### They Are Personal Friends in Vienna

Armin and Mario Zechner are **part of the same Vienna tech social circle**, introduced to agents by a mutual friend "Peter" (Peter Steinberger / @steipete, well-known iOS developer). Armin's blog explicitly says Peter "got me and Mario hooked on this idea, and agents last year."

### The Pi Blog Post — January 31, 2026
**URL:** https://lucumr.pocoo.org/2026/1/31/pi/  
This post went viral (linked to a tweet with **435,400 views**).

Key quotes:
> *"Pi happens to be, at this point, the coding agent that I use almost exclusively. Over the last few weeks I became more and more of a shill for the little agent."*

> *"Pi is written by Mario Zechner and unlike Peter, who aims for 'sci-fi with a touch of madness,' Mario is very grounded."*

> *"Pi itself is written like excellent software. It doesn't flicker, it doesn't consume a lot of memory, it doesn't randomly break, it is very reliable and it is written by someone who takes great care of what goes into the software."*

> *"Pi's entire idea is that if you want the agent to do something that it doesn't do yet, you don't go and download an extension... You ask the agent to extend itself. It celebrates the idea of code writing and running code."*

> *"Sessions in Pi are trees. You can branch and navigate within a session which opens up all kinds of interesting opportunities..."*

### His Pi Journey (Timeline)
| Date | Event |
|------|-------|
| Christmas 2025 | Builds a tank computer game with Pi + Opus, doesn't look at the code |
| Dec 22, 2025 | Names Pi one of three primary tools (Amp/Claude Code/Pi): *"Pi is the Hacker's Open Source choice for me"* |
| Jan 7, 2026 | Tweet: *"Claude Code CLI broken? No problem, just use pi ;)"* |
| Jan 8, 2026 | Demo video: "Building a Computer Game from Scratch With Opus and PI" (30.9K views) |
| Jan 16, 2026 | Shares his `loop.ts` Pi extension publicly |
| Jan 24, 2026 | Live stream building Pi extensions |
| **Jan 31, 2026** | **Pi blog post + viral tweet (435K views) — this is when Pi goes mainstream** |
| Feb 4, 2026 | Syntax.fm #976 with Mario Zechner: *"If you want to listen to two cavemen talk about agents..."* |
| ~Feb/Mar 2026 | Future Weekly #492 (German-language podcast) with Zechner: "die Balkon Muppets" |
| Mar 10, 2026 | "Leaning In To Find Out" @ PyAI San Francisco (latest talk) |

### His Pi Extensions: `mitsupi` npm Package
GitHub: `mitsuhiko/agent-stuff`  
He built and open-sourced **14 Pi extensions** he uses daily:
- `answer.ts` — Interactive TUI for answering questions (the `/answer` you're using right now)
- `go-to-bed.ts` — Late-night safety guard with explicit confirmation **after midnight** 🌙
- `whimsical.ts` — Replaces thinking messages with whimsical phrases
- `notify.ts` — Desktop notifications when agent finishes
- `loop.ts` — Rapid iterative coding loop
- `review.ts`, `todos.ts`, `control.ts`, `files.ts`, `context.ts`, `session-breakdown.ts`, `multi-edit.ts`, `uv.ts`, `prompt-editor.ts`

Also skills: `/commit`, `/sentry`, `/web-browser` (CDP-based), `/github`, `/pi-share`

### The Famous UX Tweet
> *"By far the best feature of @badlogicgames's pi coding agent is that it does not swallow any key inputs when you start typing prior to it being fully ready. Low-key best feature."*

---

## 2. His Talks on AI — Including "Claude Code Anonymous"

### "Ubertool MCPs" @ **Claude Code Anonymous London** — August 11, 2025
🎥 YouTube: https://www.youtube.com/watch?v=TMlPnIEEhPc

"Claude Code Anonymous" is a **real recurring meetup in London**. His talk argues for using code/bash as a superior alternative to traditional MCP tool calling. This is the genesis of his famous anti-MCP stance.

### Full Talk List (2025–2026)
| Talk | Event | Date |
|------|-------|------|
| "Leaning In To Find Out" | PyAI, San Francisco | March 10, 2026 |
| "The Machine and Me" | CASE Conference, Berlin | Jan 14, 2026 |
| "AI Coding" | Slush'd Bratislava | Oct 21, 2025 |
| "How to vibe code to a billion dollars" | Tech Soirée Vienna | Aug 27, 2025 |
| **"Ubertool MCPs"** | **Claude Code Anonymous London** | **Aug 11, 2025** |
| "Agentic Coding" | Online (recorded) | June 30, 2025 |
| "Do Dumb Things" | PyCon Austria | April 7, 2025 |

### Recurring YouTube Series
He co-hosts a recurring YouTube series **"State of Agentic Coding" with Ben** — episode #4 dropped March 11, 2026 (two days ago).

---

## 3. His Work at Sentry

### The Story
- Met co-founder David Cramer on IRC in Django community; they discussed starting a company at a **conference in Russia in 2013** (where Armin also met his wife)
- Joined Sentry officially **late 2014** — his first commit predates his employment
- Worked there for **exactly a decade** — left **March 31, 2025**
- Not a founder technically, but describes himself as *"so close to the founding of a company, yet not quite a founder"*

### What He Built
1. **Vienna engineering office** — grew from 0 to 50 people
2. **Event ingestion system** — scaled from thousands of req/s to **1M+ req/s**
3. **Relay** (getsentry/relay) — Sentry's Rust event proxy; he's **5th largest contributor with 474 commits**, created Jan 2018
4. **Symbolic** (getsentry/symbolic) — Rust symbolication library, created Aug 2017
5. **Milksnake** — Python/cffi tool for embedding Rust in Python wheels
6. **SDKs** — Python, JavaScript, Swift, C++, **game consoles**
7. **Functional Source License (FSL)** — championed Sentry's licensing experiments

### His Departure Post (March 31, 2025)
URL: https://lucumr.pocoo.org/2025/3/31/leaving/
> *"Ten years ago I took a leap into the unknown, today I take another. After a decade of working on Sentry I move on to start something new."*

### Fun Meta-Fact
After leaving, he built **vibe-minisentry** — "a vibecoded Sentry clone with Claude Code" written in Go — basically recreating his decade of work as a weekend AI vibe-coding project.

---

## 4. His AI/LLM Takes — Blog Posts with Specific Quotes

### Evolution Arc: Jan 2025 → Jan 2026

**Jan 30, 2025** — Uses: Open WebUI, `llm` CLI, Ollama, Cursor, ChatGPT Plus
> *"AI makes me significantly more productive... It has become indispensable for me."*

**June 4, 2025** — "AI Changes Everything" (the pivot post)
> *"Do I program any faster? Not really. But it feels like I've gained 30% more time in my day because the machine is doing the work. I alternate between giving it instructions, reading a book, and reviewing the changes."*
> *"If you would have told me even just six months ago that I'd prefer being an engineering lead to a virtual programmer intern over hitting the keys myself, I would not have believed it."*

**June 12, 2025** — "Agentic Coding Recommendations"
> *"I predominantly use Claude Code with the cheaper Max subscription for $100 a month."*  
> *"I exclusively use the cheaper Sonnet model."*  
> *"I disable all permission checks. I have an alias called `claude-yolo` set up."*  
> *"If you can choose your language, I strongly recommend Go for new backend projects."*  
> *"I expect this blog post to age very poorly. The pace of innovation here is insane."*

**September 29, 2025** — "90%"
> *"For the infrastructure component I started at my new company, I'm probably north of 90% AI-written code."*  
> *"In total: about 40,000 lines, including Go, YAML, Pulumi, and some custom SDK glue."*  
> *"I still treat every line as my responsibility, judged as if I wrote it myself. AI doesn't change that."*

**December 22, 2025** — "A Year of Vibes"
> *"2025 was the year I stopped programming the way I did before."*  
> *"Amp feels like the Apple or Porsche of agentic coding tools, Claude Code is the affordable Volkswagen, and Pi is the Hacker's Open Source choice for me."*

**January 14, 2026** — "Porting MiniJinja to Go With an Agent"
> *"Turns out you can just port things now."*  
> *"In total I probably spent around 45 minutes actively with it. It worked for around 3 hours while I was watching, then another 7 hours alone."*  
> *(Ported entire Jinja2 implementation from Rust to Go in 10 hours using 2.2 million tokens)*

**January 18, 2026** — "Agent Psychosis: Are We Going Insane?"
> *"When Peter first got me hooked on Claude, I did not sleep. I spent two months excessively prompting the thing and wasting tokens."*  
> *"Two things are both true to me right now: AI agents are amazing and a huge productivity boost. They are also massive slop machines if you turn off your brain and let go completely."*

**February 9, 2026** — "A Language For Agents"
> *"I'm now routinely reaching for JavaScript in places where I would have used Python. Not because I love it or the ecosystem is better, but because the agent does much better with TypeScript."*  
> *"Many of today's languages were designed with the assumption that punching keys is laborious... The cost of writing code is going down, but understanding what the code does is becoming more important."*

**February 13, 2026** — "The Final Bottleneck"
> *"Historically, writing code was slower than reviewing code."*  
> *"So when more and more people tell me they no longer know what code is in their own codebase, I feel like something is very wrong here."*  
> *"I too am the bottleneck now. But you know what? Two years ago, I too was the bottleneck. I was the bottleneck all along."*

**March 5, 2026** — "AI And The Ship of Theseus" (8 days ago)
> *"When the cost of generating code goes down that much, and we can re-implement it from test suites alone, what does that mean for the future of software?"*  
> *"A court still might rule that all AI-generated code is in the public domain, because there was not enough human input in it."*

### His Consistent Anti-MCP Stance
(July 2025 → Dec 2025 — consistent across 4+ posts)
> *"Try completing a GitHub task with the GitHub MCP, then repeat it with the gh CLI tool. You'll almost certainly find the latter uses context far more efficiently."*  
> *"I've been moving all my MCPs to skills, including the remaining one I still used: the Sentry MCP."*

The December 2025 post "Skills vs Dynamic MCP Loadouts" argues skills (markdown docs) outperform MCP servers — which is directly relevant to how Pi works.

---

## 5. Python-to-Rust Transition

### Timeline
| Year | Event |
|------|-------|
| 2012 | First Rust blog post: "Such a Little Thing: The Semicolon in Rust" |
| 2014 | Deep exploration: "A Fresh Look at Rust", multiple error handling posts |
| 2015 | "Rust for Python Programmers" guide |
| 2017 | Production Rust at Sentry: **Symbolic** (Aug) |
| 2018 | **Relay** created (Jan) — 1M+ req/s event proxy in Rust |
| 2021+ | MiniJinja, insta, similar — personal Rust ecosystem |
| 2025 | Still writing Rust actively; "Rust is probably my favorite language" |

### The "Why" (from 2014 "A Fresh Look at Rust")
> *"Rust is in your face with memory and data. It's very much like C and C++. However unlike C and C++ it feels more like you're programming with Python..."*

He had a "huge hatred" for C++'s complexity (STL, Boost) but needed performance. Rust filled the gap. **He never abandoned Python** — Flask still exists and he maintains it — but Rust is his systems/infra language.

### Key Rust Projects
- **MiniJinja** — Rust reimplementation of Jinja2 (2,509 ★)
- **insta** — Snapshot testing for Rust (2,794 ★) 
- **similar** — High-level diffing library (1,228 ★)
- **better-panic** — Python-inspired panic handler for Rust (439 ★)

### The Rust Community Controversy
**"Seeking Purity"** (Feb 8, 2025):
> *"Rust positions itself as a champion of memory safety... I love Rust: it's probably my favorite language."*  
> *"As with many movements rooted in purity, what starts as a technical pursuit can evolve into something more ideological."*  
> *"Using Rust's unsafe blocks is increasingly frowned upon, despite their intended purpose of enabling low-level optimizations when necessary."*

---

## 6. What He's Building Now

**Earendil** — founded with co-founder Colin, Vienna, PBC (Public Benefit Corporation) structure
- Focus: software and open protocols that "strengthen human agency"
- **>90% AI-written code** in production (40k lines Go/YAML)
- Built a durable workflow execution system ("Absurd") on top of Postgres for agent orchestration
- His Pi agent work feeds directly into Earendil's products
- Founded January 2026; announced: https://lucumr.pocoo.org/2026/1/27/earendil/

---

## 7. Controversial Takes & Debates

### Python Asyncio
His "I don't understand Python's Asyncio" post is legendary — *"I don't understand Python's Asyncio"* from someone who built Flask is devastating to asyncio's credibility. Core devs had to respond publicly.

**"Threads Beat Async/Await"** (Nov 18, 2024):
> *"I'm now convinced that async/await is, in fact, a bad abstraction for most languages, and we should be aiming for something better... that I believe to be threads."*

### Python Packaging
Built **Rye** unilaterally outside PyPA — annoyed official channels but resonated with devs. Now absorbed into Astral's **uv** (which he endorsed). EuroPython 2024 talk "The Catch in Rye" explains the story.

### AI Copyright (March 2026)
> *"Vercel, for instance, happily re-implemented bash with Clankers but got visibly upset when someone re-implemented Next.js in the same way."*  
> *"I personally think all of this is exciting. I'm a strong supporter of putting things in the open with as little license enforcement as possible."*

### AI Criticism from Open Source Community
**"GenAI Criticism and Moral Quandaries"** (June 10, 2025) — directly responds to AI skeptics in Python/OSS:
> *"For me, it's not just 'neutral-to-positive' — it's been astonishingly positive. As I write this, my agent is fixing code in another window for me."*

### Agent Addiction Warning (his nuanced take)
Despite being one of the most prominent AI enthusiasts, he was early to warn about "agent psychosis":
> *"I see people develop parasocial relationships with their AIs, get heavily addicted to it, and create communities where people reinforce highly unhealthy behavior."*  
> *"In His Dark Materials, every human has a dæmon... I'm starting to relate our relationship with agents that have memory to those little creatures."*

---

## 8. Surprising Personal Facts

1. **Flask was an April Fool's joke** — Released April 1, 2010 as a gag ("world's simplest web framework"). The design was so good people immediately demanded it become real. He was ~20-21 years old.

2. **He's young** — Born ~1989. Built foundational Python infrastructure as a **teenager in Austria**. The Python web ecosystem was partly architected by a kid in Vienna.

3. **He met his wife at the Russia conference in 2013** — the same conference where he met David Cramer and discussed founding Sentry. One trip, two life-changing meetings.

4. **Father of three** — His @mitsuhiko bio says "Husband and father of 3."

5. **His bio says "more nuanced in person"** — Self-aware about his blunt online persona.

6. **The `go-to-bed.ts` extension** — He built a Pi extension that refuses to let the agent do anything after midnight without explicit confirmation. He codes so much that he needed to code himself a bedtime.

7. **He wrote a blog post authored entirely by Claude** — "Advent of Slop: A Guest Post by Claude" (Dec 23, 2025) where he handed his blog to Claude to write about solving Advent of Code 2025.

8. **The Pocoo Collective** — As a teenager he was part of a small Austrian/German developer group (Georg Brandl, etc.) that collectively produced an extraordinary amount of Python infrastructure (Sphinx, Jinja2, Flask, Werkzeug). The whole group was tiny and mostly Austrian.

9. **He speaks English flawlessly** with no apparent accent in written form, despite German being his native language.

10. **His Christmas 2025** — He spent it building a tank computer game with Pi + Opus "without looking at the code." His family must be very understanding.

---

## 9. The Vienna Connection (Armin + Mario)

Both Armin and Mario are **Austrian developers based in Vienna/Graz area**. Their friendship predates Pi. The shared context:
- Armin: Creator of Flask, spent decade at Sentry, now Earendil
- Mario: Creator of libGDX (Java game framework), creator of Pi
- Peter Steinberger (@steipete): iOS developer, mutual friend who introduced both to AI agents
- All three are in the Austrian developer community

This explains why Pi has Sentry integration (Armin's `/sentry` skill), why Pi is built "like excellent software" according to Armin, and why you're reading this using Pi to monitor Sentry.

---

## 10. Key Quotes for the AMA

**On Pi specifically:**
> *"The future is software writing its own software. Which is why I'm so in love with Pi: a coding agent that can extend itself :)"* (435K views)

**On the current moment:**
> *"Never before have I seen a technology surface in everyday life so quickly, so widely. Smartphones adoption felt slow in comparison."*

**On his workflow:**
> *"I can go make a coffee, and progress still happens."*

**Self-aware on addiction:**
> *"When Peter first got me hooked on Claude, I did not sleep. I spent two months excessively prompting the thing and wasting tokens."*

**His famous YOLO mode:**
> *"I have an alias called `claude-yolo` set up."*

**On staying accountable with AI:**
> *"I still treat every line as my responsibility, judged as if I wrote it myself. AI doesn't change that."*

---

## Sources

- https://lucumr.pocoo.org/ — Full blog
- https://lucumr.pocoo.org/2026/1/31/pi/ — The Pi post
- https://x.com/mitsuhiko — Twitter/X
- https://x.com/mitsuhiko/status/2017604638137012335 — Viral Pi tweet
- https://github.com/mitsuhiko/agent-stuff — Pi extensions (mitsupi npm)
- https://syntax.fm/show/976/pi-the-ai-harness-that-powers-openclaw-w-armin-ronacher-and-mario-zechner
- https://www.youtube.com/watch?v=TMlPnIEEhPc — Claude Code Anonymous talk
- https://lucumr.pocoo.org/2025/3/31/leaving/ — Leaving Sentry
- https://lucumr.pocoo.org/2026/1/27/earendil/ — Earendil announcement
