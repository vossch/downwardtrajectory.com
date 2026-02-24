# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is the promotional website for **Downward**, a calorie and macro tracking iOS app, served at `downwardtrajectory.com`. No framework or build tooling has been established yet — if adding one, document it here.

## Available Assets

All images live in `assets/`:

| File | Description |
|---|---|
| `Logo.png` | App icon / logo |
| `Home.png` | Home screen (calorie equation + macro bars) |
| `home-full.png` | Full-length home screen scroll |
| `AddFood.png` | Food search and logging UI |
| `AddWeight.png` | Weight logging sheet |
| `GoalsSheet.png` | Goals setup / onboarding screen |

## App Description (for promotional copy)

**Downward** is a minimalist, Swiss-designed calorie and macro tracker for iPhone. Everything is stored locally — no account, no subscription, fully offline after setup.

**Key differentiators:**
- Log a recently-eaten food in **3 taps or fewer** (tap +, tap food, tap confirm)
- Log weight in **2 taps** (tap graph, enter, confirm)
- **~460K foods built-in** — the full USDA FoodData Central database bundled at install, no network required for search
- Falls back to OpenFoodFacts online API only when local search returns nothing
- **Weight graph** with goal trajectory line — visual progress at a glance
- Calorie equation displayed as: `budget − consumed = remaining`
- Macro progress bars for protein, carbs, and fat
- Custom food creation for homemade meals and local items
- Launches in under 1 second; all interactions feel instantaneous

**Core flows to highlight:**
1. **Onboarding**: TOS → Profile (units, height, weight, sex, activity level) → Goals (goal weight + weekly rate → auto-calculated calorie/macro targets + projected goal date) → Home
2. **Daily use**: Check remaining calories and macros, log meals, log weight on graph
3. **History**: Tap the date title to navigate to any past day

**Design personality:** Minimalist, clean, no clutter. Swiss design influence. Light and dark mode. Fast, tactile (haptic feedback on key actions).

## Reference Files

- `reference/spec.md` — Full feature specification including user stories, functional requirements, edge cases, and success criteria
- `reference/claude-md-for-downward-code.md` — CLAUDE.md for the iOS Xcode project (SwiftUI + SwiftData architecture, design system rules)

## Build & Deploy

Pure HTML/CSS static site — no build step required.

- **Local preview:** `python3 -m http.server` from the repo root, then open `http://localhost:8000`
- **Hosting:** GitHub Pages, served from the repo root on the `main` branch
- **Deploy:** Commit and push to `main` — GitHub Pages picks up changes automatically

### App Store link placeholder
Both `index.html` and `privacy.html` contain `.cta-button.disabled` anchor tags with `href="#"`. When the app is live on the App Store, replace `href="#"` with the real App Store URL and remove the `disabled` class.
