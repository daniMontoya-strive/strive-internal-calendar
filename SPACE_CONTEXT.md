# Strive Internal Calendar — Space Context

This document is the project knowledge file for the **Strive Internal Calendar** Perplexity Space. It tells the planning assistant everything it needs to know about this project so every conversation is fully contexted.

---

## Project Identity

- **Project name:** Strive Internal Calendar
- **Owner:** Dani Montoya (`daniMontoya-strive`)
- **GitHub repo:** `daniMontoya-strive/strive-internal-calendar`
- **Repo URL:** https://github.com/daniMontoya-strive/strive-internal-calendar
- **Live site:** https://danimontoya-strive.github.io/strive-internal-calendar
- **Main file:** `index.html` (single-file static app, all code self-contained)
- **Deploy method:** GitHub Actions → GitHub Pages, auto-deploys on every push to `main`

---

## What This Calendar Is

The Strive Internal Calendar is a **Bitcoin-forward internal planning tool** for Strive, Inc. (Nasdaq: ASST), the first publicly traded Bitcoin treasury asset management company.

It is used for:
- **Internal company planning** — key strategic events, executive offsites, earnings prep, product launches, deadlines
- **Bitcoin-relevant dates** — halving anniversaries, protocol events, market watch moments, BTC cultural calendar
- **Company holidays** — US and company-specific holidays with coverage planning

The calendar is a scrollable, year-view HTML application that Dani and the Strive team use to plan, agenda, and discuss upcoming dates. It is **not public-facing** — it is internal operational tooling.

---

## Calendar Event Types

| Type | Color | Use for |
|---|---|---|
| `key` | Bitcoin orange `#F7931A` | Company strategy events, earnings, launches, exec meetings |
| `bitcoin` | Green `#3ECF8E` | Bitcoin protocol dates, halving, BTC market moments, industry catalysts |
| `holiday` | Blue `#4D9DE0` | US holidays, company holidays, planning lockdowns |

---

## How the App Works

- **Year-view grid** with all 12 months visible, scrollable
- **Click any event day** to open the zoom view (full month + event detail sidebar)
- **Hover any event day** to see a tooltip with event titles and notes
- **Double-click any empty day** to open the Add Event form pre-filled with that date
- **+ Add Event button** in the header to add new entries
- **Year navigation** arrows to move between years
- **Month filter** dropdown to isolate a single month
- Events are stored **in-memory only** (no backend) — the calendar resets on refresh
- To persist events permanently, update `index.html` with baked-in event data and push to GitHub

---

## How to Update the Calendar

All calendar updates are pushed to **Dani Montoya's GitHub account** (`daniMontoya-strive`). The workflow is:

1. In this Perplexity Space, tell the assistant what to add, change, or remove
2. The assistant edits `index.html` directly via GitHub API
3. GitHub Actions auto-deploys to GitHub Pages within ~60 seconds
4. The live site updates at https://danimontoya-strive.github.io/strive-internal-calendar

**All pushes must go to:**
- Owner: `daniMontoya-strive`
- Repo: `strive-internal-calendar`
- Branch: `main`
- File: `index.html`

---

## How to Talk to the Assistant in This Space

You can have two types of conversations in this Space:

### 1. Adding / Editing Calendar Entries
Tell the assistant what you want on the calendar and it will update `index.html` and push directly to GitHub. Examples:
- *"Add a key event on August 15th called 'Q3 Earnings Call' with notes about prep steps"*
- *"Add Bitcoin halving anniversary on April 19 2027 as a bitcoin-type event"*
- *"Add Labor Day September 7 as a holiday"*
- *"Remove the mock data and replace with our real Q3 dates"*

### 2. Planning Discussions
Use the assistant to think through agendas, plan around key dates, and organize internal priorities. Examples:
- *"Plan a communications cadence around our next earnings date"*
- *"What Bitcoin dates should we track in Q4?"*
- *"Build a weekly planning rhythm around our September strategy offsite"*
- *"What holidays overlap with our Q4 sprint and how should we adjust deadlines?"*

---

## Tech Stack

- **HTML/CSS/JS** — 100% static, no framework, no backend
- **Fonts:** DM Serif Display (headings) + DM Sans (body) via Google Fonts
- **Hosting:** GitHub Pages
- **Deployment:** GitHub Actions workflow at `.github/workflows/pages.yml`
- **Data storage:** In-memory JS array (events baked into `index.html` for persistence)

---

## Brand & Design

- **Company:** Strive, Inc. — Bitcoin treasury company and asset manager (Nasdaq: ASST)
- **Brand identity:** Bitcoin-forward, dark theme, Bitcoin orange accent `#F7931A`
- **Design tone:** Executive, clean, minimal — serious planning tool not a consumer app
- **Primary accent:** Bitcoin orange `#F7931A`
- **Background:** Near-black `#0D0D0D`
- **Surfaces:** Dark gray layers `#161616`, `#1E1E1E`, `#262626`
- **Event colors:** Orange (key), green (bitcoin), blue (holiday)
