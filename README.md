# Horrified D&D — New Player Toolkit

A single-file fan reference tool for [Horrified: Dungeons & Dragons](https://ravensburger.com). Built to keep new players unblocked mid-game — everything you need to look up in one browser tab, with persistent state across a full session.

Live at **[gorgon.live/horrifiedTool/](https://gorgon.live/horrifiedTool/)**

---

## What it is

The official rulebook is thorough but dense. This toolkit surfaces the rules new players actually reach for during a game: what order to resolve things, who the monster moves toward, which items stack toward a defeat, how the Beholder's eye rays work. Eleven modules plus a persistent pace tracker pinned to the top of the screen.

No install, no account, no data leaves your browser. One HTML file.

---

## Modules

The sticky topbar shows **Terror**, **Deck count**, and **Frenzy marker** at all times. Tap any tile on the hub to open a module.

| # | Tier | Module | What it does |
|---|---|---|---|
| 1 | Essential | **Turn Coach** | Lost mid-turn? Interactive walkthrough to the right rule |
| 2 | Essential | **Monster Card Walker** | Resolve a drawn card in 3 steps: Items → Event → Attack |
| 3 | Essential | **Attack Resolver** | POW before HIT, target priority, defense options |
| 4 | Essential | **Hero Reference** | Pick your Hero, roll d20, look up your ability result, bank effects |
| 5 | Useful | **Movement Compass** | Answers "who does this Monster move toward?" — Heroes beat Citizens |
| 6 | Essential | **Eye Ray Tracker** | d20 → Beholder ray lookup, plus persistent eyestalk damage tracking |
| 7 | Essential | **Monster Mats** | All 5 monsters — Step 1 Advance, Step 2 Defeat, rules notes |
| 8 | Useful | **Item Lookup** | Full item list filterable by color, shape, strength, and location; cumulative strength calculator |
| 9 | Nice | **Lair Helper** | Tracks the 4 lair tokens (Skull Island, Dragon's Platform, Obelisk of the Eye, Abandoned Camp) — hidden / revealed / blank |
| 10 | Useful | **Setup Wizard** | Pick player count, get a setup checklist for your first game |
| 11 | Nice | **Glossary** | A–Z of every game term, searchable |

**New Game** (hub tile) wipes all tracked state — terror, eyestalks, lairs, banked hero effects — and resets to a fresh session.

---

## State persistence

Terror, deck count, frenzy, eyestalk damage, lair statuses, banked hero effects, and monsters in play are all saved to `localStorage` automatically. Refreshing the page or navigating away preserves your session. Use **New Game** to reset between sessions.

---

## Usage

Open `index.html` directly in a browser, or serve from any static host. The file is fully self-contained — no CDN dependencies, no external requests.

When hosted under `gorgon.live`, the shared `nav.js` from the root repo injects a slim `← gorgon.live` bar at the top. If `nav.js` is absent (local use, standalone deploy), nothing happens.

---

## Disclaimer

Unofficial fan tool. Not affiliated with Ravensburger, Wizards of the Coast, or Dungeons & Dragons. All game content and mechanics belong to their respective rights holders. This tool contains no copyrighted card text or artwork — only mechanical summaries written for reference.
