---
phase: 2
plan: 1
wave: 1
depends_on: ["1-1"]
files_modified: ["index.html"]
autonomous: true
user_setup: []

must_haves:
  truths:
    - "Row 1 contains Experience (370px), Listening (513px), Reading (371px)"
    - "Row 2 contains Map (370px), Photo (330px), How I work (554px)"
    - "Experience card has vertical timeline structure with doubled items"
    - "Listening card has 165x173 album, Slow Bloom, 243px progress bar, player controls"
    - "Reading card has Patient Builder title, Ada Marsh, tilted multiply-blended book"
    - "Map card has 11px inset map, centered Lisbon, bottom-left Lisbon pill"
    - "Photo card has 11px inset football photo, white pill with orange ball"
    - "How I work card has 29px title, 15px body, 40px segmented control with dark pill"
  artifacts:
    - "index.html"
---

# Plan 2.1: Bento Grid Cards Construction

<objective>
Implement all 6 bento cards in `index.html` with exact layout, typography, media integration, chips, and interactive structures.
</objective>

<context>
- .gsd/SPEC.md
- .gsd/ROADMAP.md
- index.html
</context>

<tasks>

<task type="auto">
  <name>Construct Row 1 Cards (Experience, Listening, Reading)</name>
  <files>index.html</files>
  <action>
    Implement in index.html:
    1. Card 1 (Experience, 370x258): Top-left chip, vertical timeline with 1.5px dark line, 8.5px dots, 15.5px titles, muted years, doubled 6-item list inside a fade mask container.
    2. Card 2 (Listening, 513x258): Top-left chip, album cover (165x173), "SLOW BLOOM" (18px w500), "Juno Vale" (muted), 243px progress bar (3.5px height) with dark fill and mm:ss time labels, Prev/Play/Next/Volume controls.
    3. Card 3 (Reading, 371x258): Top-left chip, "The Patient Builder" (25.5px / 35px), "Ada Marsh" (muted), book image tilted 5° bleeding to bottom right edge with mix-blend-mode: multiply.
  </action>
  <verify>Check Row 1 markup, styling, images, and dimensions</verify>
  <done>Row 1 cards structured and styled according to spec</done>
</task>

<task type="auto">
  <name>Construct Row 2 Cards (Map, Photo, How I work)</name>
  <files>index.html</files>
  <action>
    Implement in index.html:
    1. Card 4 (Map, 370x242): Top-left chip, 11px inset map image with radius 9, centered 27px grey "Lisbon" watermark, bottom-left "Lisbon" pill, pulsing location indicator.
    2. Card 5 (Photo, 330x242): 11px inset football photo with radius 9, bottom-left white pill "I love teaching football" with orange ball icon.
    3. Card 6 (How I work, 554x242): Top-left chip, 40px segmented control (Step 01–04) with dark sliding pill, dynamic 29px title, 15px body copy container with rise transitions.
  </action>
  <verify>Check Row 2 markup, styling, images, and dimensions</verify>
  <done>Row 2 cards structured and styled according to spec</done>
</task>

</tasks>

<verification>
After tasks, verify:
- [ ] All 6 cards have exact dimensions (370, 513, 371 / 370, 330, 554)
- [ ] Chips, typography, icons, and media are properly wired
- [ ] Segmented control and player controls have markup and styling
</verification>

<success_criteria>
- [ ] Full bento grid rendered with all assets and content
</success_criteria>
