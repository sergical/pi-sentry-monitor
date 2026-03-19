Research is written to `/Users/sergiydybskiy/src/pi-sentry-monitor/research.md`. Here's the key takeaway:

---

## TL;DR — Restream Studio for Your Hybrid Event

**9 out of 10 things work. One hard blocker kills it as an OBS replacement for your setup.**

### ✅ What Works
| | |
|---|---|
| **Remote guests via browser link** | Yes — exactly like StreamYard. Up to 9 guests on paid plans. Guests join via link, no install needed. |
| **Sony ZV-E10 via USB** | Yes — appears as a UVC device, Chrome picks it up normally. |
| **DJI wireless lavs** | Yes — any OS-recognized audio input works. |
| **Layouts** | Grid, spotlight, side-by-side, drag-and-drop custom layouts with one-click scene switching. |
| **Dynamic guests** | Daniel at 12:40, Mario+Armin at 1:00 — totally smooth, core use case. |
| **Local recording** | ✅ Added Feb 2026 — 4K MP4 + WAV, per-participant local recording, Premiere/FCPX compatible. Professional plan+. |

### ❌ The Dealbreaker
**No projector/monitor output.** Restream Studio is a browser tab — there's zero way to get a clean, UI-free program feed to a second display. Two separate feature requests on their Canny board (filed June and September 2025) are still "under review" with no ETA. The `F` fullscreen key just enlarges the preview within the Studio UI — it's not a clean feed.

For your in-room audience to see remote guests on a projector, **you need OBS**.

### Recommended Setup
```
OBS Studio (local)
├── Fullscreen Projector → projector (zero-latency, no UI chrome)
├── vdo.ninja browser source → remote guests join via link (free, WebRTC)
└── RTMP → Restream relay → YouTube, Twitch, etc.
```

This gives you everything Restream Studio offers for guests, plus OBS's full production power, plus the projector output. Restream is used purely as the multistreaming relay — not Studio mode.