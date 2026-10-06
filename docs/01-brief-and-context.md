# 01 · Brief and context

## The brief (from the Figma "Brief" page, frame `4010:5792`)

> We currently have a Shorts / Reels format on web: short flat videos consumed one after another in a feed. Your task is to explore how this format could be brought into a VR application so that the interaction and overall experience feels native to VR.

**What you need to do**
- propose a concept for how short-form flat videos should work in VR
- show the key screens, scenes, or states of the experience
- explain the main design decisions and trade-offs
- outline what should be included in the MVP

**What we will evaluate**
- conceptual thinking
- UX quality
- visual quality
- how naturally the concept fits VR

Format: Figma only. A prototype or animation is a bonus. Nick's time budget: "a couple of hours max" (long exceeded).

## Company and product context

- **SLR / SexLikeReal**: adult VR platform. Web at sexlikereal.com, VR app on Quest and other headsets (also Apple Vision Pro, Pico, Galaxy XR per the web download page). Premium subscription model ("Get Premium" / "Join now").
- **Web Shorts today** (`sexlikereal.com/shorts`, Figma section `4010:5786`):
  - Vertical 9:16 clips, one at a time, desktop and mobile layouts.
  - Tabs: New / For you.
  - Right-side actions: like (count), share, sound, more, a VR "go-vr" button, studio avatar + follow.
  - Bottom overlay *on the video*: "▶ Watch full video" + title. Up/down arrows on desktop.
  - The web pushes a "Go full immersive · Download the app" modal. **Shorts are a discovery funnel into full VR scenes and Premium.** This is the central insight.
- **Current VR player** (Figma frame `4010:5362`, "just for context"):
  - Dark floating panels with an orange accent (`#FE4E11`).
  - Top row: info, title / studio, Get Premium, likes, comments, playlist.
  - Timeline with chapter marker ("Intro") and preview thumbnail.
  - Transport: volume, ±15 s, pause, next, passthrough, haptics (toy), settings, quality tag.
  - Bottom navbar: back button, clock / battery status.
  - Heavy vignette.
- **Design system**: SLR library is linked into the file (Inter font, `#FE4E11` accent, `#191919` panels, white 8% strokes, Button / Icon Button / side button / avatar / tabs / sidebar / player components). See `06-figma-map.md`.
- **Reference shots** (Figma section `6004:8669`): YouTube Shorts (controls *outside* the video), SLR Shorts, SLR "Go full immersive" modal, SLR VR app landing ("You'll feel it. Not just see it.").

## Category-specific realities (worth stating in the presentation)

- Watched alone, often reclined or lying down, often one-handed.
- Privacy needs an instant way out (hide content and audio, show passthrough).
- The bottom of the frame often carries the important content, so UI overlays there are costly. This is why "controls outside the card" (the YouTube point) matters more here than in general video.
- The business job is conversion: short → full VR scene → Premium.
