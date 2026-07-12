# Live Demo Runbook — "JomFix" in Google AI Studio (slide 10, ~20 min)

**Rule: type the prompt, then TALK while it generates (~30–60s each). Never stand silent watching a spinner.**

## How you're running it (your plan)

You're **not building from scratch live** — you're showing your finished **jomfix.ai.studio** and walking the phases. So:

- Walk **Stations 1-4** (slides 11-12) by showing the **Gemini chat you already made** — the idea → scope → brief → blueprint you ran today.
- Show the **finished JomFix app** for the build (slide 13). Narrate the steps; you don't have to re-type them.
- Do the **slop reveal on slide 14**, then the **Pasar API "how to get real data" on slide 15**.
- Have jomfix.ai.studio open and reachable in an incognito window (a stranger with no sign-in should open it clean).

The verbatim prompts below are your reference (and exactly what the students do at their stations).

## Stations 1-4 FIRST — think it through in an AI chat (before AI Studio)

Open a plain AI chat (Gemini / ChatGPT / Claude) on screen. Run these four in order, reading each reply out loud before the next — that models "you still judge the work." Keep it all in one chat. (These are the same prompts on your slides 11-12.)

**1 · Idea** — paste:
> Here's my rough idea: find & message a local home-service pro. Help me turn it into one clear sentence.

**2 · Scope** — paste, dropping in the one-liner it gave you:
> My idea is [the one-liner]. Suggest exactly 3 sections and 3 features — nothing more. Nothing that needs to work while the app is closed, like notifications — everything happens live, on screen, right now.

**3 · Brief** — paste:
> Using my idea and the 3 sections + 3 features I just gave you, write me a short project brief — Name, Audience, Goal, Tone — one line each, consistent with that scope.

**4 · Blueprint** — paste:
> Using the EXACT 3 sections and 3 features from earlier — not new ones — plus my brief, turn it into a blueprint: for each section give Purpose, Content, Action; for each feature give Trigger and Feedback. Nothing that needs to fire while the app is closed, like reminders or notifications.

**Say:** "I did the thinking BEFORE I touched the AI. That blueprint the chat just wrote? That's my first prompt into AI Studio — not a wish."

## Prompt 1 — Build: paste the Blueprint (Station 6)

> Build me a web app called JomFix — find local Malaysian home-service
> pros. Top: a search bar and category icons (Plumbing, Air-Cond,
> Electrician, Runners). Below: provider cards with name, service,
> rate, and star rating. Tapping a card opens a slide-up panel with
> their details and a Call/WhatsApp button. Clean, friendly,
> trustworthy Malaysian style. Use a few sample providers.

**While generating:** "See? That's not 'make me a services app' — that's my Blueprint, word for word. The thinking is why the AI got it right the first time."

**When done:** tap a category, open a provider card. Show the room it works.

## Prompt 2 — test, then improve one thing

Tap the **Call/WhatsApp** button. Does it actually open WhatsApp? Often it won't — it's a pretty button wired to nothing.

> Make each provider card show its star rating in gold, right-aligned.

**While generating:** "One change per prompt. Small steps. If I'd asked for five things and one broke, I wouldn't know which."

## Prompt 3 — THE BUG BEAT (the review/fix lesson)

Tap **Call/WhatsApp** again in front of the room. Very often it does nothing (or find ANY real flaw — something will be off; there always is).

**Say:** "See this? The button's right there, it looks done, and it does nothing. The AI was confident and wrong. This is the whole 'you still judge the work' rule — I only caught it by TESTING."

If it happens to work: "Normally something's broken here — lucky run. Doesn't change the rule: test after every prompt."

**Fix prompt:**

> The Call/WhatsApp button should open WhatsApp with the provider's number (use a wa.me link).

## Prompt 4 — one useful feature

> Add an "Available Today" toggle at the top that shows only providers who are free right now.

**While generating:** "This is the rhythm — describe, test, fix, improve. You'll do this exact loop yourself in an hour."

## Prompt 5 — the twist: REAL live data (via Pasar API) — this is slide 15

Show the room **pasarapi.xyz** — KrackedDevs' directory of Malaysian APIs. Search **fuel**, open the fuel-price API card. Point at the **"Copy AI prompt"** button — it packages the endpoint + "build me a page with safeguards" into a ready prompt. "This is the skill — you don't memorise APIs, you look them up here and copy the prompt."

Hit **Copy AI prompt** → paste straight into AI Studio → it wires the live fuel bar for you.

**Link shortcut** (slicker, but test it in rehearsal first — only works if AI Studio fetches URLs): paste the API's permalink and say:
> Fetch https://pasarapi.xyz/a/weather-forecast, find the API endpoint on that page, and connect it to my app.

The permalink page is server-rendered and really does contain the endpoint, so a browsing-capable AI reads it fine — but if AI Studio can't fetch, fall back to **Copy AI prompt** (self-contained, always works).

(Manual fallback: the endpoint is `https://api.data.gov.my/data-catalogue/?id=fuelprice&limit=1&sort=-date`; newest row has `ron95`, `ron97`, `diesel`.)

**When done:** point at the real RON95 price. "That number is live, from the government, right now. That's a real system — not a mockup."

## The SLOP REVEAL — this is your SLIDE 14 moment (~2 min)

The payoff for the "AI slop" slide, done on your real JomFix (the one with the weather panel). Land on **slide 14 — "One of these is real. One is slop."**

- Show off the beautiful "Live weather advisories — synced with MET Malaysia" panel. Let them be impressed.
- Then tell them straight: **it's 100% fake.** The weather, the cities, the "synced with local councils" line — all hardcoded, invented by the AI. It calls nothing.
- **The kicker (leads into slide 15):** a REAL live MET Malaysia weather API was on Pasar API the whole time — `api.data.gov.my/weather/forecast/`, one "Copy AI prompt" away. The AI made up fake data instead of using it.
- **Land it:** "The petrol price is real because I grabbed a real API. The weather is fake because I didn't. Same app, same AI — the only difference is whether *I* checked. That's the job."

## Step 6 — publish

In AI Studio hit **Publish** (free), copy the link (like `jomfix.ai.studio`), open it in a **new tab** — or on your phone, held up.

"That's a real URL. Anyone here can open this right now. That's the finish line tonight."

---

## Antigravity peek (slide 24, end of class, ~3 min)

You already use Antigravity daily, so keep this loose and live — not a tutorial.

- Take the SAME JomFix idea (or grab a student's idea) and let Antigravity build it as a real project on your machine.
- One line to land it: "AI Studio built us a site in the browser. Antigravity does this on your own machine, with real files you own — this is the next lane when you're ready."
- It's a wow + a "where you go next," not a lesson. Fine to run a touch past 9:00 — it's the finale.

---

## Pacing note (learned the hard way, first run 2026-07-06)

**The stations are the class.** When you hit a timer slide — Idea Lock, the Guillotine, First Build — say the setup lines, start the timer, then *stop presenting*. Walk the room. Silence with a room full of people typing is the class working, not you failing. Only advance slides when a timer ends and the pacing takes care of itself.
