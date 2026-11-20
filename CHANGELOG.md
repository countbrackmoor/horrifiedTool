# Changelog — Horrified: D&D Toolkit

Fan toolkit for Horrified: Dungeons & Dragons. Repo: `countbrackmoor/horrifiedTool`. Deployed at `gorgon.live/horrifiedTool/`.

---

## 2026-11-19 — Review pass: fixes, dim theme, undo, offline

### Fixed
- Terror 5 alert ("One more and you lose") never displayed — the Terror ≥ 4 check ran first and shadowed it; order corrected
- Setup Wizard silently set Terror to 3 when solo was chosen and never reverted it if the player count changed; it now only raises Terror if the game hasn't moved it, and undoes its own change when switching away from solo (`soloTerrorApplied` flag)
- Eye Ray Tracker eyestalk grid overflowed 18px at phone width (forced 5 columns with long ray names); now 2 columns under 600px, 5 on wider screens
- Print checklist printed the sticky top bar and the whole UI; added `@media print` sheet that prints only the active module in black on white

### Changed
- Storage schema v2: key `hd5e-toolkit-v2`, stored as `{schemaVersion, state}`; deep-merges against defaults so new nested fields (lairs, citizens) survive older saves. Existing `hd5e-toolkit-v1` saves migrate automatically on first load and the v1 key is removed
- Eye Rays 12–20 (Telekinetic, Sleep, Petrification, Disintegration, Death) and Perks Skeemo Weirdbottle / Ott Steeltoes now say plainly that their card text is not transcribed, with a "Card text needed" badge — previously the text implied the toolkit covered them
- All colors moved to role-based CSS custom properties (`--name-fg/-bg/-line`); Item shape chips keep their fixed game colors
- `meta color-scheme` changed from `light only` to `light dark`
- Embedded icons (favicon, apple-touch-icon, four Monster portraits) reduced to 48-colour PNGs and wrapped across short lines (browsers ignore the breaks): file 226 KB → 145 KB, no change in dimensions

### Added
- Dim theme for low-light tables; follows the device setting by default, top-bar button cycles Auto → Dim → Light (per-device key `hd5e-toolkit-theme`)
- Undo (↶ in top bar): steps back through the last 40 tracked changes — Terror, deck, Frenzy, eyestalks, lairs, citizens, defeats, New Game
- Keyboard and screen-reader access: every clickable tile/pill/eyestalk gets `role="button"`, a tab stop, and Enter/Space activation (including content rendered later); visible focus ring; labelled Terror/deck steppers; live region on top-bar values; focus moves to the module heading on navigation
- Offline support: `manifest.webmanifest` and `sw.js` (network-first, falls back to cache). Registration only runs over https, so local/file use is unchanged. The existing embedded apple-touch-icon covers iOS home-screen installs; the manifest has no icon of its own yet

### Removed
- `standalone/Horrified DnD Toolkit.html` — byte-identical duplicate of `index.html` (same blob SHA) that would drift
- `horrifiedTool-CHANGELOG.md` — stale duplicate of this file

### Notes
- Not verified against the rulebook (no rulebook in the Project): Hero d20 bands, Item list, 30-card deck, 60-token/draw-12 setup, Terror cap of 6, and `defeatMonster` lowering Terror by 1 on each defeat — the last one is suspect and should be checked
- The 2026-06-20 open item (make the Monster selector prominent) is done: the Monster strip under the top bar shows monsters in play, Frenzy holder, and opens each mat

---

## 2026-06-21 — Changelog established

### Added
- This CHANGELOG.md, reconstructed from past work sessions
- Project rule: future changes to this module must be logged here in the same session they're made

---

## 2026-06-20 — Initial integration into gorgon.live

### Added
- `nav.js` integration via silent-fail script tag (works standalone and under the gorgon.live domain)
- Inline topbar offset adjustment script that reads nav.js height and sets the sticky pace tracker bar's `top` dynamically, so it docks beneath the gorgon.live nav and doesn't slide under it
- `README.md` for the `horrifiedTool` repo documenting all 11 modules with tier labels (Essential / Useful / Nice) drawn from the hub tile labels
- Horrified D&D card on the gorgon.live hub (purple `rgba(148,60,220)` accent on `#0c0012` background, animated beholder SVG)

### Notes
- Hub card href settled at `/horrifiedTool/` after initial `/horrified-dnd/` was corrected
- GitHub Pages enablement on the `horrifiedTool` repo was pending at the end of the session — toggle in repo settings to resolve 403s
- The session ended mid-task on a follow-up: making the Monster Selector / Monster Mat more prominent in the toolkit UI (integral to topbar state and many other modules, rather than just another hub tile). Not yet implemented.

---

## Earlier — Baseline (pre-changelog)

The toolkit existed prior to integration with the following established before this log began:

- Single-file HTML toolkit with sticky topbar showing Terror, Deck count, and Frenzy marker at all times
- Hub-grid landing with tappable tiles for each module
- 11 modules including:
  - Turn Coach — interactive turn walkthrough
  - Monster Card Walker — step-by-step Monster card resolution (Items → Event → Attack)
  - Attack Resolver — resolves POW before HIT; target priority and defense options
  - Hero Reference — Hero picker, d20 roll, ability result lookup
  - Movement Compass — answers "who does this Monster move toward?"
  - Plus six additional modules covering items, setup, and monster-specific references
- Persistent state across a full session

No reliable dated record of the toolkit's initial build.
