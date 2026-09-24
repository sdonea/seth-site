---
project: seth-site
phase: complete
progress: 7/7 (step 1)
principal_stated_goal: "I need a personal website for my Horowitz Andreesen Academy application ... go ahead and start the three directions"
---

# Seth personal site — ISA

## Goal
A personal site for the a16z application that reads as Seth's, not as a generic AI-built portfolio. Step 1: three distinct design directions to choose from.

## Vision
A reviewer knows who Seth is and what he has shipped within the first screen (Paul Stamatiou pattern). One signature idea per direction, no gimmick gating the content.

## Claims
- [x] C1 Three directions exist as standalone pages in `directions/`, each visually distinct in type, color and layout. Probe: screenshots side by side.
- [x] C2 Every direction shows PageMD, Helping Hands, Send Energy, CVL internship, and the RAG benchmark (as in-progress). Probe: grep each file.
- [x] C3 No fabricated facts: unknown numbers/wins are visible `[TBD]` placeholders. Probe: grep for TBD; review copy against sources.
- [x] C4 Credentials visible on first screen at 1440px desktop. Probe: browser screenshot.
- [x] C5 Readable at 390px phone width, no horizontal scroll. Probe: browser at narrow width / scrollWidth check.
- [x] C6 Room direction: content reachable without using the room (plain list present). Probe: screenshot + grep.
- [x] C7 No console errors on load. Probe: browser console.

- [x] C8 The name is always written Sebastian “Seth” Donea (Seth, 2026-09-24): in titles, headings, and footers. Probe: `rg "Seth Donea"` finds no bare form.

## Anti-claims
- [x] A1 None of the usual AI-site tells: purple/blue gradient, Inter, glass cards, emoji icons, three-feature grid. Probe: grep for backdrop-filter, Inter, gradient.
- [x] A2 No fake testimonials or invented metrics. Probe: grep.

## Out of scope
Deploy, domain, final copy, real photo (not yet supplied).

## Decisions
- Content sourced from TELOS, PROJECTS.md, principal memory, pagemd about.html (STARTedUP Challenge), benchmark CLAUDE.md.
- Friend co-founder and CVL supervisor not named on the page (third-party data minimization).
- Evidence (2026-09-24): Chrome screenshots at 1440 and 390 for all three; 390px scrollWidth == clientWidth on all three after poster name fix; room hotspot click opens panel; zero console errors; grep for backdrop-filter/Inter/testimonial empty.
- Next: Seth picks a direction; then real photo, PageMD result/prize, links, email.
- 2026-09-24: Added direction D (`directions/d-your-room.html`), traced from IMG_5551. The lamp crossfades to the real photo (`room/room-real.webp`). GPS and EXIF were stripped with ffmpeg `-map_metadata -1` and cwebp `-metadata none`; mdls lat reads null afterward. All 5 hotspots open the right card, the lamp works from the keyboard, the page doesn't scroll sideways at 390px, and the console shows no errors.
- Rule: never publish the original HEICs. They carry the home's GPS coordinates.
- 2026-09-24: Redrew D as a stylized, tidy version of the room (Seth: don't draw the mess or the bed, spread the objects out). The lamp reveal still shows the real photo. Re-verified: all 5 hotspots, the lamp toggle, and 390px width, with no console errors.
- 2026-09-24: Detail pass on D (Seth: too simple). Added trim, vents, a clock, a rug pattern, wood grain, desk items, a PC with RGB fans, a headset, chair stitching, and poster art. Re-verified the hotspots, the lamp toggle both ways, 390px width, and no console errors.
- 2026-09-24: Rendering pass on D (Seth: more stylized, no new objects). Added gradients on the leather, fur, lamp shade, pots, leaves and desk wood, bloom on the screen, pager and PC fans, ambient occlusion at the seams and corners, plus vignette and grain. Re-verified hotspots, the lamp, 390px width, and no console errors.
- 2026-09-24: Removed the right closet door and extended the back wall. Fixed the top-left light: the lamp glow is clipped off the ceiling and side wall, a soft upward cone lights the alcove, and the side wall now darkens toward the left. Re-verified hotspots, the lamp, and no console errors.
- 2026-09-24: Added resume items to all 4 directions: PageMD betas, regionals, team size; Alumni Mentoring; Extended Essay; Youth & Government; Mock Trial; tutoring; interests. Helping Hands is now 'developer' after the UE Changemaker win. In D, the trophy on the PC is Helping Hands, the certificate is Mock Trial, the ribbons are Y&G, and the books are the EE. 8 hotspots verified, 390px checked on all 4, no console errors. Home address and phone from the resume kept off the site.
- 2026-09-24: Linked Helping Hands and Send Energy in all 4 directions. Both links return 200. The lifefuel-web store still says 'Lucky Energy PUMP'. Only footer placeholders remain (email, LinkedIn, GitHub).
- 2026-09-24: Ceiling fan now spins: 5 blades rotating top-down, squashed to 0.16 for perspective, 2.4s per turn, and it stops under prefers-reduced-motion. Verified with two zoomed frames showing different blade positions around the hub, and no console errors.
- 2026-09-24: Added subtle motion: a query dot hops the graph and flashes each node it reaches, the caret blinks, the pager LED flashes, the mug steams, both plants sway, the CVL lanyard swings, the PC fans pulse, the husky wags now and then, and the clock shows real Chicago time. All of it is off under prefers-reduced-motion. Verified: the walker moved 1215,772 -> 1145,798 -> 1095,758 with a node flash visible in a zoomed frame, getAnimations lists all 9 CSS animations, the clock matched 12:46 AM CT, and no console errors.
- 2026-09-24: Notes now pop out beside the clicked object, with a pointer, on whichever side has room, scaling out from the object. Clicking outside closes them. On phones it stays a bottom sheet. Verified: all 8 hotspots stay inside the stage (right-edge ones flip left), a real mouse click on the pager opens beside it, outside click closes, the 390px bottom sheet stays in view, and no console errors.
- 2026-09-24: Name set to Sebastian “Seth” Donea on all 4 pages: titles, h1s, top bars, footers. The poster name is now two lines at 16.5vw. Verified no bare 'Seth Donea' remains, no overflow at 1440 or 390, the h1 fits on all 4, and the tab title reads correctly.
