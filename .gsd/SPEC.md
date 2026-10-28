# SPEC: Jagruti Profile Page (Bento)

## 1. Objective
Build a production-grade, single-file personal profile page for Jagruti (product designer) featuring a calm, editorial aesthetic, a short hero introduction, and a 6-card bento grid with quiet real UI motion synchronized to a single Web Animation clock.

## 2. Requirements & Constraints
- **Format**: Single-file `index.html` containing HTML, CSS, and vanilla JS. No framework, no build step.
- **Stage & Viewport**:
  - Desktop: 1440×960 fixed-aspect stage scaled via `transform: scale(min(100vw/1440, 100vh/960))` centered in viewport with even margins; never cropped.
  - Mobile / Narrow screens (<=820px): Normal scrollable vertical column (intro then full-width stacked cards).
- **Typography & Font**:
  - Inter (tight neo-grotesk) via font CDN/embed.
  - Headline: 39.5px / 46px, weight 520, tracking -0.021em.
  - Bio: 20.5px / 31px.
  - Card titles: 15.5px–29px; chips: 12.5px.
- **Color Palette**:
  - Page: `#EEECE8`
  - Cards: `#F5F3EF`
  - Hairlines: `rgba(0, 0, 0, 0.07)` (black at 7%)
  - Ink: `#1E1C1A`
  - Secondary: `#77736E`
  - Muted: `#A7A39D`
  - Chips background: `#E9E6E1`
  - Orange accent: `#EE6A1F`
  - Green status: `#3BC45E`
  - Dark segment / pill: `#2A2624`
- **Media Assets**:
  - Avatar: `https://d2ol7oe51mr4n9.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/60582a62-dbab-4bc1-9169-07db0fcb51b1.jpg` (440x440)
  - Album cover: `https://d2ol7oe51mr4n9.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/ed0c3ef0-5a75-4933-9f3c-6afbea39e2ec.jpg` (500x500)
  - Book cover: `https://d2ol7oe51mr4n9.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/b820bd2c-7312-4ac3-8162-76f6d97d4de4.jpg` (503x700, multiply blend)
  - Football photo: `https://d2ol7oe51mr4n9.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/9f4e5ca0-844d-4c0a-8665-5cc5024e3281.jpg` (960x645)
  - Map: `https://d2ol7oe51mr4n9.cloudfront.net/user_38xzZboKViGWJOttwIXH07lWA1P/4f3be2d6-3848-493b-b3d7-5880dac21a63.jpg` (960x645)
- **Intro Layout (Stage Pixels)**:
  - Avatar: 145×145 at (136, 82), radius 11px.
  - Headline at (321, 92), 900px wide.
  - Bio at (321, 203), 790px wide.
  - Voice-note pill at (321, 287), 495×53, rounded, play/pause button (29px orange), 78 waveform bars (2px wide), right-aligned timer.
  - Available for work pill at (841, 287), 174×53, green dot with pulsing halo.
- **Bento Grid Layout (Stage Pixels)**:
  - Outer margins 76px, gaps 17px, radius 14px.
  - Row 1 (top 390, height 258): Experience (370px), What I'm listening (513px), What I'm reading (371px).
  - Row 2 (top 665, height 242): Map (370px), Photo (330px), How I work (554px).
  - Chips on top-left of cards: 12.5px text, icon + text ("Experience", "What I’m listening", "What I’m reading", "Map", "How I work").
- **Card Interactive Motion & Contents**:
  - Experience: Vertical timeline (1.5px line, 8.5px dots, 15.5px titles, muted years), doubled list seamless drift up at 9px/s with top/bottom fade mask.
  - What I'm listening: Album 165×173, "SLOW BLOOM" (18px w500) / "Juno Vale", 243px progress bar (3.5px height) ticking 00:34 to 3:12, Prev/Play/Next/Volume controls.
  - What I'm reading: "The Patient Builder" (25.5px/35px), "Ada Marsh", book tilted 5° bleeding to bottom edge with multiply blend.
  - Map: 11px inset, radius 9, centered Lisbon 27px, bottom-left Lisbon pill, gentle location pulse.
  - Photo: 11px inset, radius 9, football photo, bottom-left pill "I love teaching football" with ball icon.
  - How I work: Title 29px, body 15px, 40px segmented control (01–04) with dark sliding pill. Auto-advances every 1.9s with 0.42s cubic ease (outgoing rises out, incoming rises in). Step click holds for 6s.
- **Unified Clock Engine**:
  - Single Web Animation `currentTime` clock driver on a hidden element.
  - Frame-by-frame `requestAnimationFrame` loop driven from this clock.
  - Entrance: 14px rise + fade-in over 0.7s with 80ms DOM-order stagger.
  - Voice note starts at 1.3s, plays 32s with live playhead, active bar darkening, bouncing bars near playhead.
  - Available dot: halo scale 1 to 2.4, fade out every 1.8s.
  - Cards hover: lift 3px with soft deeper shadow.
  - Prefers-reduced-motion: settle in final static state.
