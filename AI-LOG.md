# AI-LOG.md — ClubFlow PA#2

## 2026-11-06 — Initialize the ClubFlow repository scaffold

Tool: OpenAI Codex

Asked for: Inspect the workspace, initialize Git when needed, and create a static HTML5 and plain-CSS scaffold with three linked pages, shared rules, required documentation, evidence placeholders, verification, and one setup commit.

Kept: The requested static stack, file structure, three minimal page scaffolds, shared navigation, CSS foundation, documentation sections, pending checklist, and Git workflow.

Changed: Selected plain CSS because the repository had no existing CSS choice, and adapted the nearby course-style documentation templates to the ClubFlow PA#2 headings and pending evidence requirements.

Rejected: None.

By hand: None reported; no manual authorship or testing is attributed to the user in this entry.

Checks: Confirmed the required scaffold paths existed; compared the prompt recorded in `brief.md` with the supplied prompt for an exact textual match; inspected each HTML source for its expected title, viewport, semantic landmarks, exactly one `h1`, and resolvable relative links; checked the CSS source for both required breakpoints and the absence of `!important` and `overflow-x: hidden`. No browser, W3C validator, screenshot, responsive-layout, contrast, or accessibility inspection was performed.

## 2026-11-06 — Add course sources and prepare the team handoff

Tool: OpenAI Codex

Asked for: Read the five original course documents, reference them in the repository rules, replace the placeholder checklist with source-based requirements, create a three-person handoff plan with unknown details left as TODO, append the actual prompt, verify the documentation-only scope, and commit the task without pushing.

Kept: The five source files under their existing filenames, the selected static HTML/plain-CSS project decisions, the existing screen scaffolds, and all unrelated repository content.

Changed: Replaced the missing-source placeholders with the brief's screen features, eight exact “Fix these” issues, rubric checks, evidence requirements, and submission rules; added explicit source-reading rules and a role-based handoff plan.

Rejected: A read-only Word PDF import stalled without returning document text, so that path was stopped and the PDFs were read through their embedded local text and Unicode maps instead. No screen or CSS implementation was attempted.

By hand: None reported; the user supplied the original course documents, and no manual authorship or testing is attributed to the user.

Checks: Confirmed the requirements directory contains exactly the five supplied filenames and calculated SHA-256 hashes; confirmed the source files are not ignored; read both text sources and all pages of the three PDFs; confirmed no HTML or CSS diff; counted exactly eight “Fix these” checklist items; checked the task-role/TODO structure; and compared Prompt 2 with the actual request for an exact textual match. No browser, W3C, responsive-layout, screenshot, contrast, or accessibility testing was performed.
