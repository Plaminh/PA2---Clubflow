# ClubFlow PA#2 Prompt Record

## Prompt 1 — 2026-11-06

```text
Initialize the repository scaffold for PA#2 — ClubFlow Responsive Prototype.

This task is repository setup only. Do not implement the full screens yet.

1. Inspect before changing anything
- Read existing project rules, files, and Git status.
- Read the updated requirement.txt, ClubFlow final project brief, PA2 rubric, AI-LOG template, and self-assessment template if available.
- Report missing source documents; do not invent their contents.
- Preserve existing work, Git history, remotes, and the team's existing CSS choice.
- If this is an existing ShiftNest repository, retain its history and prepare the scaffold for ClubFlow. Do not delete old work without explaining what needs replacement.
- If Git is not initialized, run git init.
- Do not create a remote, push, or change branches.

2. Stack and scope
- Use static HTML5 and CSS.
- If no CSS choice exists, use plain CSS.
- No build step, new dependencies, JavaScript framework, backend, authentication implementation, or database.
- Pages must open directly from the folder and show all content with JavaScript disabled.
- Three screens:
  index.html → Create Recruitment Campaign
  review.html → Application Review
  scheduling.html → Interview Scheduling
- Use relative links between files.

3. Create or safely update this structure

AGENTS.md
README.md
PROTOTYPE.md
brief.md
AI-LOG.md
SELF_ASSESSMENT_REPORT.md
.gitignore
index.html
review.html
scheduling.html
assets/css/styles.css
assets/images/.gitkeep
screenshots/.gitkeep
checks/.gitkeep
docs/PA2-CHECKLIST.md

Keep existing equivalent rules and assets where appropriate instead of duplicating them.

4. AGENTS.md
Write team-wide rules in English:
- ClubFlow PA2 scope and static stack.
- Read the provided brief and rubric before implementation.
- Mobile-first responsive design at 360, 768, and 1280 px.
- Use a shared spacing scale: 4, 8, 12, 16, 24, 32, 48, 64 px.
- Use flexible layouts; no fixed page/container widths that cause overflow.
- Never hide layout defects with overflow-x: hidden.
- At most one CSS framework; preserve the selected CSS approach.
- No new dependencies, JavaScript frameworks, backend, or out-of-scope features.
- Semantic landmarks, exactly one h1 per page, no skipped heading levels, visible associated labels, meaningful alt text.
- Actions use buttons; navigation uses anchors or form submission with a real relative destination.
- Main-flow navigation must not use href="#" or onclick-only buttons.
- Body text at least 16 px; standalone buttons/links at least 44 px tall at mobile width; body text and button contrast at least 4.5:1.
- No !important in custom CSS.
- All static content remains available with JavaScript disabled.
- Record actual prompts and AI work honestly; never fabricate tests, evidence, screenshots, validator results, or contributions.
- Keep documents in English; interface text may be Vietnamese.
- Do not commit or overwrite unrelated work.

5. HTML scaffold
Create three minimal, valid HTML documents:
- <!DOCTYPE html>, correct lang, charset, viewport, distinct title.
- Shared CSS link.
- header, nav, main, footer, and one h1.
- Working relative navigation connecting all three screens.
- A short, clearly labeled implementation placeholder in main.
- No fake application functionality, elaborate layout, mock statistics, or finished-screen claims.
- No template legal/support footer.
These pages are scaffolds, not completed PA2 screens.

6. Shared CSS
Add only the foundation:
- Spacing custom properties using the selected scale.
- Basic colour and typography tokens with readable contrast.
- border-box, body defaults, responsive images, wrapping for long text.
- A fluid container, accessible focus-visible styling, and navigation links at least 44 px tall.
- Explicit mobile-first breakpoints at 768 and 1280 px.
- Do not claim the responsive pass is complete.

7. Documentation
Write documentation in English.

README.md:
- Project purpose and current status: scaffold only.
- Open index.html directly; no installation or build required.
- Folder overview.
- Explain the required final ZIP must include .git and exclude node_modules.

PROTOTYPE.md:
Create the six required sections:
1. Team — use TODO placeholders for unknown full names and student IDs.
2. How to open it — open index.html; no network needed for this scaffold.
3. Screens — table with file, source screen, user goal, and destination of each current navigation link.
4. Your design choices — only current decisions; mark pending decisions TODO.
5. Not wired yet — distinguish scaffold work still pending from controls outside the three-screen scope.
6. CSS — selected approach, spacing scale, breakpoints.

brief.md:
- Save this entire actual prompt verbatim as the first prompt entry.
- If a brief already exists, append this prompt without replacing earlier prompts.

AI-LOG.md:
- Follow the supplied template:
  date/task, Tool, Asked for, Kept, Changed, Rejected, By hand.
- Add one factual entry for this scaffold task, using the actual tool and local date.
- Do not claim the user wrote anything by hand.
- Record only checks actually performed.
- Do not invent a rejected AI mistake.

SELF_ASSESSMENT_REPORT.md:
- Title: Self-assessment — PA#2.
- Team placeholders.
- Seven rubric rows with maximum scores:
  Three linked screens: 20
  Responsive: 25
  Semantic, valid HTML: 20
  Design you can check: 10
  Brief and rules file: 10
  AI-LOG.md: 10
  Commit history: 5
- Leave claimed scores and total as TBD.
- Leave evidence pending rather than inventing it.
- Include “What we did not manage” and “What we would do differently”.
- State that implementation and final verification remain pending.

docs/PA2-CHECKLIST.md:
Include pending checks for:
- All three screens and required features.
- All eight items in the brief's Fix these list.
- Coherent campaign/application/interview timeline and sample data.
- Independent decisions per application.
- Valid scheduling eligibility and confirmation/read-only states.
- Three widths, no horizontal page overflow, long-content wrapping, mobile tap targets.
- JavaScript disabled.
- Semantic HTML, visible labels, alt text, heading outline.
- W3C: zero errors per page; save actual results.
- Contrast and spacing checks.
- Nine full-page screenshots named:
  index-360.png, index-768.png, index-1280.png
  review-360.png, review-768.png, review-1280.png
  scheduling-360.png, scheduling-768.png, scheduling-1280.png
- Three validator results named validator-index, validator-review, validator-scheduling, with .png or .txt extension.
- Required English documents and final evidence.
- Git history: initial rules commit, at least one implementation commit per screen, and a responsive-pass commit.
- ZIP includes .git; student IDs in ascending order; filename total matches self-assessment.
- Deadline: November 9, 2026, 22:00, Vietnam time.

.gitignore:
- Ignore editor/OS clutter, temporary files, secrets, node_modules, and generated submission ZIPs.
- Do not ignore screenshots/, checks/, required documents, or source assets.

8. Git
- Inspect configured Git author identity.
- Do not invent or modify user.name or user.email.
- If identity exists, create one setup commit containing only this task's files:
  chore: initialize ClubFlow PA2 scaffold and project rules
- If identity is missing, finish all file setup and report the exact commands the user must run before committing.
- Do not create empty per-screen commits. The later implementation commits must represent real screen work.
- Do not rewrite existing history or stage unrelated files.

9. Verify and report
- Check that all required scaffold files exist.
- Check each HTML file has the expected title, viewport, landmarks, and one h1.
- Check all current relative page and stylesheet links resolve.
- Review Git diff and status.
- Do not claim W3C validation, browser responsiveness, screenshots, or accessibility inspection unless actually performed.

Finish with a concise report:
- Files created or updated.
- Checks actually performed.
- Commit hash, or why a commit could not be created.
- Missing team/source information.
- Next step: implement the Create Recruitment Campaign screen.
```

## Prompt 2 — 2026-11-06

```text
The five original course documents are now in docs/requirements/.
Read all five files, keeping their existing filenames.

Update AGENTS.md to reference these sources and require reading them before implementation.
Update docs/PA2-CHECKLIST.md against the actual requirements and rubric.

Create docs/TASKS.md recording:

- Team leader: repository setup, review, integration, final verification, submission documentation and packaging.
- The other two members: divide all three screens between themselves, including shared design/CSS, consistent sample data, implementation and page-level verification.
- Leave names and the exact screen allocation as TODO until provided.

Append this actual prompt to brief.md and record the work honestly in AI-LOG.md.
Do not implement screens or change CSS.
Do not invent evidence, team information or scores.
Preserve unrelated work.

Verify the changes and commit only this task's files:
docs: add course sources and prepare team handoff

Do not push. Report what changed and any unresolved requirements.
```

## Prompt 3 — 2026-11-06

```text
Prepare this ClubFlow PA2 repository for handoff to two developers.

Read AGENTS.md, all documents in docs/requirements/, and the existing project documentation first.

Roles:

- Team leader: repository setup, review, integration, final verification, submission documentation and packaging.
- Two developers: divide all three screens between themselves, agree on shared design and sample data, implement and fix their screens.
- Do not assign screen implementation to the team leader.
- Keep unknown names, student IDs and exact screen allocation as TODO.

Tasks:

1. Create or update docs/SCREEN-CONTRACT.md:

- Map index.html, review\.html and scheduling.html to the three required ClubFlow screens.
- List each screen's required UI features using the actual source documents.
- Define relative navigation between the screens.
- List the eight Fix these problems.
- Distinguish static prototype requirements from working backend functionality.
- Record shared data that the developers must agree on before coding: campaign identity, timeline, positions, applications, interviewers, rooms and consistent counts.
- Leave visual design and actual sample-data choices to the developers.

2. Update docs/TASKS.md:

- Record the roles above.
- Require the developers to assign an owner to each screen and to shared CSS.
- Require agreement on shared styles and sample data before parallel implementation.
- Define handoff requirements per screen:
  implementation, actual verification at 360/768/1280 with JavaScript disabled,
  three full-page screenshots, W3C result with zero errors,
  actual prompts, honest AI-log entries, and meaningful commits.
- Require the leader to repeat integration checks after merging.

3. Add a concise collaboration section to README.md:

- Open index.html directly; no build required for the selected static stack.
- Developers create feature branches from the latest main.
- Use one implementation branch per screen:
  feat/campaign
  feat/application-review
  feat/interview-scheduling
- Agree on ownership of shared CSS before changing it.
- Submit changes through pull requests for leader review.
- Preserve meaningful per-screen commits when merging.
- Keep brief.md and AI-LOG.md entries from both developers; resolve conflicts by retaining both histories.
- Never commit fabricated evidence or claim checks that were not run.

4. Review repository readiness:

- Required scaffold files exist.
- HTML navigation and stylesheet paths resolve.
- Required documentation and source files are not Git-ignored.
- No contradiction between README, AGENTS, PROTOTYPE, TASKS and the selected static stack.
- Keep self-assessment scores TBD.
- List outstanding team decisions separately from actual setup blockers.

5. Append this actual prompt to brief.md and record the task honestly in AI-LOG.md.

Do not implement screens, choose a visual design, modify CSS, generate fake evidence, or add dependencies.
Preserve unrelated work.

Verify the changes and commit only this task's files:
docs: prepare developer handoff and screen requirements

Do not push.

Report:

- Changes made.
- Checks actually performed.
- Remaining decisions for the two developers.
- Whether the repository is ready for them to start.
```

## Prompt 4 — 2026-11-08

```text
Mở figma, sử dụng prompt này và các ngữ cảnh cần thiết cho Figma agent tạo 3 wireframe
```

## Prompt 5 — 2026-11-08

```text
use superdesign plugins - complete  assets/css/styles.css: colour, font, spacing, component và responsive use together in the project.
```

## Prompt 6 — 2026-11-08

```text
Tiêu chí Hoàn thành khi

- Đúng brief, semantic HTML; chạy khi tắt JS; đạt responsive 360/768/1280.
- Có 3 screenshot thực tế và kết quả W3C 0 lỗi.
- Cập nhật prompt, AI-log; commit gửi PR

Bạn hãy giúp tôi chạy, không dừng, sai thì quay lại sửa.
```

## Prompt 7 — 2026-11-08

```text
Execute Phase 1 only: register the approved ClubFlow PA2 wireframes.

1. Inspect

- Read AGENTS.md.
- Check the current branch, git status and existing docs/design/.
- Preserve existing work, commits and Git identity.
- Work on feat/pa2-finalize.
- If it does not exist, create it from local main when the working tree is clean.
- If switching would affect uncommitted work, report the situation without stashing, resetting or discarding anything.

2. Add the actual approved images
   Locate the three supplied Final PNGs and copy them into:
   docs/design/01-Create-Recruitment-Campaign-Final.png
   docs/design/02-Application-Review-Final.png
   docs/design/03-Interview-Scheduling-Final.png

- Keep the image contents unchanged; filenames may be normalized.
- Do not regenerate, crop, edit or replace them with older versions.
- Compare existing destination files before replacing anything.
- If the intended originals cannot be identified, report which are missing or ambiguous. Do not invent placeholders or search unrelated personal folders.

3. Document their purpose
   Create or update docs/design/README.md in English:

- Link each image and map it to index.html, review\.html or scheduling.html.
- Explain these are approved visual references, not submission screenshots.
- Implementation may adapt the layout for responsive and semantic HTML.
- Course requirements take priority over image omissions.
- Alternate-state panels are illustrative; no backend or dynamic business logic is required for this static PA2 prototype.
- Record this wording correction for later implementation:
  Replace “Regenerating replaces the current draft after confirmation.”
  with “You will be asked before replacing the current draft.”
- Mark implementation alignment as pending.

4. Record the actual work

- Append this prompt verbatim to brief.md.
- Add an honest Phase 1 entry to AI-LOG.md.
- Do not claim manual user review, browser tests, W3C checks or implementation alignment unless actually established.

5. Verify

- All three destination PNGs exist, open correctly and match their source bytes.
- Documentation links resolve.
- These files are not Git-ignored.
- HTML, CSS and existing screenshots/checks remain unchanged.
- Inspect the final diff and staged paths.

If all three approved images are available and verification passes, commit only Phase 1 changes:
docs: add approved ClubFlow wireframes

Do not push, merge or start Phase 2.

Report:

- Current branch.
- Files added/updated.
- Verification actually performed.
- Missing files or unresolved issues.
- Commit hash and final Git status.
```

## Prompt 8 — 2026-11-08

```text
Execute Phase 2: complete the ClubFlow PA2 static prototype using the approved wireframes.

IMPORTANT:
Do not stage, commit, push, merge or change branches.
Finish the implementation and verification, then STOP for my review.
Commit only after I explicitly approve it in a later message.

1. Read and inspect
- Read AGENTS.md, the course sources in docs/requirements/,
  docs/SCREEN-CONTRACT.md and docs/design/README.md.
- Visually inspect all three approved Final wireframes in docs/design/.
- Inspect current HTML, CSS and git status before editing.
- Stay on feat/pa2-finalize. If another branch is active, report it before editing.
- Preserve unrelated changes and existing Git history.

2. Scope
- Static HTML5 and plain CSS, no new dependencies or JavaScript.
- No backend, persistence, real filtering, scheduling algorithm or dynamic business logic.
- Preserve useful existing implementation.
- Use the wireframes as visual references, adapting layouts for responsive and semantic HTML.
- Course requirements take priority over image omissions.
- Keep the existing interface language consistent.
- Alternate-state examples may use clearly labelled sections or native details/summary.
- All content must remain accessible with JavaScript disabled.

3. Shared CSS and Campaign
Update assets/css/styles.css and index.html:
- Match the approved visual direction without reproducing every pixel.
- Reuse the spacing scale, colours and shared components.
- Campaign information, dates, instructions, departments, positions, quotas,
  job descriptions and requirements.
- Save Draft, Preview and Publish controls.
- A readable static campaign preview.
- A clearly labelled Published example if used.
- A working relative link to review.html.
- Use an intentionally long Vietnamese campaign title consistently across all three pages.
- Do not lock campaign configuration merely because it is published.

4. Application Review
Update review.html:
- Consistent campaign context and realistic application/applicant statistics.
- Search, position/status filters, sorting and coherent pagination representation.
- If all six records are on one page, show Page 1/1 with appropriate disabled
  pagination controls; do not invent a second page.
- List and readable application details: candidate information, full sample SOP,
  CV affordance, visible labelled note textarea, Shortlist and Reject controls.
- Clear affordances for reviewing an application and closing its details.
- Do not claim state preservation or saving actually works if it is only illustrative.
- Decisions apply to individual applications, including separate applications
  from the same candidate.
- Relative navigation to index.html and scheduling.html.
- Do not invent a working CV link. Reuse a valid local sample if available;
  otherwise report the missing asset and represent the control honestly.

5. Interview Scheduling
Update scheduling.html:
- Date, time window and duration controls with 15/20/30-minute options.
- Interviewer-position assignments, availability and existing room choices.
- Draft schedule with Proposed, Conflict and Unassigned states.
- Concrete availability/reasons sufficient to explain the sample schedule.
- Edit, Resolve, Assign Slot, Save Changes and Export controls.
- A real sample conflict and internally consistent totals.
- If Review contains a pending application, confirmation must remain blocked.
- A compact, clearly separated Confirmed/read-only example may illustrate the final state.
- If the confirmed example still has only four interviews, explicitly show that
  pending CF-028 was rejected during CV screening.
- Use this wording:
  “You will be asked before replacing the current draft.”
- Do not implement revalidation, regeneration or confirmation logic.
- Provide relative navigation back to review.html.

6. Cross-screen requirements
- Use identical campaign identity, dates, positions and application IDs.
- Department Digital Product → Position User Experience Design.
- Department Communications → Position Content Creation.
- Applicant and interviewer identities must be distinct.
- Counts and statuses must match their displayed records.
- Avoid all eight Fix these problems.
- One h1 per page, appropriate landmarks and heading order.
- Visible associated labels; actions are buttons, navigation uses anchors.
- Main-flow links must resolve to real relative HTML destinations.
- No href="#" substitutes or onclick navigation.
- Body text at least 16 px; standalone mobile targets at least 44 px.
- No custom !important or overflow-x: hidden used to conceal layout problems.
- Support 360, 768 and 1280 px; tables may scroll inside their own wrapper.

7. Documentation during this task
- Append this actual prompt to brief.md.
- Update AI-LOG.md honestly with changes and checks actually performed.
- Do not attribute my review or approval before I provide it.
- Do not finalize self-assessment scores or claim submission readiness.
- Do not overwrite existing submission screenshots/checks in this phase.
  Report which evidence becomes stale and needs regeneration in Phase 3.

8. Verify before handing back
- Check relative links and asset paths.
- Review cross-screen dates, positions, counts and statuses.
- Inspect HTML structure and CSS.
- If browser tooling is available, inspect all three pages at the three widths
  with JavaScript disabled and fix obvious layout defects.
- Keep review captures separate from final submission evidence.
- Do not claim browser or W3C checks that were not performed.
- Inspect git diff and confirm no unrelated files were modified.

Finish with:
- Files changed and concrete changes per page.
- Checks actually performed.
- Any unresolved issues, missing assets or assumptions.
- How I can open and review the three pages.
- Suggested separate commit messages for each page, without committing.
- Final git status.

STOP and wait for my review. Do not proceed to Phase 3.
```

## Prompt 9 — 2026-11-08

```text
Finish Phase 2 with these limited changes:

1. Add a clearly labelled fictional sample CV for CF-026, using synthetic
   information only. Prefer a valid local PDF and a real relative link from
   review\.html. Do not use personal data or fabricate verification evidence.

2. Move repetitive implementation explanations out of the interface into
   PROTOTYPE.md's “Not wired yet” section. Keep the UI concise while preserving
   clear labels for alternate-state examples.

3. Verify the CV opens, relative links resolve, and the changed Review layout
   still works at 360/768/1280 with JavaScript disabled.

Update the actual prompt record and AI-log honestly.
Do not stage, commit, push or start Phase 3.
Report changes, checks and remaining issues for my review.
```

## Prompt 10 — 2026-11-08

```text
# ClubFlow PA#2 — Phase 2 Final Correction and Recheck

The independent browser audit is complete.

Results:

- All 9 responsive test cases PASS.
- Navigation PASS.
- Business-data consistency PASS.
- Accessibility checks PASS.
- One remaining Phase 2 UI defect: the invalid campaign example does not display a disabled Publish control.

## Task 1 — Fix the invalid Publish state

Inspect `index.html` and the relevant styles in `assets/css/styles.css`.

Correct the invalid campaign publication example so that:

1. The invalid campaign state clearly communicates why publishing is blocked.
2. A real Publish button is visibly disabled in that invalid state.
3. Use the native HTML `disabled` attribute.
4. The button styling clearly communicates its disabled state.
5. Error text is associated with the relevant field.
6. The separate Published example remains clearly distinguishable.
7. There is no contradiction between the validation message and the available actions.

Preserve the current static HTML/CSS implementation.

Do not introduce JavaScript or dependencies.

Do not implement actual publishing logic.

## Task 2 — Regression testing

After the correction, repeat browser testing with JavaScript disabled.

Verify all three pages at:

- 360px
- 768px
- 1280px

Check:

- No horizontal overflow.
- No clipping or overlapping.
- Existing navigation remains functional.
- Existing application and scheduling statistics remain unchanged.
- Campaign validation state is now semantically correct.
- Disabled button is visually identifiable and cannot be activated.
- Keyboard focus and labels remain correct.

Also verify direct file opening compatibility for all three HTML pages, if local browser permissions allow.

## Task 3 — Final assessment

Compare the corrected prototype against the ClubFlow PA#2 rubric.

Separate:

- Phase 2 implementation defects.
- Phase 3 evidence/documentation tasks.
- Unverified requirements.

Do not treat stale screenshots, missing current W3C results, or unfinished self-assessment as functional UI defects. They remain required before final submission.

## Task 4 — Report for review

Return:

1. Files changed.
2. Exact correction made.
3. Regression test matrix.
4. Remaining UI defects.
5. Remaining Phase 3 tasks.
6. Whether Phase 2 implementation is ready to commit.

## Restrictions

- Do not commit or push.
- Do not switch branches.
- Do not regenerate screenshots.
- Do not regenerate W3C evidence.
- Do not rewrite unrelated pages.
- Do not install packages.
- Preserve existing staged changes.
- Show the final diff and wait for my review.

Stop after reporting.
```
