---
phase: 4
plan: 1
wave: 1
depends_on: ["3-1"]
files_modified: ["index.html", ".gsd/phases/4/01-VERIFICATION.md"]
autonomous: true
user_setup: []

must_haves:
  truths:
    - "Page renders cleanly with no console errors or broken assets"
    - "At 1440x960 desktop window, intro and all six cards are fully visible with even margins and zero cropping"
    - "Within 6.5s: page rises in, voice note plays with moving playhead, song ticks, experience list drifts, How I work changes 01 -> 02 -> 03"
    - "On narrow screens (<=820px), layout collapses to a fluid scrollable column"
    - "User interactions (voice note play/pause, music controls, step selection hold) work seamlessly"
  artifacts:
    - "index.html"
    - ".gsd/phases/4/01-VERIFICATION.md"
---

# Plan 4.1: Empirical Verification & Visual Polish

<objective>
Serve `index.html` locally, inspect through real browser automation, test all motion criteria, check edge cases and responsive viewports, and verify zero cropping.
</objective>

<context>
- .gsd/SPEC.md
- .gsd/ROADMAP.md
- index.html
</context>

<tasks>

<task type="auto">
  <name>Serve page locally and perform browser verification at 1440x960</name>
  <files>index.html</files>
  <action>
    Start local static server. Run browser testing to verify:
    - Zero cropping at 1440x960 and various window dimensions
    - Entrance animation stagger
    - Voice note playhead, bouncing bars, and timer countdown
    - Timeline drift at 9px/s
    - How I Work step auto-advance (01 -> 02 -> 03 within 6.5s)
    - Photo card and map card styling
    - Mobile column layout at <=820px
  </action>
  <verify>Capture browser screenshots and check DOM properties and console logs</verify>
  <done>Empirical verification completed with browser evidence</done>
</task>

<task type="auto">
  <name>Fine-tune any layout details and generate VERIFICATION.md</name>
  <files>.gsd/phases/4/01-VERIFICATION.md</files>
  <action>
    Apply any polish adjustments if needed.
    Write comprehensive VERIFICATION.md documenting all truths, artifacts, and verification evidence.
  </action>
  <verify>Review VERIFICATION.md against all acceptance criteria</verify>
  <done>All acceptance criteria verified with empirical proof</done>
</task>

</tasks>

<verification>
After tasks, verify:
- [ ] All acceptance criteria met
- [ ] VERIFICATION.md generated with status: passed
</verification>

<success_criteria>
- [ ] Flawless verification and proof
</success_criteria>
