# 06 · Figma map, reusable assets, API gotchas

File key `94B8znXNJOY4odQBBBUHrB`. IDs captured 6 Oct 2026. **Re-verify before writing**: Nick renames, moves and deletes things.

## Pages (current order)

| Page | ID | What's there |
|---|---|---|
| Brief | `0:1` | Brief frame `4010:5792`; web Shorts section `4010:5786`; current VR player `4010:5362`; reference shots section `6004:8669` |
| **Submission** | `6143:500` | The page to present. Sections: A · Story `6143:501`, B · Key screens `6143:2415`, C · Spatial captures `6147:2117`. Copies of the originals with updated copy |
| Key Screens | `6051:767` | Section `6051:768`: 11 V2 frames + captions (01 Library … 11 Gesture map), made by session 1 |
| Story | `6053:767` | Section `6053:768`: 00 Cover `6053:769`, 01 Concept `6053:862`, 02 Flow map `6053:891`, 03 Decisions `6054:896`, 04 MVP `6054:1011` |
| Sandbox | `6004:512` | Apple visionOS kit samples; "UI within sight areas" guide `6004:8167`; Nick's 01 A/B/C (`6018:9181`, `6018:9650`, `6018:9750`); restyles A′ `6027:2256`, B′ `6027:2349`, C′ `6027:2438`, D `6027:2528`, D2 You tab `6033:2051`; notes `6027:2606`; components holder `6025:2255` |
| ↳ v.1.0 | `6043:26712` | Nick's polished Winner A frames (two rows; top row was taken as final) + captions |
| VR Shorts · Concept | `6014:767` | Session 1 v1: Intro section `6019:1133` (cover, framing, flow), Key scenes `6014:768` (flat style), visionOS pass `6028:562` (01, 01b, 02–06 glass), Direction B/decisions/MVP `6021:1262` |
| VR Shorts · Product Logic | `6088:500` | Not by session 1. "Flat by default. Immersive by invitation." Product bet, user job, principles, lo-fi wireframes, rules, MVP, validation |
| VR Shorts · Visual Exploration | `6116:500` | Not by session 1. Additive visual exploration (feed, first-run, immersive, preview complete, quick hide, flow contract) |

The old **DESIGNS** page `6023:13743` (LAB Layouts A–G, Winner A `6043:25141`, Winner B `6043:25142`, "Winner A · redesigned" `6047:4520`) and the **GUIDES** and **Cover** pages no longer appear in the page list. Check before assuming they're gone.

## Reusable assets

**SLR library (remote, already in file)**
- Fonts: Inter (Regular, Medium, `Semi Bold` with a space, Bold). Accent `#FE4E11`, panel `#191919`, muted `#B0B0B0`.
- Web Button set: get it via the instance `I4010:4228;11067:955` → `getMainComponentAsync().parent`. Variants like `Size=Medium, Type=Primary, State=Default`. Props: `Label#356:10`, `Show Left Icon#8093:0`, `Icon Instance#376:0`.
- Side button main `4010:856` (child `icon` instance + count TEXT). Avatar `4010:921`. Tabs group `4010:1850`.
- Sidebar: instance `4010:4229`; nav item set has `state=active`.
- VR player group `4010:5791` (clone for the existing player).
- Icon main components:

| Icon | ID |
|---|---|
| heart-stroke | `4010:839` |
| share | `4010:900` |
| volume | `4010:967` |
| dots | `4010:833` |
| go-vr | `4010:847` |
| playlist_add | `4010:5021` |
| arrow_backward | `4010:5298` |
| passthrough | `4010:5183` |
| favorite-filled | `4010:5017` |
| diamond | `4010:5015` |
| play | `4010:936` |

- Sidebar icons:

| Icon | ID |
|---|---|
| VR Videos | `4010:2505` |
| Following | `4010:2541` |
| Shorts | `4010:2547` |
| VR Cams | `4010:2212` |
| History | `4010:2554` |
| Playlists | `4010:2556` |
| Liked | `4010:2558` |
| Purchases | `4010:2560` |

- Player transport icons (backward_15, pause, forward_15, volume_up, settings): resolve from instances inside `4010:5369` with `getMainComponentAsync`.

**Apple visionOS kit (remote styles, imported by Nick)**

| Style | ID |
|---|---|
| Fill `Windows/Glass` | `S:3bf6afa0fd0e2f28be8033e448b05c68a6f8997c,130:0` |
| Effect `Blur` | `S:a6cddc9c3d99ecd86b8fe4a46a63147a6be9cf04,138:2` |
| Stroke `Windows/(Stroke) Glass Specular` | `S:141d78137c9b007be5d0ba9864232f472f3d29d2,125:64` |

Apply with `setFillStyleIdAsync` / `setEffectStyleIdAsync` / `setStrokeStyleIdAsync`, then `strokeWeight 1.4`, `strokeAlign INSIDE`.

- Window controls: `6004:580` (no toolbar) / `6004:584` (with toolbar). Hide the `Resize - Leading/Trailing` children.
- Backgrounds: `6004:516` (Paris room); Apartment variant used in `6043:27659`.
- Hand gestures set: `Gesture-One-Hand` (Person / Gesture Pinch | Pinch - Halfway | Point / Arm Roll / Opacity Full | Semi / Hand). Example `6004:1711` = Person 2, Pinch, Neutral, Semi, Right.

**Local components (session 1)**
- `vOS / Tab` `6025:2256`
- `vOS / Short thumbnail` `6025:2259` (Nick changed its fill to red)

**Nick's components**
- `vOS` card set `6023:10287`: `Property 1=Short thumbnail, NSFW=on|off, Blur=on|off`. It has Title / Meta / Scrim children; hide those to keep the title outside the card.

**Placeholder image**
- Kitten from the player context frame. imageHash `ca5e378c3469a0e1e2a1ff5d81af0e05c2291ca7`.

## use_figma gotchas learnt the hard way

- Load skills via `get_figma_skill` (`skill://figma/figma-use/SKILL.md`, `.../figma-generate-design/SKILL.md`). `ReadMcpResourceTool` isn't supported by this server.
- One `setCurrentPageAsync` per call. Cross-page `clone()` + `appendChild` into the current page works.
- Failed scripts roll back atomically (no partial nodes), so fix and retry.
- TEXT has no padding props. Wrap text in an auto-layout frame to pad it.
- `layoutSizing* = FILL` only after appending to an auto-layout parent. `counterAxisSizingMode` takes `FIXED | AUTO`.
- Instance names can differ from what you expect (e.g. a background instance is called `Background - Apartment`). Find by index or `startsWith`.
- Editing text inside instances: load the node's current fonts with `getRangeAllFontNames` first.
- `get_metadata` on a whole page can overflow (SSE parse error). Use a read-only `use_figma` outline instead.
- Section children coordinates are relative to the section.
- Glass on a near-black frame reads flat grey. Put a blurred "ambient spill" ellipse behind it.

## Prototype notes

- The browser pane throttles `requestAnimationFrame` when hidden. To inspect states, run this from JS:

  ```js
  step=n=>{const r=requestAnimationFrame;window.requestAnimationFrame=()=>0;let t=performance.now();for(let i=0;i<n;i++){t+=16.7;last=t-16.7;tick(t)}window.requestAnimationFrame=r;last=performance.now()}
  ```

  `dt` is clamped to ≥ 0 so stepping doesn't explode the smoothing.
- Globals reachable from the console: `state`, `cards`, `stepIn()`, `stepOut()`, `setArc()`, `toggleOverlay()`, `toggleHidden()`, `toggleRecline()`.
- Some text uses **Martian Mono SemiCondensed**, a local font the MCP can't load. Those nodes can't be edited by script; leave them to Nick.
- Key Screens has two identical rows: `6051:*` at y=160 and `6139:*` at y=-4875.
