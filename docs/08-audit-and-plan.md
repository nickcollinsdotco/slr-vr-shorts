# 08 · Audit and submission plan (6 Oct 2026, evening)

Based on docs 01 to 07, the prototype, and a full read of the Figma file (all pages screenshotted).

## Progress (6 Oct, late)

- Questions 1 to 7 answered: all recommendations agreed. Imagery: blur **upcoming** clips only (focus + curiosity), "Blur previews" as an optional privacy setting. Full images elsewhere.
- New Figma page **Submission** (`6143:500`), non-destructive copies:
  - `A · Story` (`6143:501`): cover, concept, flow map, decisions, MVP.
  - `B · Key screens` (`6143:2415`): row-2 key screens + captions (08a sits above 08b).
  - `C · Spatial captures` (`6147:2117`): 20 prototype captures (your view, over the shoulder, side, wide; like/skip drags; pull in; step-in storyboard in first person and wide; stepped in; hidden; vertical stack sinking into the floor).
- Copy on Submission updated: skip, pull in / towards you, SLR player style, Hide button, `-->` → `→`, caption fixes, Hide fallback in the gesture map.
- **Not editable by Claude**: gesture map cells in *Martian Mono SemiCondensed* (local font). Nick to change by hand: `Pinch + pull down (BONUS…)` → `Pinch + pull in`, `Grip + pull down, or A` → `Grip + pull in, or A`, `Palm flip` → `Palm flip (if Meta allows)`.
- Prototype: skip, pull in, blurred deck (V), Hide in the rail, shot cameras (C), XR grip now measures pull towards the head. Captures saved in `captures/`.

### 7 Oct: Key Screens 2 (`6156:6581`, section `v2` `6156:10143`)
Nick restyled the screens in SLR's language (room backdrop, Quest-style hands, controller on 09). Claude fixed:
- 05 toast "Skipped Show fewer like this" → "Skipped" (skip is neutral). Frames renamed (05 Skip, 06 Pull in), stamp layer renamed.
- 06, 07a, 07b titles made consistent for the step-in clip: "Anal as Rent · SLR Originals · Full scene 24:10" (was Dirty Sheets / Studio North).
- 06, 07a: one hand only (pinch on the card), down arrows hidden, "Pinch and pull towards you to step in" / "Release to step in" hint chip added.
- 07b: thumbs-up hands hidden (not a gesture in the system).
- Hide button (passthrough icon) added to every rail.
- Missing captions 02, 05, 07, 08, 09 copied in from Submission.
- 11 Gesture map: "Hand tracking" header, Undo and Recentre rows, stick ↓ for step in, no N/A, fallback for Previous, and a "One model, two inputs" direction diagram in the empty space.
All hidden layers are hidden, not deleted.

Open: 05 info panel still says "Dirty Sheets" for the clip being skipped (needs that clip's real title); skip glow is orange like the Like glow (make it neutral grey).

### 7 Oct, late: handover structure
- Pages: 0 · Brief, 1 · Concept, 2 · Key screens, 3 · In the room, 4 · Decisions & MVP, Sandbox. Nick removed the other archive pages.
- 3 · In the room: boards "In the room" and "Stepping in" (storyboard reshot so each step reads: pull, grow, wrap, 180°).
- 07b: curved vignette (`Curved vignette · 180°`) under the player UI to suggest the 180° wrap.

### Still to do (Nick, design)
1. Recolour feed ornaments (rail, info, CTA, coach mark, toasts) from glass to the SLR player panel style.
2. Library: switch to `01 B` (SLR sidebar), swap kittens for blurred stills.
3. Blur the deck cards behind the current clip in the feed frames.
4. Concept slide: replace verb cards + pills with the wide capture and a side-view diagram; add the floor-sink capture as "why depth".
5. Step in: use the 4-frame wide storyboard; curve the 180° frame edges on 07.
6. Skip stamp icon: 🚫 reads as "banned"; use an arrow.
7. Add the Hide button to the rail in the feed frames.
8. Show a controller once (frame 02 or gesture map).
9. Record a 30 s walkthrough of the prototype for the motion bonus.

## Headline

There's more done than the docs suggest. The flow map, the decisions table, the MVP slide and the stepped-in/player frames are good. The job tonight is **curate, unify and add space**, not redesign. Three fixes matter most:

1. One visual language. The feed uses Apple glass; the stepped-in screens already use SLR's real player. Pull the feed towards the player.
2. Show that it's in a room. Only frame 01 has any spatial cue (floor grid). Everything else is a card in a brown void.
3. Tighten two gestures and the words around them (Skip / Pass / Not interested; down / towards).

## Against the brief

| Brief asks for | Status | Gap |
|---|---|---|
| Concept | Strong idea | Three pitch lines: cover "Swipe to judge, pull to step in", Story "The short is the trailer. VR is the film.", Product Logic "Flat by default. Immersive by invitation." |
| Key screens / states | 11 frames, good coverage, including preview in progress, 2D-only tag, end of feed | Flat. Step in shown as window → fullscreen, not into a 180° space. Two identical rows on the page. |
| Decisions + trade-offs | Story 03 is solid | "Look: visionOS glass" row is the weak one. |
| MVP | Story 04 is good, metrics and risky assumptions are a strength | MVP column has 10 items. |

## Page by page

| Page | Verdict | Action |
|---|---|---|
| Brief | Context | Keep |
| Key Screens | Core. Rows at y=160 (`6051:*`) and y=-4875 (`6139:*`) are identical | Keep one row, archive the other |
| Story › 00 Cover | Good personal brand. Sub-line contradicts concept line. Preview cards are small and cropped | Swap sub-line, use a spatial hero |
| Story › 01 Concept | Weakest slide. Bullets + 3 cards + 5 pills, bottom 40% empty. Reads templated | Rebuild around one diagram |
| Story › 02 Flow map | Strong, clear, honest about decision points | Keep. Update edge labels if gestures change |
| Story › 03 Decisions | Strong | Edit the Look row, trim to 6 to 7 rows |
| Story › 04 MVP | Strong. "Ship the door first, then widen the hallway" is a good line | Cut MVP list, move loading/end of feed to "states" |
| Product Logic | Reads the most AI-generated in the file: pill labels, card grid, grey lo-fi boxes, abstract copy ("A quiet preview earns trust") | Archive |
| Visual Exploration | Useful: SLR-native feed ornaments + real SLR player. Kittens, tiny notes | Archive, but borrow its SLR-native ornament styling |
| Sandbox, v1.0, Concept | Process | Archive under one "Process" divider |
| Loose `01 B` on Key Screens | SLR-native library (sidebar, #191919). Closer to SLR than the glass window | Consider as the library frame |

## What's working (lead with it)

1. **Funnel insight.** "Watch full video" becomes the gesture. Senior product thinking.
2. **Controls outside the card**, argued from the content (bottom of frame).
3. **Continuity.** "Continuing at 2:35 of 24:10" toast and "Preview 1:59 left" chip make the timestamp idea tangible.
4. **Paywall in place**, over the paused scene, with "Back to Shorts". Value first, then ask.
5. **Hide.** Category empathy. The passthrough room frame is one of the best in the file.
6. **End of feed** ("12 liked, 3 saved") and skeleton loading. Shows you design edges.
7. **Flow map** and **decisions table**. Clear and honest.
8. **Measures and riskiest assumptions with cheapest tests.** Most candidates won't do this.
9. **Deck in depth came from prototyping** (stack sank into the floor). Not in the file yet. Add it.
10. **Working WebXR prototype.**

## What's wrong, ranked

1. **Two visual languages.** Feed and library: Apple glass, visionOS window, grabber, tab ornament. Stepped-in: SLR's own player (±15, toy, passthrough, timeline thumbnail). Caption 07 even says "Same glass player style", which is no longer true. Pick SLR. It's mostly a recolour of the ornaments to `#191919` at ~85% + 8% white stroke, and you already have that styling in Visual Exploration.
2. **No space.** One card in a brown vignette, at the same scale, in every frame. Nothing says VR except the hand. Add: a side-view diagram on the concept slide, one over-the-shoulder or perspective hero (prototype capture), and the floor grid from 01 behind the feed frames.
3. **Step in lands in a TV.** 06 → 07a → 07b is a window growing to fullscreen. VR 180° should wrap: curve the frame edges, show the peripheral fade, and draw the feed card shrinking behind. One frame done well is enough.
4. **Naming drift on the left flick.** Stamp says "Skip", toast says "Not interested", decisions say "pass", layer is called "Stamp · Like". One word.
5. **Pull "down" vs "towards".** Caption 06 says "pull the card down towards you". The frame shows the card growing (towards). Decide; I'd say towards.
6. **Hide has no visible fallback.** Gesture map says N/A for Hide, but caption 09 calls it a must-have. Add a button (eye-off in the rail). Also: palm flip sits close to Quest's palm-up system gesture. Mention it as a risk.
7. **Hands only.** Every gesture is shown with a photoreal Apple hand. Most Quest users hold controllers. Show the controller once (frame 02 or the gesture map).
8. **Explicit imagery, inconsistently blurred.** Library blurs some thumbnails; feed, step-in and player don't. It also pulls attention off the UI. Use `Blur=on` across the deck, or blur everything except one hero.
9. **Concept slide is templated.** Three verb cards and five principle pills are the "AI deck" pattern. Replace with one diagram and two lines of text.
10. **Caption copy.** `-->` arrows, "(like YouTube )", mixed sentence styles. Quick pass needed.
11. **Numbers as fact.** 1.6 m, 7°, 30%, 3 s, 2 min. Say "starting values, tested in the prototype, to validate in headset".

## Signals that make it read as yours

- One annotated spatial diagram drawn by you beats five generated cards.
- Show one dead end with the reason it died (vertical stack in the floor, arc wall neck turns, Winner B two hands). The prototype screenshot of the floor problem is the strongest proof of real design work in the whole project.
- Fewer, denser boards. Curate the 11 key screens to ~8.
- Extend SLR's player, don't import Apple's kit.
- Copy in your voice, consistent terms.

## Proposed submission (one "Submission" page, left to right)

1. Cover (spatial hero, one line)
2. Insight + concept: web short → "Watch full video" → in VR that's the gesture. Side-view diagram. Deck in depth with the floor-sink capture.
3. Flow map (existing)
4. Key screens: Library, First run, Feed, Like, Skip, Step in (transition strip), Stepped in, Preview → Premium, Hide, Loading / end
5. Gesture map with controller column visualised
6. Decisions and trade-offs (existing, edited)
7. MVP + measures + risks (existing, trimmed)
8. Prototype link + 30 s recording

Everything else under a "Process" divider.

## MVP cut

- **MVP:** Shorts tab, one-clip feed with controls outside, like / skip / previous + Undo, step in at timestamp, Back to the same card, 2-min preview → Premium, hide, controller mapping.
- **States, not features:** first-run hint, loading, end of feed.
- Next / Later unchanged.

## Tonight

| Step | Who | Time |
|---|---|---|
| Answer the questions below | Nick | 10 min |
| New "Submission" page, move/duplicate the keepers in, archive the rest (non-destructive) | Claude | 20 min |
| Prototype: apply gesture answers, capture perspective hero, step-in strip, floor-sink comparison, 30 s recording | Claude | 45 to 60 min |
| Recolour feed ornaments to SLR, curve the 180° frame, blur pass, rebuild concept slide | Nick (Claude can draft) | 1.5 to 2 h |
| Caption + slide copy pass, naming consistency | Claude | 20 min |
| Final check vs brief from screenshots | Claude | 15 min |

## Questions (with recommendations)

1. **Visual language?** SLR's own. Recolour the feed ornaments to match the existing player. Drop the visionOS window and grabber.
2. **Left flick?** Make it neutral "Skip" (just next). "Not interested" moves to More. Removes forced judgement without redrawing frames. A full rethink goes in Decisions as "next".
3. **Step in?** "Pinch and pull towards you." Matches frame 06 already. Update arrow, caption, gesture map, flow label.
4. **Imagery?** Blur everything except one hero frame.
5. **Pitch line?** "The short is the trailer. VR is the film." Cover sub-line becomes the how: "Browse flat, step into 180° at the same moment."
6. **Hide fallback?** Add an eye-off button to the rail. Keep long-press B; palm flip as "if Meta allows".
7. **Library frame?** Keep the glass 01 restyled, or switch to `01 B` (SLR sidebar)? Rec: `01 B`, recoloured, kittens swapped for blurred stills.
