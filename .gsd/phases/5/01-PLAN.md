---
phase: 5
plan: 1
wave: 1
depends_on: ["4-1"]
files_modified: ["index.html"]
autonomous: true
user_setup: []

must_haves:
  truths:
    - "Hero avatar displays Jagruti's attached photo"
    - "Headline reflects Jagruti Gothwal, Product Designer at Delta Infosoft"
    - "Bio reflects 3+ years of experience in SaaS mobile & web apps"
    - "Map card displays Ahmedabad, India"
    - "Experience card features real experience items from resume (Delta Infosoft, My Time SaaS, Attendance App, Pick & Pack, MCA Parul Univ, BCS Kadi Sarva)"
    - "How I Work card features her 4-stage product design methodology from resume"
    - "Available for Work pill links directly to gothwaljagruti@gmail.com"
    - "All existing animations, clock engine, 1440x960 fit, and <=820px responsive modes remain fully functional"
  artifacts:
    - "index.html"
---

# Plan 5.1: Personalize Portfolio with Jagruti's Resume Details & Avatar

<objective>
Update index.html with Jagruti Gothwal's attached photo, verified resume details (Delta Infosoft, Ahmedabad location, 3+ years SaaS mobile/web experience, design process, projects, and education) while preserving all animations and pixel-perfect bento layout.
</objective>

<context>
- index.html
- avatar.png
- User uploaded resume of Jagruti Gothwal
</context>

<tasks>

<task type="auto">
  <name>Integrate attached avatar photo and update hero section details</name>
  <files>index.html</files>
  <action>
    1. Set hero avatar image to avatar.png (Jagruti's uploaded photo) with proper framing and fallback.
    2. Update Headline: "Hi I’m Jagruti — I’m a Product Designer at<br>Delta Infosoft.<span class=\"muted\"> Mobile &amp; Web Apps.</span>"
    3. Update Bio: "Product designer with 3+ years of experience designing SaaS mobile and web apps,<br>specializing in simplifying complex workflows into intuitive, scalable experiences."
    4. Connect Available for Work pill to mailto:gothwaljagruti@gmail.com with Behance link accessibility.
  </action>
  <verify>Check hero avatar, headline, bio, and email link in index.html</verify>
  <done>Hero section personalized with Jagruti's verified identity and attached photo</done>
</task>

<task type="auto">
  <name>Update Bento cards with resume data (Ahmedabad map, real experience timeline, design process)</name>
  <files>index.html</files>
  <action>
    1. Update Experience card timeline with real milestones from resume:
       - Delta Infosoft — UI/UX Designer (2022 – Present)
       - My Time — Workforce SaaS Dashboard (2023 – 2024)
       - Attendance App — Mobile Workforce (2023)
       - Pick & Pack — Logistics Operations (2024)
       - MCA — Parul University (2021 – 2023)
       - BCS — Kadi Sarva Vishvavidyalaya (2018 – 2021)
       Maintain doubled list for 9px/s seamless infinite drift.
    2. Update Map card from Lisbon to Ahmedabad:
       - Centered text: "Ahmedabad"
       - Bottom-left pill: "Ahmedabad, India"
       - Adjust map visual/pin to represent Ahmedabad.
    3. Update How I Work card with 4-step process from resume:
       - 01 Discovery & Scope: Stakeholder discovery sessions to align operational requirements with business goals.
       - 02 Workflows & UX: Simplifying complex business workflows & data-heavy interfaces into guided, digestible interactions.
       - 03 Design System & UI: Designing reusable UI components and high-fidelity prototypes in Figma adhering to Material Design & Apple HIG.
       - 04 Handoff & Visual QA: Partnering with frontend engineering for pixel-perfect implementation and usability refinements.
  </action>
  <verify>Verify Experience timeline, Ahmedabad map, and How I Work step copy in index.html</verify>
  <done>All cards reflect authentic professional background from resume</done>
</task>

</tasks>

<verification>
After tasks, verify:
- [ ] Avatar displays attached photo
- [ ] Headline, bio, experience, map, and process reflect Jagruti Gothwal's resume
- [ ] Browser rendering and animations remain 100% smooth and error-free
</verification>

<success_criteria>
- [ ] Portfolio fully customized to Jagruti Gothwal's resume and verified in browser
</success_criteria>
