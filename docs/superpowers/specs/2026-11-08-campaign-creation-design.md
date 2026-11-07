# Campaign Creation Screen Design

## Intent

Implement the `index.html` Create Recruitment Campaign screen for the ClubFlow PA#2 prototype. It helps a Club Executive review campaign information, departments, positions, quotas, and requirements before moving toward Application Review.

## Goals

- Replace the scaffold placeholder with a complete, readable campaign setup screen.
- Include campaign details, one campaign timeline, department and position details, quotas, job descriptions, and requirements.
- Show Save as Draft, Preview Campaign, and Publish Campaign controls, plus a real relative Applications link to `review.html`.
- Keep all information visible with JavaScript disabled and preserve the existing static HTML5/plain CSS stack.
- Use semantic HTML, visible labels, one `h1`, responsive layout, shared spacing, readable contrast, and 44 px mobile action targets.

## Non-goals and anti-goals

- No persistence, server behavior, authentication, database, JavaScript dependency, framework, or new pages.
- Do not imply that Save, Publish, Preview, or moving to Application Review actually stores or publishes data or creates applications.
- Do not change `review.html`, `scheduling.html`, course source files, or unrelated working-tree changes.

## Constraints

- Build on the current shared `assets/css/styles.css` and keep static pages directly openable from the repository.
- Check the required page at 360 px, 768 px, and 1280 px; avoid fixed-width overflow, hidden overflow, and `!important`.
- Keep all copy in English unless the existing product context requires otherwise.
- Validate the page with W3C and save three real screenshots at the required widths.

## Approaches

1. Expand the shared stylesheet with reusable campaign layout and form styles. This preserves a consistent base for the three screens and uses the existing CSS architecture. **Selected as the recommended default** because the project already has one shared stylesheet.
2. Keep the shared stylesheet almost unchanged and add page-specific styling in `index.html`. This limits cross-page effects but duplicates styles and makes the shared interface less consistent.

No response arrived during the short clarification window, so approach 1 is used as the working assumption and can be corrected before implementation.

## Interaction representation

The campaign form and controls are static prototype content. Native HTML form semantics and browser validation can represent required fields and dates without JavaScript. Preview content and the post-publication Applications link remain present on the page. Actions must not claim successful storage or publication.

## Open implementation choices

Use the existing visual foundation and the course brief's sample content as guidance. Keep page-specific content in `index.html`; add only shared campaign-related classes and responsive rules to `assets/css/styles.css`.
