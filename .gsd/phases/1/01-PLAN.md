---
phase: 1
plan: 1
wave: 1
depends_on: []
files_modified: ["index.html"]
autonomous: true
user_setup: []

must_haves:
  truths:
    - "Viewport scales 1440x960 stage centered without cropping on desktop"
    - "Narrow screens (<=820px) stack intro and cards in a scrollable column"
    - "Intro contains avatar at (136, 82), headline at (321, 92), bio at (321, 203)"
    - "Voice note pill at (321, 287) has 29px orange button, 78 waveform bars, timer"
    - "Available pill at (841, 287) has green dot with pulsing halo"
  artifacts:
    - "index.html"
---

# Plan 1.1: Core Stage, Typography & Intro Section

<objective>
Scaffold the single-file `index.html` with responsive 1440x960 stage container, CSS design tokens, Inter font, and complete intro header section according to exact pixel coordinates and styling.
</objective>

<context>
- .gsd/SPEC.md
- .gsd/ROADMAP.md
</context>

<tasks>

<task type="auto">
  <name>Scaffold HTML foundation, stage scaling, design system & typography</name>
  <files>index.html</files>
  <action>
    Create index.html with meta viewport, Inter font integration, CSS variables for page (#EEECE8), cards (#F5F3EF), hairlines (rgba(0,0,0,0.07)), ink (#1E1C1A), secondary (#77736E), muted (#A7A39D), orange (#EE6A1F), green (#3BC45E), dark (#2A2624).
    Implement desktop viewport wrapper centering a 1440x960 stage using transform: scale(min(100vw/1440, 100vh/960)), and media query <=820px making it a fluid scrollable column.
  </action>
  <verify>Open or inspect index.html, check CSS rules and DOM structure</verify>
  <done>index.html exists with styling tokens and responsive stage scaling</done>
</task>

<task type="auto">
  <name>Build Intro section (Avatar, Headline, Bio, Voice-note pill, Available pill)</name>
  <files>index.html</files>
  <action>
    Implement:
    1. Avatar: 145x145px image at (136, 82) with border-radius 11px.
    2. Headline at (321, 92), 900px wide, font 39.5px/46px, weight 520, tracking -0.021em: "Hi I’m Jagruti — I’m a Product Designer at Fieldnote." followed by muted " Previously at Orbit.".
    3. Bio at (321, 203), 790px wide, 20.5px/31px, two lines: "I am a seasoned product designer with 5 years of experience specializing in / crafting creative tools solutions and empowering creatives.".
    4. Voice-note pill at (321, 287), 495x53px, fully rounded, off-white fill, hairline border, 29px orange play/pause button, 78 waveform bars (2px wide with seeded heights and 2 loud bursts), timer.
    5. Available for Work pill at (841, 287), 174x53px, green dot with pulsing halo.
  </action>
  <verify>Check exact coordinates, dimensions, fonts, and elements in index.html</verify>
  <done>Intro section rendered cleanly at specified stage coordinates</done>
</task>

</tasks>

<verification>
After tasks, verify:
- [ ] 1440x960 stage scales and centers
- [ ] <=820px switches to normal scrolling
- [ ] Intro elements match position and visual specifications
</verification>

<success_criteria>
- [ ] Stage and intro section complete and verified
</success_criteria>
