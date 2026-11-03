# Walkthrough Video Script — 9 min 30 sec

> **Format**: screen recording (slides + live product, cut between them). Picture-in-picture optional.  
> **Pace**: measured, about 150 words per minute. Total 9:30, leaving 30 seconds of headroom under 10 minutes.  
> **Before recording**: open the product in a browser, paste a working API key, start a fresh game and leave it on the setup screen.

---

## [0:00 – 0:40] Opening · Slide 1 (cover)

> On screen: cover slide

"Hi, I'm (your name), and this is my project: Seed Round Simulator.

In one line: **it lets business school students lose the fundraising conversation a hundred times before they have it for real.**

It's a browser-based conversation trainer. The student plays the founder and talks to an AI venture capitalist who carries a real set of constraints. And the reason this matters is simple — a real fundraising conversation gives you exactly one attempt."

---

## [0:40 – 2:10] The problem · Slides 3, 4, 5

> On screen: slide 3 (section), slide 4 (giant number), slide 5 (three approaches)

"Let me start with the problem.

In the classroom we teach the knowledge of fundraising — how to build a valuation model, how to read a term sheet, how to write a business plan. Students can memorise all of it and score well.

But the moment that decides the outcome isn't knowledge. It's response. The follow-up question you didn't expect, the number you can't recall, the second her tone goes cold. There's no model answer, and there's no second attempt.

So why can't you practise response? Because every existing option is missing the same component.

Books and lectures give you input, but no opponent. You never learn how your answer sounds on the other side of the table.

Studying success stories: the ending is known, so you learn how someone else answered, not how you should.

Mock interviews: the script is fixed. By the third run you're reciting, not responding.

What all three lack is the same thing — **repeated practice with feedback.** You need an opponent who shifts, and a coach who tells you that her last line was just politeness."

---

## [2:10 – 3:10] What it is · Slides 6, 7

> On screen: slide 6 (section), slide 7 (interface mock)

"So our approach is to **reproduce the VC's decision structure** and turn it into an opponent you can practise against.

The investor is Sarah Chen, a partner at a US-dollar seed fund. Behind her sits a ledger the student can't see — interest, trust, alertness, and three red lines she never states: at least eight percent ownership, pro-rata, and information rights.

None of these numbers are visible. The student has only her tone, the depth of her questions, and how long her answers are.

And her posture works in tiers. At a low score she wraps up politely. Once the score climbs, she starts offering resources — introducing you to a portfolio company, for example.

The same sentence gets a completely different response at 30 versus at 80. Which means memorising a script doesn't survive."

---

## [3:10 – 4:10] Two AI features · Slides 8, 9

> On screen: slide 8 (the new feature)
> This is the surprise-feature moment. Give it room, do not rush it.

"One more thing, and it is the part I am proudest of.

Before she ever speaks, she works out who you are.

(gesture at the left column) The founder writes a few lines about himself. Not a dropdown. Free text. 'I am a solo founder. Eight years as a nurse before this, I cannot code. I found this problem on the ward.'

The model reads that and infers what it actually implies: what it buys him, what she will suspect, and what she will press him on. It decides he is a solo non-technical insider, so it presses him on who builds it, and it goes easy on problem insight.

And then her first question changes. A solo non-technical founder gets: 'You are on your own, then. Who is actually building this?' A second-time founder gets: 'You have done this before. So why this, and why now?' An engineer gets: 'You can build it. Who is going to sell it?'

Same product. Three founders. Three completely different interviews. That is what happens when the AI actually understands who it is talking to.

(slide 9) The second one is the other half of the same idea.

Fundraising is spoken. So the student answers out loud, and we do not stop at the transcript - we measure how it sounded. Pace, stalls, filler words, how long he took.

Take one stuttering answer: 'Um, so, like, you know, the retention is, um, sort of fine.' Typed, that answer scores eleven. Spoken, it scores two. Same words. The typing deleted the doubt, and the doubt is exactly what a listener hears.

Speech-to-text on its own would just be a faster keyboard. What she scores is the delivery. And that is the skill a business student actually needs."

---

## [4:10 – 5:00] Live demo · cut to the browser

> Action: switch to the product → start a new round → **click through 3–4 turns quickly** (2–3 seconds each) → point at the side panel changing  
> Note: rehearse this segment twice beforehand. If recording stalls, skip it — the talk still works without it

"Let me show you.

(switch to the product, start a new game)

This is stage one, Cold Start — you have 30 minutes, she arrives two minutes late, and she hasn't opened your deck yet.

(click through a few turns)

Notice the panel on the right: interest, trust, and the questions she's **still waiting on you to answer.** Leave those unanswered and they accumulate — and she remembers.

(by stage three) This is diligence-style questioning. It's noticeably harder, because her interest was pushed up by your earlier answers, so the questions get sharper and more specific."

---

## [5:00 – 6:30] The subtext reveal · back to slide 11, then the debrief screen

> On screen: slide 9 → cut to the product debrief page  
> This is the most important segment in the video. Slow down.

"Now the part I think matters most.

Real investors don't tell you the real reason they're passing. They use presentable excuses. When she says 'we're still getting smart on this space', what it usually means is — it's an excuse, and if I believed in you I'd learn it myself. When she says 'I want to see more traction', it usually means 'I doubt this team can execute'.

(cut to the debrief screen)

When the round ends, the simulator puts both columns side by side: **what she said**, and **what she actually thought.**

(point at the entries)

Look at this one. The student answered 'we're still reconciling that internally, I can't share it right now'. She didn't say anything harsh. But what she actually thought was: 'he's hiding something, I have to assume the most conservative case.'

And here's the line that matters more — the system also gives **the answer that would have worked**: how to respond to the same question properly. Then it closes with 'three things to practise before the next meeting'.

One thing I want to stress: **no real VC will ever show you this.** This is the feedback that the real situation structurally cannot provide."

---

## [6:30 – 8:00] How AI is used · Slide 12

> On screen: slide 10

"Now, what the AI actually does here. This isn't a chat box bolted on. The model has to hold three roles at once, and the product doesn't work if any one of them is missing.

**First, play an opponent whose posture shifts.** Her replies are driven by hidden numbers, not a fixed script. The same question, answered well or badly, produces a completely different follow-up. A rule-based bot can't hold a stateful conversation like that, and a human can't run it a hundred times.

**Second, judge every single answer.** The model reads the student's sentence for signal — concrete numbers score up, admitting a weakness scores up; vague giant markets, defensiveness, overpromising score down — then emits a state delta that decides whether she warms or cools. That's natural-language understanding with structured output.

**Third, coach in the debrief.** After the round, the model explains what each of its own lines actually meant, and gives the answer the student could have given instead.

All three have to happen in a single call, or the conversation stops being coherent."

---

## [8:00 – 8:55] Build evidence · Slides 13, 16

> On screen: slide 11 → slide 14

"Finally, the build.

Three deliberate trade-offs. First, a **single-file web page** — double-click and it runs. No build step, no dependencies, no server. On demo day any one broken link takes the whole thing down. Second, **model access uses the user's own API key**, stored only in local storage: zero cost, and any model they like. Third, **three-tier fallback** — if the model is unavailable it drops to the offline engine, so the conversation never breaks.

What's done: the full four-stage flow, the hidden state machine and three red lines, the subtext reveal and turn-by-turn debrief, and the model integration with fallback.

I also wrote seven automated test suites, including 300 randomised runs, 16 edge-case inputs, and 15 injected failure modes. All passing. That's my basis for saying it runs reliably."

---

## [8:55 – 9:35] Closing · Slide 17

> On screen: slide 15

"To sum up.

This isn't positioned as 'a chatbot'. It's **a practice ground**. What it teaches isn't a script — it's reading the person across the table.

We're not yet a real VC's instinct and industry intuition, and I won't pretend otherwise. But it solves something a real VC structurally cannot: **a real VC gives you one attempt. We let you take a hundred.**

Next: expand the topic library from 16 to over 50, add a second investor with a different style, and bring practising VCs in to calibrate the question framework.

Thank you."

---

## Recording checklist

- [ ] Before recording: product open, API key entered, **network working**, browser zoom at 100%
- [ ] Close unrelated windows, notifications, and taskbar icons
- [ ] Microphone test: record 10 seconds and play back — no hum, no echo
- [ ] Rehearse the demo segment (3:20–4:50) twice so you don't misclick
- [ ] If the model connection fails mid-recording, skip the demo segment — **never debug on camera**
- [ ] Export: MP4, 1080p, filename `Seed_Round_Simulator_Demo.mp4`
- [ ] Check the final duration lands between 7 and 10 minutes

## If you run short on time, cut in this order

1. Cut the live demo first (3:20–4:50) — replace with "I have a recorded demo, skipping here"
2. Then compress the build-evidence segment (7:50–8:50) — keep only the fallback chain and testing
3. **Never cut the subtext segment** (4:50–6:20) — that is the entire value proposition
