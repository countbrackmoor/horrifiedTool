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

| # | Module | What it does |
|---|---|---|
| 1 | **Turn Coach** | Interactive walkthrough of your turn — tap where you are, get the right rule |
| 2 | **Monster Card Walker** | Step-by-step resolution for a drawn Monster card: Items → Event → Attack |
| 3 | **Attack Resolver** | Resolves POW before HIT, surfaces target priority and defense options |
| 4 | **Hero Reference** | Pick your Hero, roll d20, look up your ability result, bank effects |
| 5 | **Movement Compass** | Answers "who does this Monster move toward?" with a priority checker |
| 6 | **Eye Ray Tracker** | d20 → Beholder ray lookup, plus persistent eyestalk damage tracking |
| 7 | **Monster Mats** | All 5 monsters — Advance steps, Defeat conditions, rules notes |
| 8 | **Item Lookup** | Full item list filterable by color (Red/Blue/Yellow), shape, strength, and location; cumulative strength calculator |
| 9 | **Lair Helper** | Tracks the 4 lair tokens (Skull Island, Dragon's Platform, Obelisk of the Eye, Abandoned Camp) — hidden / revealed / blank |
| 10 | **Setup Wizard** | Guided setup: player count → monster selection → hero picks → printable checklist |
| 11 | **Glossary** | Searchable A–Z of every rule term used in the game |

**New Game** (hub tile) wipes all tracked state — terror, eyestalks, lairs, banked effects — and resets to a fresh session.

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
