# 04 · Decision log

Format: decision · picked · over · why · trade-off · status. "Status" is how solid it is, not whether it's in Figma.

| # | Decision | Picked | Over | Why | Trade-off | Status |
|---|---|---|---|---|---|---|
| 1 | Job of Shorts in VR | Funnel into full VR scenes, plus a feed | Standalone snack feed | Web already funnels to "Watch full video" / app; business is Premium | Must design the paywall moment | Solid |
| 2 | Feed layout | Deck in depth (next behind, watched lifts away) | Vertical stack, arc wall | Seated stack sinks into floor; one decoder; depth hints "more" | Weak preview of what's next | Solid-ish, prototype-tested only |
| 3 | Arc wall | Rejected for MVP, v2 browse mode | Hero | Decode budget, ±60° head turns, splits attention, breaks one-clip rhythm | Less "wow" | Solid |
| 4 | Controls | Outside the card (ornaments), fade 3 s | Overlay like web | Bottom of frame matters most; YouTube + visionOS precedent | Wider footprint | Solid |
| 5 | Next clip | Flick right = like, left = pass | Both = next; vertical swipe | Every flick is a For you signal | No neutral skip; forces judgement | **Contested**, see critique |
| 6 | Step in | One-hand pinch + pull down + button | Two-hand stretch only; pull toward (z) | One-handed; down is free in Winner A | Less dramatic | Contested: "down" vs "toward" untested |
| 7 | Going back | Flick up + 3 s Undo | None | Hand-tracking misfires | Another gesture | Solid |
| 8 | Continuity | Resume at the short's source timestamp | Start at 0:00 | Keeps the hook moment; conversion | Needs timestamp metadata per short | Solid if data exists |
| 9 | Paywall | 2-min preview from same moment → Premium panel | Block before step-in; hide step-in | Value first | Free viewing given away | Plausible, needs A/B |
| 10 | Environment | Dark space + clip light spill, passthrough toggle | Themed room | Focus, cheap, matches player | Less branded | Open: Quest 3 users may default to passthrough |
| 11 | Visual style | visionOS-style glass | Flat SLR dark panels | Reads as objects in space | **SLR ships on Quest, not mainly Vision Pro**; glass greys out on dark | **Contested**, see critique |
| 12 | Teaching | Ghost hand on first 3 cards | Tutorial screen | Learn by doing | Easy to miss | Plausible |
| 13 | Privacy | Palm flip / long-press B hides all | Pause only | Category need | Extra global gesture | Solid |
| 14 | Posture | One-time recline re-anchor | Head-locked | Head-lock causes discomfort | Manual trigger | Solid |
| 15 | Navigation | One tab bar ≤5 (VR Videos, Following, Shorts, VR Cams, You) | Sidebar in window; 8-tab pill; split pills | visionOS idiom, ≤6 tabs | "You" hides 4 items one level deeper | Plausible |
| 16 | "You" tab | Shelves (Continue watching, Playlists, Liked, Purchases), "See all" → list | Inner sidebar; avatar menu | Glanceable; tab bar stays 5 | Long lists need list view | Plausible |
| 17 | Final key-screen row | Top row (glass player with "From the short" marker) | Row 2 (reuses real SLR player) | Marker proves continuity | Less design-system reuse | Nick's call; reversible |
| 18 | Winner A vs B | A (side flicks + pull down) | B (down flick + two-hand stretch) | B's step-in breaks one-handed rule | B's stretch is more "magical" | Picked by Nick |
