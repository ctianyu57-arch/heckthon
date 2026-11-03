# Baseline vs New Implementation — Disclosure

> For the disclosure template in the brief. The judges are checking whether the two AI
> features were genuinely built during the event, so this separates what already existed
> from what was added.

---

## 1 · What existed before the 10:00am reveal on 2 Nov?

A working single-file web app, built on 3–4 October. Already running before the reveal:

| Already built | Status |
|---|---|
| Four-stage conversation flow (16 rounds, L1→L4) | Working |
| Hidden ledger: interest, trust, alertness, three red lines | Working |
| Six behaviour tiers driving her tone | Working |
| Subtext reveal + turn-by-turn debrief with a stronger answer | Working |
| Three-tier fallback (model → offline engine → minimal) | Working |
| Live model connection using the user's own API key | Working |
| Seven automated test suites | Passing |

In short: **the simulator already ran a full fundraising conversation before the event.**
But it was text-only, and every founder got the same interview.

## 2 · Which surprise features did you implement?

| Round | Feature | One line |
|---|---|---|
| Round 1 | **Feature 1 · Your User Changed** | The investor infers what kind of founder you are from free text, and interviews you differently because of it |
| Round 2 | **Feature 3 · No More Typing** | You answer out loud; the model reads the speech *and* scores the delivery |

## 3 · What did you build or change?

### Round 1 — Your User Changed

**Added**
- A free-text field where the founder describes himself in his own words, with four one-click examples
- An inference step: local keyword rules run instantly, then the model upgrades the read into a structured profile — advantage, suspected blind spot, what she will press, what she will go easy on, and her opening question
- That profile is injected into the system prompt, so her opening line, her questions and her leniency all change
- Topic weighting: the same question bank is reweighted toward what this founder type cannot dodge
- A side-panel card showing how she read him, plus a debrief block asking whether he ever used the advantage he was given

**Evidence**
- Four founder descriptions → four distinct archetypes
- Three archetypes → three completely different opening questions
- Over 40 runs each: a solo non-technical founder drew the team-gap question 72 times and unit economics 42; the technical founder inverted it to 60 and 74

### Round 2 — No More Typing

**Added**
- A microphone button; speech is transcribed in the browser and placed in the answer box, so the student can still edit before sending
- Delivery measurement on every spoken answer: duration, word count, words per minute, long stalls, filler words
- Four delivery signals feeding the same scoring engine the typed answers use, so the offline engine reacts too
- The metrics are passed to the model, which is told to notice hesitation without announcing the number
- A live strip under the input showing how it sounded, and a debrief block summarising the spoken answers

**Evidence**
- One stuttering answer, identical words: **typed +11, spoken +2**. The doubt is real, and only the spoken channel carries it.
- Clean delivery earns a positive signal, so speaking well is worth something rather than only avoiding penalties
- Browsers without speech support disable the mic and keep typing fully working

### What did not change

The four-stage structure, the hidden-ledger design and the debrief format were already there.
Both features are additions on top of a working baseline, not a rebuild.

## 4 · The AI test — remove the AI and the feature stops working

| Feature | Remove the model | What breaks |
|---|---|---|
| Your User Changed | No inference of advantage, blind spot or opening question | She opens every founder the same way. A four-option dropdown cannot produce "who actually builds it" for a nurse and "who is going to sell it" for an engineer. |
| No More Typing | No speech model, no delivery judgment | There is no text to judge. A hardcoded list cannot tell whether eight fillers in eighteen words means doubt or just a small vocabulary. |

Neither feature is a fixed rule set. The first needs inference over free-form language; the
second needs a model to interpret unscripted speech and judge how it was delivered.
