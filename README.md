# Seed Round Training Simulator

**An AI-powered VC funding conversation trainer.** You play the founder. Sarah Chen, a seed-stage partner with real constraints, interviews you — and she never tells you what she is actually thinking.

> *"A real VC gives you one attempt. We let you take a hundred."*

---

## What it does

Walk into a simulated first meeting with a US-dollar seed fund. Sarah listens to **what you say** and **how you say it** (voice delivery: pace, filler words, stalls). Behind the scenes she keeps a hidden ledger — conviction, trust, alertness — that moves with every answer, and a debrief reveals it only after the conversation ends.

- **Offline keyword engine** — works with zero setup, no network, no API key
- **LLM integration** (optional) — plug in any OpenAI-compatible model; Sarah genuinely listens and probes what you did not prepare for
- **Voice in & voice out** — speak your answer, hear her reply (TTS + speech recognition)
- **Delivery analytics** — she notices hesitation and filler words, not just content
- **Player growth system** — every run earns XP from how satisfied she is; level up and she holds a *stricter* bar next time
- **Pixel-art scene** — a seed-generated pixel founder and a fixed pixel Sarah, seated across a table in her office

## Quick start

The whole product is a **single HTML file** — no build step, no dependencies, no install.

1. Open `vc-sim/index.html` in a browser (or `vc-sim/演示离线版.html` for the offline demo copy).
2. Fill in your founder identity (or just click **Enter the room**).
3. For the full experience, paste an API key under *Connect a model* — it stays in your browser's localStorage and never touches a server.

### Live demo

- Main: `https://seed-round-simulator.app.workbuddy.host/?sharecode=SE6MRGV37C`
- Demo mode (jumps straight to the negotiation stage): append `&demo=1`, or press `Shift + D` anywhere.

## How it works (architecture)

```
founder input ──► SIGNALS keyword engine (always-on fallback)
              └─► LLM (optional, OpenAI-compatible, streaming JSON)
                       │
                       ▼
              hidden state: conviction / trust / alertness
                       │
        ┌──────────────┴───────────────┐
        ▼                              ▼
   Sarah's reply (typed + TTS)     right-rail meters + mood ring
        │
        ▼
   Debrief: radar chart, turn-by-turn ledger, XP settlement
```

- **Single-file frontend**: HTML + CSS + vanilla JS. No framework, no build.
- **Privacy**: API key and all state live in `localStorage`. Nothing is uploaded.
- **Resilience**: the offline engine is a first-class path, not a fallback stub — the whole game runs with no network.

## Repository layout

```
vc-sim/index.html          # the entire product (single file, ~270 KB)
vc-sim/演示离线版.html      # offline demo copy (byte-identical)
vc-pitch/                  # pitch deck, 3-min script, submission materials
vc-pitch/SUBMIT/           # final submission files (use these)
hackathon-kit/             # hackathon planning templates
```

## Built for

"AI solves a real problem" hackathon — the problem: founders rehearse their pitch on themselves and never learn how a real investor actually *reads* them.
