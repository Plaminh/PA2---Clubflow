# ClubFlow Style System Implementation Plan

> **For agentic workers:** REQUIRED SUB-SKILL: Use superpowers:executing-plans to implement this plan task-by-task. Steps use checkbox (`- [ ]`) syntax for tracking.

**Goal:** Complete the shared plain-CSS design foundation and apply it consistently to the three ClubFlow PA#2 pages.

**Architecture:** Keep design tokens and reusable component classes in `assets/css/styles.css`. Add only semantic class hooks and compact, static screen-context content to the three existing HTML scaffold pages so the shared shell and component styles are visible throughout the project.

**Tech Stack:** Static HTML5 and plain CSS; no JavaScript, framework, build step, or new dependency.

**Spec:** Approved Superdesign direction in the `ClubFlow PA2 UI System` draft; repository rules in `AGENTS.md`; screen requirements in `docs/SCREEN-CONTRACT.md`.

## Global Constraints

- Use static HTML5 and the existing plain CSS approach. Pages must work when opened directly from the repository without a build step.
- Keep work within the three required screens: Create Recruitment Campaign, Application Review, and Interview Scheduling.
- Use the shared spacing scale: 4, 8, 12, 16, 24, 32, 48, and 64 px.
- Use flexible layouts. Do not introduce fixed page or container widths that cause overflow.
- Never hide layout defects with `overflow-x: hidden`.
- Keep body text at least 16 px.
- At mobile width, standalone buttons and links must be at least 44 px tall.
- Body text and button contrast must be at least 4.5:1.
- Do not use `!important` in custom CSS.
- Main-flow navigation must use real relative destinations and remain available without JavaScript.

## Review Focus

- Long Vietnamese content must wrap within the fluid page and cards.
- Navigation and standalone action targets must remain usable at 360 px.
- Two-column layouts must collapse cleanly on narrow screens and use available space at tablet/desktop widths.
- Forms, tables, and status labels must remain distinguishable without relying on color alone.
- Color, type, spacing, and control styles must remain consistent across all three routes.

---

### Task 1: Build shared design tokens and component styles

**Files:**
- Modify: `assets/css/styles.css`

**Interfaces:**
- Produces: semantic CSS variables under `:root`; shared shell and layout classes; button, panel, form-control, table, badge, alert, and action-row classes for all three pages.

- [x] Replace the scaffold-only rules with tokens for page/surface/text/muted/border/brand/focus/status colors, the required font stack, and the exact shared spacing scale.
- [x] Add base rules for fluid media, readable line lengths, semantic focus visibility, links, page containers, headings, and the shared header/navigation/footer.
- [x] Add reusable styles for `.page-heading`, `.flow-steps`, `.card`, `.button` variants, `.field`, `.field-grid`, `.toolbar`, `.stats-grid`, `.split-layout`, `.status-badge`, `.alert`, `.table-wrap`, and `.action-row`.
- [x] Add mobile-first rules and breakpoints at 48rem and 80rem; stack narrow layouts, permit contained table scrolling, and keep standalone controls at least 44px tall.

### Task 2: Apply the shared system to the three static pages

**Files:**
- Modify: `index.html`
- Modify: `review.html`
- Modify: `scheduling.html`

**Interfaces:**
- Consumes: shared classes and tokens produced by Task 1.
- Produces: all three pages use the shared page shell and responsive screen primitives while keeping the correct page title and active relative navigation link.

- [x] Replace generic placeholder-only markup with compact static screen previews for campaign setup, application review, and interview scheduling, using semantic headings and labels where controls are shown.
- [x] Keep one campaign identity and timeline across the pages: application dates 12/10/2026–30/10/2026 and interview date 05/11/2026.
- [x] Keep sample application totals and schedule statuses consistent; use distinct interviewer/applicant identities and show a genuine same-applicant overlap if a Conflict sample is shown.
- [x] Use real relative links between the three screens and no `href="#"` or JavaScript-only actions.

### Task 3: Inspect the final source changes

**Files:**
- Review: `assets/css/styles.css`, `index.html`, `review.html`, `scheduling.html`

- [x] Inspect the diff for forbidden dependencies, fixed page widths, `overflow-x: hidden`, `!important`, invalid navigation, and inconsistencies in campaign dates, sample counts, and role names.
