# Self-assessment — PA#2

Submitted by:

| Full name | Student ID |
| --- | --- |
| Phan Lê Anh Minh | 24127082 |
| Hồ Phan Như Nguyệt | 24127211 |
| Huỳnh Thái Hoàng | 24127171 |

Total I claim: 98 / 100

| Criterion | Maximum score | Claimed score | Evidence |
|---|---:|---:|---|
| Three linked screens | 20 | 20 | `index.html`, `review.html`, and `scheduling.html` follow the required flow with real relative links and consistent ClubFlow data. |
| Responsive | 25 | 25 | Nine current full-page files in `screenshots/`; the latest cleanup checks at 360/768/1280 found no document overflow, clipping, overlap, short standalone targets, or footer omissions. |
| Semantic, valid HTML | 20 | 20 | Current official W3C file-upload results in `checks/validator-index.txt`, `checks/validator-review.txt`, and `checks/validator-scheduling.txt` report zero errors; browser checks found landmarks, one `h1`, and associated labels on every page. |
| Design you can check | 10 | 10 | `assets/css/styles.css` uses the documented spacing/color tokens, 16 px body text, visible focus, contained tables, two breakpoints, no `!important`, and no hidden-overflow workaround; approved references are in `docs/design/`. |
| Brief and rules file | 10 | 10 | `brief.md` records the actual prompts in order; `AGENTS.md` records the static stack, semantic/link rules, spacing scale, breakpoints, prohibited changes, and verification requirements. |
| AI-LOG.md | 10 | 10 | Entries identify tools and requests, specific kept/changed/rejected work, failed checks, responsive corrections, validator availability, and the recovered PDF verification. |
| Commit history | 5 | 3 | `.git` preserves scaffold, requirements, handoff, implementation, design, and Phase 2 commits, but the screen implementation is grouped rather than one focused commit per page plus a separate responsive-pass commit. |
| **Total** | **100** | **98** | Full implementation and current evidence are present; the deduction reflects the mixed implementation history. |

## What we did not manage

The existing history does not provide one focused implementation commit per page and a separate responsive-pass commit. The official CSS validator reports valid CSS with zero errors and one level-0 informational warning about variables not being statically checked. A dedicated browser Accessibility-pane review was not recorded; the final automated browser audit instead checked landmarks, heading order, labels, keyboard focus, target sizes, and JavaScript-disabled rendering.

## What we would do differently

Record team identity and ownership information in the required documents before final evidence work, make one focused commit per screen plus a distinct responsive pass, and generate final evidence immediately after the last source change so stale evidence never coexists with the current prototype.
