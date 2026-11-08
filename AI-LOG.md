# AI-LOG.md — ClubFlow PA#2

## 2026-11-06 — Initialize the ClubFlow repository scaffold

Tool: OpenAI Codex

Asked for: Inspect the workspace, initialize Git when needed, and create a static HTML5 and plain-CSS scaffold with three linked pages, shared rules, required documentation, evidence placeholders, verification, and one setup commit.

Kept: The requested static stack, file structure, three minimal page scaffolds, shared navigation, CSS foundation, documentation sections, pending checklist, and Git workflow.

Changed: Selected plain CSS because the repository had no existing CSS choice, and adapted the nearby course-style documentation templates to the ClubFlow PA#2 headings and pending evidence requirements.

Rejected: None.

By hand: Reviewed the generated repository structure and confirmed the scaffold setup before proceeding.

Checks: Confirmed the required scaffold paths existed; compared the prompt recorded in `brief.md` with the supplied prompt for an exact textual match; inspected each HTML source for its expected title, viewport, semantic landmarks, exactly one `h1`, and resolvable relative links; checked the CSS source for both required breakpoints and the absence of `!important` and `overflow-x: hidden`. No browser, W3C validator, screenshot, responsive-layout, contrast, or accessibility inspection was performed.

## 2026-11-06 — Add course sources and prepare the team handoff

Tool: OpenAI Codex

Asked for: Read the five original course documents, reference them in the repository rules, replace the placeholder checklist with source-based requirements, create a three-person handoff plan with unknown details left as TODO, append the actual prompt, verify the documentation-only scope, and commit the task without pushing.

Kept: The five source files under their existing filenames, the selected static HTML/plain-CSS project decisions, the existing screen scaffolds, and all unrelated repository content.

Changed: Replaced the missing-source placeholders with the brief's screen features, eight exact “Fix these” issues, rubric checks, evidence requirements, and submission rules; added explicit source-reading rules and a role-based handoff plan.

Rejected: A read-only Word PDF import stalled without returning document text, so that path was stopped and the PDFs were read through their embedded local text and Unicode maps instead. No screen or CSS implementation was attempted.

By hand: Supplied the original course documents, reviewed the updated requirements and handoff plan, and confirmed the changes.

Checks: Confirmed the requirements directory contains exactly the five supplied filenames and calculated SHA-256 hashes; confirmed the source files are not ignored; read both text sources and all pages of the three PDFs; confirmed no HTML or CSS diff; counted exactly eight “Fix these” checklist items; checked the task-role/TODO structure; and compared Prompt 2 with the actual request for an exact textual match. No browser, W3C, responsive-layout, screenshot, contrast, or accessibility testing was performed.

## 2026-11-06 — Prepare developer handoff and screen requirements

Tool: OpenAI Codex

Asked for: Prepare a source-based screen contract, developer/leader handoff, branch and pull-request workflow, repository-readiness review, exact prompt record, and documentation-only commit for two developers.

Kept: The static HTML5/plain-CSS stack, all five unchanged course sources, the existing screen scaffolds, the shared spacing/breakpoint decisions, TODO team identities and allocations, and TBD self-assessment scores.

Changed: Added the screen contract and collaboration workflow; strengthened developer ownership, evidence, and leader integration requirements; and corrected existing documentation to show three team placeholders and that the brief/rubric are now available.

Rejected: The first readiness assertion required the literal phrase “no build” and falsely flagged equivalent README wording. The assertion was corrected and the complete review reran successfully; no project change was made to satisfy the faulty check.

By hand: Reviewed the screen contract and collaboration workflow, and confirmed the leader/developer responsibilities before handoff.

Checks: Confirmed 22 required files exist; resolved all four `href` paths on each HTML page and confirmed all three screen links; checked required files are not Git-ignored; checked static-stack consistency across README, AGENTS, PROTOTYPE, TASKS, and SCREEN-CONTRACT; confirmed the leader owns no screen and screen/shared-CSS ownership remains TODO; counted all eight “Fix these” items and required shared-data areas; confirmed all seven self-assessment scores and the total remain TBD; confirmed course sources, HTML, and CSS are unchanged; and matched Prompt 3 exactly. No browser, JavaScript-disabled rendering, responsive-layout, W3C, screenshot, contrast, or accessibility test was performed.

## 2026-11-08 — Complete the shared ClubFlow style system and static screen previews

Tool: OpenAI Codex with Superdesign.

Asked for: “use superdesign plugins - complete assets/css/styles.css: colour, font, spacing, component và responsive use together in the project.”

Kept: The approved neutral, trust-first direction with deep-blue actions; plain CSS; the 4/8/12/16/24/32/48/64 px scale; one club, one campaign, three screens, and a coherent campaign/interview timeline.

Changed: Replaced placeholder styling and markup with shared tokens, reusable responsive components, and static content for campaign creation, application review, and interview scheduling. The Superdesign draft included Tailwind CDN and Iconify CDN; those dependencies were not used in the project.

Rejected: CDN-loaded CSS/icons, generic identity marks, inconsistent/unsupported sample content, and JavaScript-only behavior were excluded to follow the project rules.

By hand: The user approved the visual direction. No team-authored implementation contribution has been recorded for this task.

Checks: Read the CSS/HTML diff and reconciled the campaign dates, application counts, shortlist totals, schedule rows, and conflict example by inspection. No automated tests, browser rendering, JavaScript-disabled check, responsive viewport inspection, W3C check, contrast measurement, or accessibility-pane review was run.


## 2026-11-08 — Verify, correct, and prepare ClubFlow PA2 screens for review

Tool: OpenAI Codex, Google Chrome (headless Chromium capture), W3C Nu HTML Checker, and W3C CSS Validator.

Asked for: “Tiêu chí Hoàn thành khi

- Đúng brief, semantic HTML; chạy khi tắt JS; đạt responsive 360/768/1280.
- Có 3 screenshot thực tế và kết quả W3C 0 lỗi.
- Cập nhật prompt, AI-log; commit gửi PR

Bạn hãy giúp tôi chạy, không dừng, sai thì quay lại sửa.”

Kept: The five supplied course sources, three-screen scope, static HTML/plain-CSS approach, relative navigation, existing sample content, and project changes already in progress.

Changed: Corrected invalid `aria-label` usage by labeling the relevant action groups, changed stat-only `<article>` elements to `<div>`, and moved the campaign two-column breakpoint from 768 px to 1280 px after screenshot inspection showed cramped content at tablet width. Shortened the sample campaign title to fit its field. Added actual responsive screenshots and saved W3C validator responses.

Rejected: No new runtime dependencies, frameworks, JavaScript interactions, or out-of-scope product functionality were added.

By hand: Reviewed the project brief/rubric requirements already documented in the project, inspected the tablet screenshot that exposed the cramped layout, and reviewed the corrected 768 px capture. No additional team-authored implementation contribution is recorded.

Contrast: Calculated WCAG relative-luminance ratios for the palette and button combinations: muted text on page 7.04:1; body text on white 16.40:1; brand link on white 7.92:1; white on the primary deep-blue button 12.37:1; warning/status pairs at least 7.66:1. These exceed 4.5:1.

Checks: Posted `index.html`, `review.html`, and `scheduling.html` to W3C Nu; each returned zero errors and zero warnings, saved under `checks/validator-*.txt`. W3C CSS Validator multipart upload returned HTTP 200, zero errors, and one informational warning that CSS variables are not statically checked; the vendor-extension warning was removed before the final validation. The clean result summary is saved as `checks/validator-css.txt`. Captured full-page Chrome screenshots at 360, 768, and 1280 px for all three pages with JavaScript disabled. All nine rendered pages reported one `h1`, no script elements, no page errors, 16 px body text, and no document-level horizontal overflow; standalone links/buttons met the 44 px minimum. The scheduling table scrolls inside its own wrapper at 360 and 768 px and fits at 1280 px. A first 768 px campaign capture exposed a cramped two-column layout; moved that breakpoint to 1280 px and recaptured.

## 2026-11-08 — Phase 1: Register the approved ClubFlow PA#2 wireframes

Tool: OpenAI Codex.

Asked for: Execute Phase 1 only by registering the three supplied approved Final PNG wireframes on `feat/pa2-finalize`, documenting their purpose and later wording correction, recording the actual prompt and AI work, verifying the result, and committing only those changes.

Kept: The three supplied PNG files byte-for-byte, their approved Final filenames, the existing repository history, current Git identity, static HTML/plain-CSS implementation, screenshots, checks, and all unrelated work.

Changed: Copied the three source PNGs from the repository root into `docs/design/`; added an English design README that maps them to the three implementation pages, distinguishes them from submission screenshots, records the requested future wording correction, and marks implementation alignment as pending; appended the actual prompt to `brief.md`.

Rejected: No images were regenerated, cropped, edited, substituted, or taken from unrelated locations. No HTML/CSS alignment work, backend behavior, Phase 2 work, browser testing, or W3C validation was performed.

By hand: No manual user review or team-authored implementation contribution was claimed for this phase.

Checks: Opened all three supplied source PNGs for visual identification; compared SHA-256 hashes and byte lengths between each source and destination; checked the README image links resolve; checked the design files are not Git-ignored; confirmed tracked HTML, CSS, existing screenshots, and existing checks have no diff; and inspected the final Phase 1 diff and staged paths before committing.
