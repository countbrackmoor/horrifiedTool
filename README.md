# Horrified D&D — New Player Toolkit

A single-file fan reference tool for [Horrified: Dungeons & Dragons](https://ravensburger.com). Built to keep new players unblocked mid-game — everything you need to look up in one browser tab, with persistent state across a full session.

Live at **[gorgon.live/horrifiedTool/](https://gorgon.live/horrifiedTool/)**

---

## What it is

The official rulebook is thorough but dense. This toolkit surfaces the rules new players actually reach for during a game: what order to resolve things, who the monster moves toward, which items stack toward a defeat, how the Beholder's eye rays work. Twelve modules plus a persistent pace tracker pinned to the top of the screen.

No install, no account, no data leaves your browser. One HTML file, with optional offline support when hosted.

---

## Modules

The sticky topbar shows **Terror**, **Deck count**, **Frenzy marker**, your Hero, **Undo**, and a theme toggle at all times. Below it, the Monster strip shows Monsters in play and opens their mats. Tap any tile on the hub to open a module.

| # | Tier | Module | What it does |
|---|---|---|---|
| 1 | Essential | **Turn Coach** | Lost mid-turn? Interactive walkthrough to the right rule |
| 2 | Essential | **Monster Card Walker** | Resolve a drawn card in 3 steps: Items → Event → Attack |
| 3 | Essential | **Attack Resolver** | POW before HIT, target priority, defense options |
| 4 | Essential | **Hero Reference** | Pick your Hero, roll d20, look up your ability result, bank effects |
| 5 | Useful | **Movement Compass** | Answers "who does this Monster move toward?" — Heroes beat Citizens |
| 6 | Essential | **Eye Ray Tracker** | d20 → Beholder ray lookup, plus persistent eyestalk damage tracking (rays 12–20 not yet transcribed) |
| 7 | Essential | **Monster Mats** | All 5 monsters — Step 1 Advance, Step 2 Defeat, rules notes, add/remove from game |
| 8 | Useful | **Item Lookup** | Full item list filterable by color, shape, strength, and location; cumulative strength calculator |
| 9 | Nice | **Board Trackers** | Lair tokens (hidden / revealed / blank) and Citizen status |
| 10 | Useful | **Setup Wizard** | Pick player count, get a printable setup checklist |
| 11 | Nice | **Glossary** | A–Z of every game term, searchable |
| 12 | Useful | **Perk Cards** | All 9 Perks with timing tips (Skeemo Weirdbottle and Ott Steeltoes not yet transcribed) |

**New Game** (hub tile) wipes all tracked state — terror, eyestalks, lairs, banked hero effects — and resets to a fresh session. It can be undone.

---

## State persistence

| Key | Contents |
|---|---|
| `hd5e-toolkit-v2` | `{schemaVersion: 2, state}` — Terror, deck, Frenzy, monsters in play, eyestalks, lairs, citizens, banked hero effects, Red Dragon step |
| `hd5e-toolkit-theme` | `auto` / `dark` / `light` (per device) |

Saved automatically on every change. Older `hd5e-toolkit-v1` saves migrate on first load. Undo history (last 40 changes) is in memory only and clears on reload.

---

## Usage

Open `index.html` directly in a browser, or serve from any static host. The file is fully self-contained — no CDN dependencies, no external requests.

When served over https, `sw.js` caches the page for offline play (network-first, so updates still arrive) and `manifest.webmanifest` lets it run standalone from a home screen. Neither is needed for local use.

Theme: follows the device's light/dark setting; the ◐ button in the top bar cycles Auto → Dim → Light.

When hosted under `gorgon.live`, the shared `nav.js` from the root repo injects a slim `← gorgon.live` bar at the top. If `nav.js` is absent (local use, standalone deploy), nothing happens.

---

## Disclaimer

Unofficial fan tool. Not affiliated with Ravensburger, Wizards of the Coast, or Dungeons & Dragons. All game content and mechanics belong to their respective rights holders. This tool contains no copyrighted card text or artwork — only mechanical summaries written for reference.
