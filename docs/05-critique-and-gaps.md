# 05 · Critique and gaps (don't treat the Figma file as canon)

An honest list of what's weak, unproven or missing. Ordered roughly by how much a hiring panel would notice.

## Concept and UX

1. **Platform mismatch.**
   - The visual language borrows Apple visionOS: the glass, the tab bar ornament, the system grabber, Apple's hand illustrations and the Paris/Apartment backdrops.
   - SLR's VR audience is mostly on Meta Quest (plus Pico and others). A reviewer may read it as "designed for the wrong headset".
   - Options: restyle against Meta Horizon OS patterns (check Meta's current Horizon OS UI Set / design guidelines), or keep the glass but frame it as SLR's own spatial style, not Apple's.
   - Either way, swap the Apple hands for Quest controller and hand-tracking visuals.
2. **The flick model is borrowed from dating apps.**
   - Like/pass on every clip forces a judgement each time, and "Tinder for adult clips" may read as transactional or crude.
   - The case for it (free personalisation signal) is real but untested.
   - Alternatives worth one more look:
     - Neutral swipe to advance, with a separate like.
     - Dwell-time as the implicit signal.
     - Like via double-pinch.
3. **"Pull down to step in" is a guess.**
   - Physically, pulling *toward* you (z) is the more spatial metaphor. Down was chosen only because it was free in Winner A.
   - Pull-down could also misfire with a relaxed hand dropping to the lap, which is common when reclined.
   - Needs prototyping in a headset, or at least a defended rationale.
4. **No real spatial depth in the frames.**
   - The key screens are flat 2D compositions: card centred, black void, no perspective, scale reference, environment or stereo cues.
   - "How naturally it fits VR" is a graded criterion. Consider:
     - Over-the-shoulder or third-person shots of the user in the space.
     - A side-view diagram on every key frame.
     - Real environment context (passthrough room, SLR environment).
5. **The step-in transition is described but never shown.**
   - Card → 180° dome, feathered edges, dim. This is the signature moment.
   - Needs a storyboard (3–5 frames) or the motion bonus (record the prototype, or build a HyperFrames/Figma Smart Animate sequence).
6. **Landscape window ≠ VR 180°.**
   - In the Winner A frames, "stepped in" shows a big landscape window, not an enveloping 180° scene.
   - That undersells the concept and contradicts "the short is the trailer, VR is the film".
7. **Undesigned states and flows:**
   - The "2D only" clip path (no VR source) appears only in captions and the flow map.
   - The You tab and its "See all" list.
   - Error / offline.
   - Settings: card distance and size, sound, comfort.
   - The 2-min preview *in progress* (timer chip), not just its end.
8. **Accessibility and comfort are thin.** Nothing covers:
   - Adjustable card distance or size.
   - Text legibility at distance (font sizes weren't validated in angular terms).
   - Seated vs standing height.
   - Left-handed use.
   - Reduced motion.
   - Users who can't do flick gestures.
9. **Evidence is assumed, not cited.**
   - Comfort numbers (1.6 m, −7°, 35° vFOV, 44 pt targets, 3 s fade, 30% threshold, 2-min preview) are reasonable starting values, not researched ones.
   - Either cite sources (Meta/Apple guidelines) or label them "starting values to test".

## Figma file hygiene

- **Too many overlapping truths**: VR Shorts · Concept (v1 + visionOS v2 sections), Sandbox variants, ↳ v.1.0, Key Screens, Story, Product Logic, Visual Exploration. Each tells a slightly different story. The final file needs one clear path: Brief → Story → Key Screens, with everything else archived.
- **Placeholder data is inconsistent and sometimes explicit**:
  - Real-looking titles next to "Performer A" / "Studio North".
  - Red solid thumbnails in Library frames.
  - Kitten placeholders in v1.
  - "Alex" in You tab.

  Pick one data set. Use `Blur=on` or tasteful stills for anything shown widely.
- **Captions vs frames drift**: names and numbers changed several times, so verify caption ↔ frame pairs.
- **Local components are thin**:
  - `vOS / Tab` and `vOS / Short thumbnail` exist.
  - Ornaments (rail, info panel, CTA pill, toasts) are rebuilt per frame as raw frames, not components.
  - Componentise before polishing, so changes propagate.
- **Mixed fonts / styles**: Inter everywhere, but glass styles are Apple-linked remote styles, and the old v1 frames use flat `#191919`. Decide one token set (the SLR library + a few spatial tokens).
- The Story page's concept slide has an empty bottom third and is waiting for a hero visual.

## Prototype

- Updated to Winner A (default), with Tab to compare against Direction A and the Arc wall, plus a WebXR "View in VR" mode.
- Still to do:
  - Test on a real Quest (sizes, distances, the comfort of pull down, controller mapping).
  - Hand-tracking flicks.
  - Real passthrough for hide (needs an `immersive-ar` session).
  - Screen-record a walkthrough for the motion bonus.

## Questions still open

1. Quest-native or visionOS-flavoured visual language?
2. Judge-on-flick, or neutral flick + explicit like?
3. Pull down vs pull toward for step in?
4. Dark environment vs passthrough as the default feed backdrop on Quest 3?
5. What does SLR's real data allow (source timestamps per short, VR vs 2D availability, Premium gating per scene)?
6. How much of this belongs in a "2-hour" submission vs an appendix?
