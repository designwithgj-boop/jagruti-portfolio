# Phase 6: Works Page, 3 Case Studies, Resume PDF Tab, and Global Navigation

## Goal
Expand Jagruti Gothwal's personal portfolio into a multi-page product design experience with:
1. A dedicated **Works page (`works.html`)** showcasing her 3 flagship SaaS & mobile projects.
2. 3 in-depth, editorial **Case Study detail pages**:
   - `case-study-my-time.html` (Workforce Management SaaS Dashboard)
   - `case-study-attendance-app.html` (Mobile Workforce Tracking App)
   - `case-study-pick-and-pack.html` (Operations Management App & Web Dashboard)
3. A **Resume tab & viewer (`resume.html`)** with interactive preview, key qualifications, and direct download for `resume.pdf`.
4. Unified, sticky floating **Global Navigation Header** connecting Overview (`index.html`), Works (`works.html`), Resume, Contact, and Behance across all viewports.
5. Interactive linkages from `index.html`'s Experience timeline and action pills directly to the case studies.

---

## Tasks

<task id="6.1">
  <title>Create Resume PDF viewer and download page (resume.html)</title>
  <description>
    Build `resume.html` featuring a cohesive top nav, a prominent "Download PDF" button pointing directly to `resume.pdf`, an embedded responsive PDF iframe/object viewer, and an editorial summary of Jagruti's core competencies, experience at Delta Infosoft, and education.
  </description>
</task>

<task id="6.2">
  <title>Build Works showcase gallery page (works.html)</title>
  <description>
    Build `works.html` displaying the 3 featured case studies with filter tags (All, SaaS Dashboard, Mobile App, Logistics & Ops), rich project preview cards, role/timeline metadata, key metrics badges, and direct links to the individual case study pages.
  </description>
</task>

<task id="6.3">
  <title>Build Case Study 1: My Time SaaS Dashboard (case-study-my-time.html)</title>
  <description>
    Create a detailed editorial case study for "My Time — Workforce Management SaaS Dashboard" with project overview, problem statement, research & personas, user flow redesigns, design system standardization, interactive UI mockups, and business impact metrics.
  </description>
</task>

<task id="6.4">
  <title>Build Case Study 2: Attendance App (case-study-attendance-app.html)</title>
  <description>
    Create a detailed mobile UX case study for "Attendance App — Mobile Workforce Tracking Application" covering field-worker friction points, 1-tap geo-verified clock-in flows, Material Design & Apple HIG compliance, offline resilience, and usability outcomes.
  </description>
</task>

<task id="6.5">
  <title>Build Case Study 3: Pick & Pack Operations App (case-study-pick-and-pack.html)</title>
  <description>
    Create a comprehensive cross-platform case study for "Pick & Pack — Operations Management App & Web Dashboard" detailing warehouse floor barcode scanning flows, step-based guided interactions, web admin inventory queues, and operational error reductions.
  </description>
</task>

<task id="6.6">
  <title>Integrate Unified Navigation Header & Links in index.html</title>
  <description>
    Add the global navigation header (Overview, Works, Resume, Contact) to `index.html`. Link the Experience card timeline items directly to the respective case studies, and ensure flawless responsive behavior on desktop, tablet, and mobile.
  </description>
</task>

<task id="6.7">
  <title>Empirical Verification, Git Commits & Vercel Deployment</title>
  <description>
    Empirically test all routes and links using headless Chrome (desktop, tablet, mobile), take screenshots, verify HTTP 200 responses, commit atomically to GitHub, and deploy production build to Vercel.
  </description>
</task>
