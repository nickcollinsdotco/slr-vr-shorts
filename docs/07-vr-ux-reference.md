# 07 · VR UX reference notes

Working knowledge gathered in session 1. **These are starting values, not citations.** Verify against current Meta Horizon OS and Apple visionOS design guidelines before presenting them as fact.

## Placement and size
- Content panels typically sit **1–2 m** away, centred a little **below eye level** (≈5–15° down) to reduce neck strain.
- Session 1 used: card 1.6 m away, 1.1 m tall (≈35° vertical FOV), 7° below eye line, slightly curved (radius = distance).
- Comfortable head rotation is roughly ±30° horizontally. Content much beyond that causes fatigue, which is why the arc wall (±60°) was rejected.
- Seated eye height ≈ 1.2 m. Anything stacked far below the main card drops into the floor plane.
- Nick's Sandbox has a "UI within sight areas" guide (`6004:8167`) with a 848 × 560 px "UI comfort area" and sight-limit rings. Use it.

## Targets and text
- Apple's minimum interactive target is 44 pt with ~60 pt between centres (visionOS). Meta has its own minimums; check them.
- At 1.6 m, ~7 cm targets (≈2.5°) felt right in the prototype. Validate in a headset.
- Size text in angular terms (degrees), not px. Body text on a far panel needs to be much larger than desktop sizes.

## Motion and comfort
- **Move content, never the user.** Moving the world causes vection and motion sickness.
- Transitions into immersive scenes: keep them short (~1 s). A brief dim or fade hides the cut between sources.
- Avoid **head-locked** UI (content glued to the face). Re-anchor on demand (recline) instead.
- Lying down: a feed placed for seated users forces neck flexion, so offer a one-time re-anchor along the gaze.

## Input
- **Quest**: controllers are common (thumbstick, trigger, grip, A/B/X/Y), and hand tracking is widely used. Every gesture should map to a controller action and a visible button.
- Hand tracking misfires: flicks need a distance/velocity threshold, visible feedback past ~30% of travel, and a cancel (spring back).
- Two-handed gestures conflict with one-handed use, which matters in this category.
- Discreet / hide needs a global, fast, unambiguous gesture (palm flip / long-press B were proposed; check they don't clash with system gestures on Quest, where palm-up pinch opens the system menu).

## Visual
- visionOS glass = luminosity-blend grey fill + background blur + specular gradient stroke. It needs something lit behind it. On a dark void it goes flat grey.
- "Ornaments" (visionOS) = controls attached outside a window's edge. That's the same idea as YouTube Shorts' controls outside the video. Useful precedent.
- Light spill: tinting the environment with the clip's average colour (like a bias light) makes flat content feel placed in space. Cheap and effective.
- Decode budget: standalone headsets struggle with many simultaneous video streams. Show neighbours as stills and play only the focused clip.

## Platform note
SLR's VR app runs on Quest, Pico, Apple Vision Pro, Galaxy XR and others (per SLR's site). The current work uses Apple visionOS styling, so decide deliberately whether the final design speaks Quest-native, visionOS, or SLR's own spatial language (see `05-critique-and-gaps.md` #1).
