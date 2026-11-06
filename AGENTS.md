# ClubFlow PA#2 Team Rules

## Scope and stack

- This repository is for the ClubFlow PA#2 responsive prototype.
- Use static HTML5 and the existing plain CSS approach. Pages must work when opened directly from the repository without a build step.
- Read the provided project brief and PA2 rubric before implementation. If either source is unavailable, report it instead of inventing requirements.
- Keep work within the three required screens: Create Recruitment Campaign, Application Review, and Interview Scheduling.
- Do not add dependencies, JavaScript frameworks, a backend, authentication implementation, a database, or other out-of-scope features.
- Use at most one CSS framework. Preserve the selected CSS approach instead of replacing it.
- Do not commit or overwrite unrelated work.

## Required course sources

- Before any implementation or implementation review, read all five course sources in `docs/requirements/`:
  - `requirement.txt`
  - `ClubFlow-final-project-brief.pdf`
  - `PA2-rubric-responsive-prototype.pdf`
  - `AI-LOG.md`
  - `SELF_ASSESSMENT_REPORT template.pdf`
- Treat the files in `docs/requirements/` as unchanged source material. The root `AI-LOG.md` and `SELF_ASSESSMENT_REPORT.md` are the team's working submission documents, not replacements for the course templates.
- Implement and verify against both the final project brief and the PA2 rubric. Where the sources are silent, use a documented product-owner clarification instead of inventing scope.

## Responsive layout

- Design mobile-first and verify at 360 px, 768 px, and 1280 px.
- Use the shared spacing scale: 4, 8, 12, 16, 24, 32, 48, and 64 px.
- Use flexible layouts. Do not introduce fixed page or container widths that cause overflow.
- Never hide layout defects with `overflow-x: hidden`.
- Keep body text at least 16 px.
- At mobile width, standalone buttons and links must be at least 44 px tall.
- Body text and button contrast must be at least 4.5:1.
- Do not use `!important` in custom CSS.

## HTML and interaction

- Use semantic landmarks and exactly one `h1` per page.
- Do not skip heading levels.
- Give form controls visible associated labels and images meaningful alternative text.
- Use buttons for actions. Use anchors or form submissions with real relative destinations for navigation.
- Main-flow navigation must not use `href="#"` or buttons that work only through `onclick`.
- All static content must remain available when JavaScript is disabled.

## Documentation and evidence

- Keep project documents in English; interface text may be Vietnamese.
- Record actual prompts and AI-assisted work honestly.
- Never fabricate tests, evidence, screenshots, validator results, or team contributions.
