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
