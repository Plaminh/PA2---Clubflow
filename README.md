# ClubFlow Responsive Prototype

ClubFlow is a completed static HTML5 and plain-CSS prototype for the three PA#2 Executive screens. It includes final responsive implementation, a fictional local CV, approved wireframe references, and current browser/validation evidence.

## Open the prototype

Open `index.html` directly in a browser. No installation, network connection, dependency download, or build command is required.

## Folder overview

- `index.html`, `review.html`, and `scheduling.html`: the linked Create Campaign, Application Review, and Interview Scheduling screens.
- `assets/css/styles.css`: shared responsive plain-CSS system.
- `assets/documents/`: the synthetic CF-026 sample CV used by Application Review.
- `docs/design/`: approved visual references, distinct from submission screenshots.
- `docs/PA2-CHECKLIST.md`: implementation and submission checks.
- `screenshots/`: final full-page evidence at 360, 768, and 1280 px.
- `checks/`: current W3C HTML validation records and the explicitly reported CSS-validator status.
- `PROTOTYPE.md`, `brief.md`, `AI-LOG.md`, and `SELF_ASSESSMENT_REPORT.md`: required project documentation.
- `AGENTS.md`: repository-wide implementation rules.

## Collaboration notes

- Open `index.html` directly; the selected static stack needs no installation or build.
- The current repository history uses consolidated phase commits on `feat/pa2-finalize`.
- For future work, create feature branches from the latest `main` and use one implementation branch per independently reviewed screen or task.
- Agree on the owner of shared `assets/css/styles.css` before changing it.
- Submit each screen through a pull request for team-leader review.
- Preserve meaningful per-screen commits when merging.
- Keep both developers' actual `brief.md` prompts and `AI-LOG.md` entries. Resolve conflicts by retaining both histories in chronological order.
- Never commit fabricated evidence or claim checks that were not run.

## Final submission archive

The required final ZIP must include the `.git` directory so the commit history is preserved. It must exclude `node_modules` and generated or temporary files.
