# ClubFlow PA#2 Developer Handoff

Names, student IDs, screen ownership, and shared-CSS ownership remain TODO until the team records its decision. The two developers—not the team leader—must divide all three screen implementations between themselves.

Read `AGENTS.md`, `docs/SCREEN-CONTRACT.md`, `docs/PA2-CHECKLIST.md`, and all five files in `docs/requirements/` before implementation.

## Team leader — TODO: full name and student ID

The team leader does not own a screen implementation.

Responsibilities:

- Maintain repository setup, rules, and the handoff contract.
- Review developer plans against the course sources before implementation begins.
- Review pull requests, integrate the three screen branches, and preserve meaningful per-screen commits.
- Resolve documentation conflicts by keeping both developers' real prompts and AI-log histories.
- Review cross-screen navigation, shared styles, sample-data consistency, timeline, eligibility, and counts.
- After merging, independently repeat the integration checks at 360, 768, and 1280 px with JavaScript disabled.
- Repeat semantic/accessibility review and W3C validation on the integrated pages; do not rely only on developer evidence.
- Confirm the integrated screenshots and validator results match the final pages.
- Complete and review `PROTOTYPE.md`, `brief.md`, `AI-LOG.md`, and `SELF_ASSESSMENT_REPORT.md` using factual evidence only.
- Prepare the final ZIP, confirm it includes `.git` and excludes `node_modules`, verify the filename/score agreement, and submit it.

## Developer A — TODO: full name and student ID

- Screen ownership: TODO.
- Shared-CSS ownership: TODO.
- Agree with Developer B on shared styles and sample data before either developer starts parallel screen work.
- Implement and fix only the allocated screen branch or branches, plus explicitly assigned shared CSS work.
- Meet the per-screen handoff requirements below.

## Developer B — TODO: full name and student ID

- Screen ownership: TODO.
- Shared-CSS ownership: TODO.
- Agree with Developer A on shared styles and sample data before either developer starts parallel screen work.
- Implement and fix only the allocated screen branch or branches, plus explicitly assigned shared CSS work.
- Meet the per-screen handoff requirements below.

## Ownership decisions required before implementation

Assign every row before coding. One developer will own two screens because three screens are divided between two developers.

| Work item | Branch | Owner |
|---|---|---|
| Create Recruitment Campaign (`index.html`) | `feat/campaign` | TODO: Developer A or Developer B |
| Application Review (`review.html`) | `feat/application-review` | TODO: Developer A or Developer B |
| Interview Scheduling (`scheduling.html`) | `feat/interview-scheduling` | TODO: Developer A or Developer B |
| Shared `assets/css/styles.css` coordination | Used only from the relevant screen branch/branches | TODO: Developer A or Developer B |

Before parallel implementation, both developers must agree on:

- The visual system and shared CSS conventions, without changing the selected plain-CSS stack or spacing scale.
- The campaign identity, timeline, positions, application records/statuses, interviewers, rooms, schedule examples, and reconciling counts defined in `docs/SCREEN-CONTRACT.md`.
- How shared CSS changes will be sequenced to avoid conflicting edits.
- Which long name/title will be used to test wrapping.

The developers choose the actual visual direction and sample values. Record the agreement in the relevant pull requests; do not invent names, decisions, checks, or evidence in advance.

## Per-screen developer handoff

For each owned screen, the developer hands off all of the following:

- A complete implementation of that screen's contract and real relative main-flow links.
- Actual browser verification at 360, 768, and 1280 px with JavaScript disabled.
- Checks for horizontal overflow, clipped/overlapping content, long-content wrapping, and 44 px mobile tap targets.
- Three matching full-page screenshots: `<page>-360.png`, `<page>-768.png`, and `<page>-1280.png` in `screenshots/`.
- A W3C result with zero errors saved as `checks/validator-<page>.png` or `checks/validator-<page>.txt`.
- The actual implementation and correction prompts appended to `brief.md` in chronological order.
- Honest, timely root `AI-LOG.md` entries describing the tool, request, kept/changed/rejected work, hand-written work, and checks actually run.
- Meaningful commits for the screen and its verified fixes; do not collapse all three screens into one generic update commit.
- A pull request from the screen's named feature branch for team-leader review.

Evidence is not interchangeable: screenshots do not replace W3C results, and developer checks do not replace the leader's post-merge integration pass.

## Team-leader integration handoff

After all screen pull requests are merged, the leader repeats and records:

- Direct opening from `index.html` with no build or network requirement.
- All relative navigation and stylesheet-path checks.
- The complete three-page flow and shared-data/count consistency.
- JavaScript-disabled checks at 360, 768, and 1280 px for every page.
- Horizontal-overflow, protruding-element, tap-target, long-content, and responsive-layout checks.
- Semantic landmarks, heading outline, visible labels, meaningful alt text, and button-versus-link use.
- W3C zero-error validation of the integrated version of each page.
- Final full-page screenshots and validator evidence that match the integrated commit.
- Final documentation, self-assessment evidence, Git history, ZIP contents, and submission filename.
