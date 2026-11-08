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

## 2026-11-08 — Phase 2: Complete the ClubFlow PA#2 static prototype

Tool: OpenAI Codex and Microsoft Edge in headless mode.

Asked for: Complete the three-screen static prototype from the approved visual references while preserving the plain HTML/CSS stack, maintaining a coherent cross-screen data contract, documenting the actual work, and stopping before staging, committing, pushing, merging, or Phase 3 evidence generation.

Kept: The static HTML5/plain-CSS architecture, shared deep-blue visual direction and spacing scale, three-screen scope, real relative navigation, approved reference images, course source files, existing screenshots, existing validator records, repository history, and current branch.

Changed: Expanded the campaign screen with the long campaign identity, timeline, complete recruitment data, static validation example, readable preview, and a clearly labelled published-state example. Expanded Application Review with six coherent application records, five distinct candidates, accurate status totals, filters, one-page pagination, full sample statement, honest unavailable-CV control, labelled notes, and per-application decision affordances. Expanded Interview Scheduling with date/time/duration and room controls, interviewer assignments, four eligible applications, one proposed/two conflict/one unassigned draft states, blocking conditions, and a separate confirmed/read-only example. Updated shared CSS for the responsive layouts and corrected the design README links to the currently registered image filenames. Added the actual Phase 2 prompt to `brief.md`.

Rejected: No dependencies, JavaScript, backend, persistence, working filter/export/scheduling logic, fabricated CV file, or invented dynamic state changes were added. Existing submission screenshots and saved validator checks were not overwritten.

By hand: No manual user review, approval, or team-authored implementation contribution is claimed for this phase.

Checks: Inspected all nine temporary Edge captures at 360, 768, and 1280 px with JavaScript execution disabled. The first browser pass exposed document-level overflow on the scheduling page at 360 and 768 px; CSS intrinsic sizing was corrected and all nine pages were recaptured. The final pass reported one `h1`, zero script elements, 16 px body text, no document-level horizontal overflow, no elements protruding outside the viewport except tables contained by their scroll wrappers, and no standalone links or buttons below 44 px. Checked relative links and assets, form-label associations, HTML landmarks, forbidden navigation/CSS patterns, and cross-screen campaign dates, position mappings, IDs, counts, and statuses. Recalculated the active foreground/background palette pairs: all exceeded 4.5:1, with the lowest checked ratio at 7.66:1. W3C Nu validation was attempted, but the service returned a Cloudflare challenge rather than validation results, so no W3C result is claimed. The temporary review captures were kept outside the repository and are not submission evidence.

Evidence status: The existing files under `screenshots/` and `checks/` describe the earlier implementation and are now stale. They need to be regenerated and reviewed in Phase 3; they were left unchanged in this phase.

## 2026-11-08 — Phase 2 finishing pass: fictional CV and concise interface notes

Tool: OpenAI Codex, Microsoft Edge in headless mode, and the local PyMuPDF parser.

Asked for: Finish Phase 2 by adding a clearly labelled synthetic CF-026 sample CV, moving repetitive implementation explanations into `PROTOTYPE.md`, and rechecking the Review screen at 360, 768, and 1280 px with JavaScript disabled.

Kept: The existing CF-026 application identity, static HTML/plain-CSS architecture, application data, alternate-state labels, responsive layout, existing submission evidence, current branch, and Git history.

Changed: Added a one-page local PDF labelled as a fictional sample and containing only synthetic information, including an `.invalid` contact address and fictional organization/project names. Replaced the disabled CV placeholder with a real relative link. Removed repetitive static-behavior explanations from the interfaces and consolidated the unwired behavior in `PROTOTYPE.md` while retaining concise labels for invalid, published, and confirmed examples. Appended the actual finishing prompt to `brief.md`.

Rejected: No real personal data, identity verification claim, external document, JavaScript behavior, dependency, backend feature, Phase 3 evidence, or fabricated check result was added. No manual user review or approval is claimed.

By hand: No team-authored implementation contribution is recorded for this task.

Checks: Confirmed the PDF header is `%PDF-1.4`; opened it with the local PDF parser as a one-page document; extracted its fictional-data labels and synthetic `.invalid` address; rendered the page and visually inspected the result. Edge accepted the local PDF URL with exit code 0, but its headless built-in PDF viewer produced a blank screenshot, so that screenshot was not treated as visual proof. Checked every local `href` and `src` target. Loaded `review.html` directly from disk in Edge at 360, 768, and 1280 px with page JavaScript disabled; each final run had one `h1`, zero scripts, 16 px body text, no document-level horizontal overflow, no protruding elements, and no standalone links or buttons below 44 px. The local CV link resolved to the intended PDF at every width. Review captures remained outside the repository, and existing `screenshots/` and `checks/` were not changed.

## 2026-11-08 — Phase 2 final Publish-state correction and recheck

Tool: OpenAI Codex and Microsoft Edge controlled through the browser debugging protocol.

Asked for: Correct the invalid campaign publication example so it includes an associated field error and a visibly disabled native Publish button, then rerun the three-page responsive regression checks without JavaScript and stop before committing or Phase 3 evidence work.

Kept: The static HTML/plain-CSS architecture, existing enabled draft actions, separate published-state example, Review and Scheduling markup and data, current branch, staged changes, submission screenshots, and saved validator evidence.

Changed: Replaced the invalid-state explanatory alert in `index.html` with a clearly labelled alternate state containing an empty description field, a visible associated validation error, and a real `button` with the native `disabled` attribute. Reused the existing shared disabled-button CSS treatment instead of adding a one-off rule. Appended the actual correction prompt to `brief.md`.

Rejected: No JavaScript, dependency, backend behavior, publishing logic, unrelated page rewrite, screenshot regeneration, validator regeneration, commit, push, or branch switch was performed.

Checks: Loaded all three pages from the local HTTP server in Edge at exact 360, 768, and 1280 px viewport widths with page JavaScript disabled. Checked the full document through the footer, document overflow, non-table protrusion, content clipping, interactive overlap, standalone button/link height, labels, heading count, body text size, font loading, long-name wrapping, table containment, application and scheduling statistics, and keyboard focus entry. Activated the relative navigation links with native pointer input. Confirmed the invalid field is labelled and references its visible error, the Publish button matches `:disabled`, uses the shared disabled colors and `not-allowed` cursor, is skipped by keyboard navigation, and emits no click event under native pointer input. Opened all three pages through `file:` URLs at 360 px and confirmed no document overflow and relative navigation destinations. Source inspection confirmed the project HTML contains no script elements; the local development server injects its own reload script. During the final pre-commit check, compared the working-tree and staged CV bytes with the previously approved recovered Git blob; all matched exactly. PyMuPDF opened the `%PDF-1.4` file as a valid one-page document, extracted CF-026 and Nguyễn Minh Anh, and rendered the page successfully. The Review link returned HTTP 200 with `application/pdf`, and a native browser click opened the PDF in Edge's viewer, where the fictional banner and applicant content rendered correctly.

Result: The requested campaign-state correction and all nine responsive browser cases passed. The approved fictional CV is restored, staged, byte-identical to Git blob `b0d3d1bf32031474c05ddb06b90584d180af58e7`, and verified through both PyMuPDF and the browser. No remaining Phase 2 implementation blocker was found. Current W3C results, submission screenshots, and self-assessment remain Phase 3 work and were not treated as UI failures.

## 2026-11-08 — Phase 3: Validation, documentation, and submission evidence

Tool: OpenAI Codex, the official W3C Nu HTML Checker, and Microsoft Edge controlled through the browser debugging protocol.

Asked for: Complete Phase 3 without changing the approved implementation: run current official HTML validation, generate and inspect nine JavaScript-disabled full-page screenshots, finalize the required English documents and self-assessment, audit repository/submission readiness, record the exact prompt and actual work, and stop before committing or creating the ZIP.

Kept: The final Phase 2 HTML/CSS and fictional CV, approved wireframes, three-screen scope, static plain-CSS architecture, coherent sample data, existing Git history, current branch, and all unrelated work.

Changed: Replaced stale HTML-validator records with current official file-upload results; regenerated all nine required full-page screenshots from the final Phase 2 source; updated the project and design READMEs, `PROTOTYPE.md`, the completion checklist, and `SELF_ASSESSMENT_REPORT.md`; appended the exact Phase 3 prompt to `brief.md`; and recorded this Phase 3 entry.

Rejected: No design or implementation change, dependency, JavaScript, backend feature, invented team identity, fabricated validation result, history rewrite, commit, push, or submission ZIP was made. The blocked current CSS-validator attempt is not reported as a passing result.

By hand: The assistant visually inspected all nine regenerated screenshots for complete-page capture, footer inclusion, blank/missing content, clipping, overlap, wrapping, and table containment. No manual user review, team-authored contribution, or browser Accessibility-pane review is claimed.

Checks: Submitted `index.html`, `review.html`, and `scheduling.html` to the official W3C Nu file-upload endpoint; each returned HTTP 200 and the success result with zero errors and zero warnings. With page JavaScript disabled, loaded each page directly from disk at exact 360, 768, and 1280 px viewport widths, captured the complete document, and checked one `h1`, semantic landmarks, 16 px body text, associated visible form labels, footer inclusion, no document-level horizontal overflow, no non-table protrusion or clipping, no overlapping standalone controls, and no standalone mobile target below 44 px. Long Vietnamese names wrapped where space required, and wide scheduling tables remained inside their own scrolling wrappers. Rechecked relative targets, current source/evidence consistency, the fictional PDF header/content/renderability, required files, CSS restrictions, Git history, and packaging structure. The official CSS validator returned HTTP 403 behind a Cloudflare challenge, so current CSS validation is recorded as not verified. The repository still lacks team names/student IDs, preventing an honest final roster and exact ZIP filename; the self-assessment claims 98/100 with a two-point history deduction.

## 2026-11-08 — Phase 4: Final audit and submission preparation

Tool: OpenAI Codex, Microsoft Edge controlled through the browser debugging protocol, PyMuPDF, and the official W3C Nu HTML Checker.

Asked for: Independently audit the final committed PA#2 implementation, evidence, documentation, rubric score, and ZIP readiness; make no implementation/evidence/history changes; and stop before committing, pushing, or creating the ZIP.

Kept: The committed HTML/CSS implementation, fictional CV, approved references, all nine Phase 3 screenshots, all validator evidence, the 98/100 claimed score, existing commits and authorship, and the current branch.

Changed: Appended the exact Phase 4 prompt; corrected current self-assessment text that still described the now-present committed team roster as missing; reconciled the completion checklist with checks actually performed; clarified the historical status of the screen contract and handoff plan; and added this audit entry. Historical AI-log statements were not rewritten because they describe what was known when those checks ran.

Rejected: No new feature, redesign, HTML/CSS/PDF/screenshot/validator change, dependency, invented identity, manufactured commit, history rewrite, stage, commit, push, or ZIP creation was made. The self-assessment total was not changed before user review.

By hand: The assistant visually inspected all nine committed screenshots again. No manual user review, team oral-readiness check, submission-account check, or completed submission is claimed.

Checks: Confirmed Phase 3 is commit `a1ba4f5` and the worktree was clean at audit start. Loaded all three committed pages directly from disk with page JavaScript disabled at exact 360, 768, and 1280 px browser widths. All nine cases had no document overflow, non-table protrusion, overlapping controls, unlabeled visible inputs, missing landmarks, heading skips, missing CSS, or mobile standalone target below 44 px; native keyboard focus had a visible 3 px outline, and scheduling tables remained contained and horizontally scrollable where required. Native link activation followed Campaign → Review → Scheduling and back, and the Review CV link opened the local PDF URL. PyMuPDF opened/rendered the one-page `%PDF-1.4` file and extracted CF-026 and Nguyễn Minh Anh. Source parsing confirmed 6 applications, 5 applicants, 4 Shortlisted, 1 Pending Review, 1 Rejected, plus 1 Proposed, 2 Conflict, and 1 Unassigned, with the 30/10/2026 deadline and 05/11/2026 interview date on all pages. All nine PNGs are valid, have filename-matching widths, include their footers, and were visually complete. The three saved W3C records report HTTP 200 and zero errors/warnings; a fresh read-only official cross-check also returned success/empty message arrays. Alternating checker versions 26.11.4 and 26.11.5 appeared across separate current requests, which is consistent with the public validator serving requests through backends on adjacent versions rather than evidence alteration. CSS validation remains honestly NOT VERIFIED. The committed team tables consistently identify Phan Lê Anh Minh (24127082), Hồ Phan Như Nguyệt (24127211), and Huỳnh Thái Hoàng (24127171), allowing the proposed current-claim filename `24127082-24127171-24127211_98.zip`. The independent rubric estimate is 97/100 because the actual prompt/rules record does not explicitly require an Accessibility-pane check; the separate two-point commit-history deduction remains supported.

## 2026-11-08 — Final source refactoring and repository cleanup

Tool: OpenAI Codex, Microsoft Edge controlled through the browser debugging protocol, the official W3C Nu HTML Checker, and the official W3C CSS Validator.

Asked for: Audit and safely simplify the final ClubFlow PA#2 source and repository without redesigning it, preserve optional documentation pending approval, synchronize evidence after any source change, append the actual prompt, and stop before committing or packaging.

Kept: The three-screen static HTML/plain-CSS architecture, all semantic landmarks and accessibility attributes, campaign/application/scheduling data, responsive layout, relative navigation, fictional CV, approved wireframes, team identities, claimed score, optional documents, Git history, and the six pre-existing unstaged Phase 4 documentation changes.

Changed: Removed the unused `.placeholder`, `.field-label`, `.control`, and `[aria-disabled="true"]` CSS hooks; removed the unstyled `application-detail` class; reformatted dense timeline, statistics, application-list, and confirmed-schedule markup without changing its element structure or text; clarified current-versus-historical workflow/status wording in the repository documentation; corrected the checklist's viewport-gutter wording and stale ZIP-identity note; updated the current CSS-validation statement in the self-assessment; regenerated all nine screenshots; refreshed the official validator records; and appended the exact cleanup prompt to `brief.md`.

Rejected: Shared layout wrappers, generic media safeguards, component grouping, optional planning/contract/checklist documents, and approved assets were not removed because their current or historical purpose remains useful. No visual redesign, data change, JavaScript, dependency, branch change, commit, push, history rewrite, document deletion, or ZIP creation was performed.

By hand: The assistant visually inspected all nine regenerated screenshots and reviewed the final source/documentation diff. No manual user review or new team-authored contribution is claimed.

Checks: Mapped every CSS class against all three HTML files and rechecked every local HTML and Markdown reference. Loaded all three pages directly from disk with JavaScript disabled at 360, 768, and 1280 px. All nine final cases had the exact requested `window.innerWidth`, no document overflow, non-table protrusion, overlap, unlabeled visible control, missing landmark, missing stylesheet, or mobile target below 44 px; keyboard Tab focus showed the 3 px focus ring, and scheduling tables stayed inside focusable scroll wrappers. Native links completed Campaign → Review → Scheduling and back; all local targets, including the fictional CV, resolved. The visible data remained 6 applications / 5 applicants / 4 Shortlisted / 1 Pending / 1 Rejected and 1 Proposed / 2 Conflict / 1 Unassigned. An initial audit predicate incorrectly equated viewport width with `clientWidth` despite Edge's vertical-scrollbar gutter; it was corrected to test `window.innerWidth` and `scrollWidth <= clientWidth`, after which all nine cases passed. The regenerated images were visually complete and pixel-identical to the Phase 3 baseline. The official Nu checker returned zero messages for all three final HTML files; one later review file-upload retry received a transient HTTP 403, while the unchanged current review file had already passed its file-upload check and the official structured retry again returned an empty message array. The official CSS validator reported valid CSS, zero errors, and one level-0 informational warning that variables are not statically checked.
