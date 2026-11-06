# ClubFlow Responsive Prototype

ClubFlow is a static HTML5 and CSS prototype for PA#2. The repository currently contains the project scaffold only; the three required screens have not yet been implemented.

## Open the scaffold

Open `index.html` directly in a browser. No installation, network connection, dependency download, or build command is required.

## Folder overview

- `index.html`, `review.html`, and `scheduling.html`: linked screen scaffolds.
- `assets/css/styles.css`: shared plain-CSS foundation.
- `assets/images/`: source images retained for the prototype.
- `docs/PA2-CHECKLIST.md`: pending implementation and submission checks.
- `screenshots/`: required full-page evidence to be added after implementation.
- `checks/`: validator evidence to be added after verification.
- `PROTOTYPE.md`, `brief.md`, `AI-LOG.md`, and `SELF_ASSESSMENT_REPORT.md`: required project documentation.
- `AGENTS.md`: repository-wide implementation rules.

## Collaboration workflow

- Open `index.html` directly; the selected static stack needs no installation or build.
- Each developer creates feature branches from the latest `main`.
- Use one implementation branch per screen: `feat/campaign`, `feat/application-review`, and `feat/interview-scheduling`.
- Agree on the owner of shared `assets/css/styles.css` before changing it.
- Submit each screen through a pull request for team-leader review.
- Preserve meaningful per-screen commits when merging.
- Keep both developers' actual `brief.md` prompts and `AI-LOG.md` entries. Resolve conflicts by retaining both histories in chronological order.
- Never commit fabricated evidence or claim checks that were not run.

## Final submission archive

The required final ZIP must include the `.git` directory so the commit history is preserved. It must exclude `node_modules` and generated or temporary files.
