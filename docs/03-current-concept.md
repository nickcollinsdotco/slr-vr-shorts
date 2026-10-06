# 03 · Current concept (as of end of session 1)

Working pitch: **"The short is the trailer. VR is the film."** Alternative from the Product Logic page: **"Flat by default. Immersive by invitation."**

On web, every short already ends with "Watch full video". In VR that link becomes the main gesture: browse flat clips one at a time, judge them with a flick, pull the one you want into the full 180° scene at the same moment.

## Three verbs
1. **Browse**
   - One 9:16 clip at a time, ~1.6 m away, slightly below eye level.
   - Title, performer and actions sit outside the card (YouTube / visionOS ornament idea).
   - Next clips wait behind as stills.
2. **Judge**
   - Flick right = like + next (trains For you, fills You › Liked).
   - Flick left = not interested + next (3 s Undo).
   - Flick up = previous.
3. **Step in**
   - Pinch + pull down (one hand), or the Step in button.
   - The full VR 180° scene starts at the short's source timestamp.
   - Free users get a 2-minute preview, then a Premium panel. Back returns to the same card.

## Principles
- Nothing on the video
- Move content, never the user
- One hand is enough
- Every clip is a door
- Privacy is a feature

## Key screens (Figma "Key Screens" page)
01 Library › Shorts tab · 02 First run (ghost hand) · 03 Feed · 04 Flick right = Like · 05 Flick left = Not interested + Undo · 06 Pull down = Step in · 07 Stepped in (same moment) · 08 Preview ends → Premium · 09 Discreet · 10 Loading / end of feed · 11 Gesture map

## Gesture map

| Action | Hands | Controller | Visible fallback |
|---|---|---|---|
| Like + next | Flick right | Thumbstick → | Heart in rail |
| Not interested + next | Flick left | Thumbstick ← | More › Not interested |
| Previous | Flick up | Thumbstick ↑ | Undo toast |
| Step in | Pinch + pull down (two-hand stretch bonus) | Grip + pull down, or A | Step in button |
| Pause | Pinch tap | Trigger | — |
| Hide | Palm flip | Long-press B | — |
| Back to feed | Pinch Back | B | Back on player |

## Spatial spec (v1, not validated)
- Card: 9:16, 0.62 × 1.1 m, curved R 1.6 m, ~7° below eye line, ~35° vertical FOV.
- Deck: upcoming clips 0.4 m behind, 0.22 m higher, 5% smaller per step, stills only.
- Controls fade after 3 s idle. Hit targets ≥ ~7 cm at 1.6 m.
- Recline: one-time re-anchor along the gaze (~50° up), never head-locked.

## MVP (from Story › 04)
- **MVP**
  - Shorts tab in the library
  - One-clip feed with controls outside the card
  - Like / pass / previous + Undo
  - Pinch + pull down + Step in button
  - Resume at the timestamp, Back to the same card
  - 2-min preview → Premium
  - Ghost-hand first run
  - Discreet mode
  - Controller mapping
  - Loading skeleton + end of feed
- **Next**
  - You tab with shelves
  - Following / New filters
  - Two-hand stretch
  - Recline
  - Performer lane
  - Related shorts at the end of a scene
  - Spatial audio
- **Later**
  - Comments
  - Sharing
  - MR feed over passthrough
  - Haptics sync
  - Creator uploads
- **North star**: step-in rate from shorts.
- **Riskiest assumptions**: users find pull down; flicks misfire on hand tracking; every short has a source timestamp; 2 min is the right preview length.
