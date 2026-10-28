---
phase: 3
plan: 1
wave: 1
depends_on: ["2-1"]
files_modified: ["index.html"]
autonomous: true
user_setup: []

must_haves:
  truths:
    - "A single Web Animation clock drives all motion synchronously via requestAnimationFrame"
    - "Blocks rise 14px and fade in over 0.7s with 80ms stagger in DOM order"
    - "Voice note begins at 1.3s, plays for 32s with live timer, playhead bar darkening, and bouncing bars"
    - "Voice note button toggles play and pause"
    - "Available dot halo scales from 1 to 2.4 and fades out every 1.8s"
    - "Experience list drifts upward seamlessly at 9px/s"
    - "Music player progress bar and mm:ss time advance smoothly and toggles play/pause"
    - "How I work segmented control auto-advances every 1.9s with 0.42s ease, and step click holds for 6s"
    - "Hovering cards lifts 3px with deeper shadow"
  artifacts:
    - "index.html"
---

# Plan 3.1: Unified Clock Engine & UI Motion Choreography

<objective>
Implement the single Web Animation clock engine and wire all entrance, playback, drift, pulsing, and step transitions to achieve the complete synchronized motion specifications.
</objective>

<context>
- .gsd/SPEC.md
- .gsd/ROADMAP.md
- index.html
</context>

<tasks>

<task type="auto">
  <name>Implement Web Animation clock driver and entrance staggered choreography</name>
  <files>index.html</files>
  <action>
    Create a hidden Web Animation on #clock-driver that loops indefinitely.
    In the rAF loop, read clockAnim.currentTime.
    Implement entrance animation: each .motion-block rises 14px and fades in over 0.7s with 80ms stagger in DOM order based on clock time.
    Wire the available dot halo pulsing (scale 1 to 2.4, fade out every 1.8s).
  </action>
  <verify>Check clockAnim initialization, rAF loop, and entrance transformation progress</verify>
  <done>Clock engine running and entrance stagger executes smoothly from t=0</done>
</task>

<task type="auto">
  <name>Implement Experience drift, Music progress, Voice Note player & How I Work step cycle</name>
  <files>index.html</files>
  <action>
    Wire motion components to the single clock:
    1. Experience timeline: drift upward continuously at 9px/s with seamless looping.
    2. Voice note: starts at 1.3s, plays for 32s. Button shows pause icon, timer counts 0:00 to 0:32, bars left of playhead turn dark, bars near playhead bounce (scaleY up to +55%). Button toggles play/pause.
    3. Music player: progress bar (243px) and mm:ss time advance from 00:34 through 3:12. Play/pause toggles state. Prev/Next buttons interactive.
    4. How I work: auto-advances every 1.9s with 0.42s ease. Dark pill slides, outgoing text rises out, incoming text rises in. Clicking a step button holds for 6s.
  </action>
  <verify>Verify voice note playback, music advancement, timeline drift, and step sliding in browser</verify>
  <done>All interactive motion running in lockstep with the unified clock</done>
</task>

</tasks>

<verification>
After tasks, verify:
- [ ] Within 6.5s: page rises in, voice note plays with live playhead, song time ticks, experience drifts, steps change 01->02->03
- [ ] Interactive controls (voice play/pause, music play/pause, step click hold) function properly
</verification>

<success_criteria>
- [ ] All motion and acceptance checks pass flawlessly
</success_criteria>
