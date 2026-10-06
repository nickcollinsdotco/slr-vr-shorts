# SLR · Shorts in VR

Context repo for Nick Collins' Product Designer take-home: bring SLR's web Shorts into the VR app so it feels native to VR.

- **Figma**: https://www.figma.com/design/94B8znXNJOY4odQBBBUHrB/ (key `94B8znXNJOY4odQBBBUHrB`)
- **Prototype** (three.js, desktop): `shorts-vr-prototype.html`. Private artifact: https://claude.ai/artifact/JXRBiWo5zo6DAdBSkWhxSx
- **Start here**: `CLAUDE.md`, then `docs/05-critique-and-gaps.md`

| Doc | What |
|---|---|
| `docs/01-brief-and-context.md` | Brief, company and product context |
| `docs/02-session-history.md` | How the work evolved in session 1 |
| `docs/03-current-concept.md` | Concept, gestures, spec, MVP as they stand |
| `docs/04-decision-log.md` | Decisions with alternatives, trade-offs, confidence |
| `docs/05-critique-and-gaps.md` | What's weak or missing. The Figma file isn't canon |
| `docs/06-figma-map.md` | Page/node IDs, reusable components and styles, API gotchas |
| `docs/07-vr-ux-reference.md` | VR ergonomics, comfort, input, platform notes |

Run the prototype:

```bash
python -m http.server 5178
```

Then open http://localhost:5178/shorts-vr-prototype.html
