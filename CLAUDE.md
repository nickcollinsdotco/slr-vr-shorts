# CLAUDE.md

Context for any Claude session continuing this project. Read this first, then `docs/`.

## What this is

Nick Collins' take-home for a **Product Designer** role at SLR (SexLikeReal, an adult VR platform; the Figma file is titled for Infomediji). Brief: bring the web **Shorts / Reels** format (short flat vertical clips in a feed) into SLR's **VR app** so it feels native to VR. Deliverables: concept, key screens/states, decisions + trade-offs, MVP. Graded on conceptual thinking, UX quality, visual quality, how naturally it fits VR. Full brief: `docs/01-brief-and-context.md`.

The take-home was meant to be "a couple of hours max". A lot more than that has gone in. Keep scope tight.

## How Nick wants you to work

- **Report extremely concisely.** Sacrifice grammar for brevity in chat.
- Any copy Nick will present as his own (captions, slides, notes): **British English, no em dashes, no AI filler** ("seamless", "leverage", "unlock", "elevate", "delve", rule-of-three tics). Direct, senior-designer tone. The `my-writing-style` skill encodes this.
- He likes the **grilling format** for decisions: numbered questions, each with a recommended answer, asked in rounds (`grilling` skill).
- He wants to **vastly improve the Figma file**. **Do not treat the Figma file as canon.** It's a record of exploration, with placeholder data, inconsistencies and some weak decisions. `docs/05-critique-and-gaps.md` lists known problems.
- Never overwrite his frames. Make new pages/sections or duplicates; he explicitly asked to keep old content to look back on.
- Content is adult. Work with it professionally and neutrally; never describe imagery. The card component has `NSFW` and `Blur` variants, so use `Blur=on` for anything that might be shared widely.

## Figma

- File key: `94B8znXNJOY4odQBBBUHrB` (URL: https://www.figma.com/design/94B8znXNJOY4odQBBBUHrB/)
- Page/node map, component IDs, style IDs, API gotchas: `docs/06-figma-map.md`. Node IDs drift as Nick edits, so re-check with `get_metadata` or a read-only `use_figma` before writing.
- Use the official Figma MCP (`use_figma`, `get_screenshot`, `get_metadata`). Load the `figma-use` + `figma-generate-design` skills via `get_figma_skill` first (the resource endpoint isn't supported; use the tool).

## Repo contents

- `docs/01-brief-and-context.md`: the brief, company context, existing product (web Shorts, current VR player).
- `docs/02-session-history.md`: what happened in the first session, in order, with the decisions Nick made.
- `docs/03-current-concept.md`: the concept as it stands (Winner A: browse, judge, step in).
- `docs/04-decision-log.md`: decisions, rejected options, trade-offs.
- `docs/05-critique-and-gaps.md`: honest problems with the current work. **Start here when improving.**
- `docs/06-figma-map.md`: file structure, IDs, reusable assets, plugin API gotchas.
- `docs/07-vr-ux-reference.md`: VR ergonomics, comfort, input and platform notes gathered so far.
- `shorts-vr-prototype.html`: three.js browser prototype (older Direction A model, see below). Published as a private artifact: https://claude.ai/artifact/JXRBiWo5zo6DAdBSkWhxSx
- `.claude/launch.json`: static server config for the prototype (`python -m http.server 5178`).

## Running the prototype

Open `shorts-vr-prototype.html` via any static server (three.js loads from cdnjs). In the desktop app, dev servers may be unavailable: run `python -m http.server 5178` in the background, then `preview_start` with `url: http://localhost:5178/shorts-vr-prototype.html`. The browser pane throttles rAF when hidden; to inspect states, step frames manually from JS (see `docs/06-figma-map.md` › Prototype notes).

The prototype still models **Direction A** (vertical deck, Shift+drag down to step in). It does **not** yet model Winner A (flick right/left = like/pass, flick up = previous, pinch + pull down = step in). Updating it is an open task.
