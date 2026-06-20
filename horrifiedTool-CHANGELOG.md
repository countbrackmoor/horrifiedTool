# Changelog — Horrified: D&D Toolkit

Fan toolkit for Horrified: Dungeons & Dragons. Repo: `countbrackmoor/horrifiedTool`. Deployed at `gorgon.live/horrifiedTool/`.

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
