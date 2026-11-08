# PA#2 Completion Checklist

The five course sources in `docs/requirements/` control this checklist. Check an item only after completing it and saving factual evidence where required.

## Course sources and fixed project decisions

- [x] Read `docs/requirements/requirement.txt`.
- [x] Read `docs/requirements/ClubFlow-final-project-brief.pdf`.
- [x] Read `docs/requirements/PA2-rubric-responsive-prototype.pdf`.
- [x] Read `docs/requirements/AI-LOG.md` as the course AI-log template.
- [x] Read `docs/requirements/SELF_ASSESSMENT_REPORT template.pdf` as the course self-assessment template.
- [ ] Keep the selected implementation stack: static HTML5 and plain CSS, with no build step or new dependency.
- [ ] Keep the prototype to one club, one active campaign, and one interview date for the campaign.
- [ ] Use the Executive main flow in this order: Create Recruitment Campaign → Application Review → Interview Scheduling.
- [ ] Keep all three screens tied to the same campaign and use coherent, realistic ClubFlow placeholder data rather than lorem ipsum.
- [ ] Include at least one deliberately long item, such as a long Vietnamese name or title, to test wrapping.

## Screen 1 — Create Recruitment Campaign (`index.html`)

- [ ] Provide campaign name, host club, description, opening date, closing date, and application instructions.
- [ ] Provide departments and positions with quotas, job descriptions, and requirements.
- [ ] Provide Save as Draft, Preview Campaign, and Publish Campaign actions.
- [ ] Show required-field and date validation behavior without discarding valid entered information.
- [ ] Keep the user on Screen 1 when publication data is invalid.
- [ ] After publication, provide a real relative Applications link to `review.html` for the same campaign.
- [ ] Do not imply that moving to Screen 2 creates applicants or approves applications.

## Screen 2 — Application Review (`review.html`)

- [ ] Show application/applicant statistics that agree with the visible sample records.
- [ ] Show applications, applicants, positions, submission times, and statuses.
- [ ] Provide the required search, filtering, sorting, pagination, and basic CSV export controls.
- [ ] Provide a Review control that opens application details beside the list.
- [ ] Keep both the list and details readable at every required width; the details must not cover most of the list.
- [ ] Show the selected CV, application details, and motivation statement.
- [ ] Provide an Executive-only internal note that is not presented as visible to Applicants or Interviewers.
- [ ] Provide Shortlist Candidate and Reject actions for the selected application.
- [ ] Update only the reviewed application; applications by the same student for other positions remain independent.
- [ ] Preserve the current filters when the details view closes.
- [ ] Provide a real relative Continue to Interview Scheduling link to `scheduling.html` when at least one application is Shortlisted.

## Screen 3 — Interview Scheduling (`scheduling.html`)

- [ ] Include only Shortlisted applications from the same campaign; Shortlisted must not mean finally accepted or already confirmed.
- [ ] Use configured interviewers, position assignments, interviewer availability, applicant availability, and existing rooms.
- [ ] Provide an interview date, time window, and one campaign-wide slot duration of 15, 20, or 30 minutes.
- [ ] Generate draft assignments using the first available valid combination of time, qualified interviewer, and room.
- [ ] Ensure each room hosts no more than one interview at a time.
- [ ] Prevent overlaps for applicants, interviewers, and rooms, including separate applications belonging to the same student.
- [ ] Label valid draft assignments Proposed.
- [ ] Label unscheduled applications Unassigned and show the actual reason; do not reject them automatically.
- [ ] Label genuine scheduling overlaps Conflict and identify the affected interviews.
- [ ] Ensure every status count agrees with the table rows.
- [ ] Provide Edit, Resolve, and + Assign Slot controls and recheck people, time, and room after each change.
- [ ] Provide Save Changes for the draft only and a schedule-table export control.
- [ ] Block confirmation until applications have closed, every application has been reviewed, every Shortlisted application has a valid assignment, and no Unassigned or Conflict item remains.
- [ ] Provide an approval summary before Approve & Confirm Schedule.
- [ ] After confirmation, show the Confirmed state and make campaign configuration, applications, and schedule read-only.
- [ ] Do not present schedule confirmation as the announcement of final recruitment results.

## The brief's eight “Fix these” requirements

- [ ] Use one coherent timeline; applications close before interviews, and dates agree across all three screens.
- [ ] Give Screen 2 the correct Application Review page title; do not retain Screen 1/Draft wording.
- [ ] Keep the Screen 2 list and details/drawer readable together at every width.
- [ ] Make every Screen 3 status count equal the visible schedule rows.
- [ ] Show only real scheduling conflicts whose overlapping assignments can be identified.
- [ ] Do not use the same sample person as both an applicant and an interviewer.
- [ ] Remove “Verified” student/attachment/credential claims because university account verification is out of scope.
- [ ] Do not include template footer content such as “© 2025 ClubFlow”, Privacy Policy, Terms of Service, or Support Center.

## Scope boundaries

- [ ] Do not add multiple clubs, simultaneous campaigns, self-service account registration/recovery, university verification, university SSO, or multi-level administration.
- [ ] Do not add dynamic room creation, capacity/booking management, external schedule checks, or large-scale schedule optimization.
- [ ] Do not add AI CV screening/ranking, advanced analytics, audit trails, or customizable application forms.
- [ ] Do not add post-recruitment events/member/task management, chat, video calls, payments, or a mobile application.
- [ ] Keep applicant submission/results and interviewer assessment views outside these three PA#2 screens; document any visible out-of-flow controls as not wired yet.

## Links, static content, and realistic behavior

- [ ] Use relative file links such as `review.html`, never `/review.html`, a directory route, `href="#"`, or an `onclick`-only navigation button.
- [ ] Use an anchor or a form submission with a real relative action for every main-flow transition.
- [ ] Open all pages directly from the folder and confirm all content remains visible with JavaScript disabled.
- [ ] Confirm any external resource requirements are accurately documented and the pages work under the stated network conditions.
- [ ] Confirm every visible action/state is an honest static prototype representation and is not described as implemented application functionality when it is not.

## Responsive checks at 360, 768, and 1280 px

- [x] Check every page at 360 px.
- [x] Check every page at 768 px.
- [x] Check every page at 1280 px.
- [x] At each width, confirm `document.documentElement.clientWidth` equals the selected viewport width.
- [x] At each width, confirm `document.documentElement.scrollWidth > document.documentElement.clientWidth` returns `false`.
- [ ] At each width, confirm the rubric's protruding-element query returns `[]`, except content intentionally contained by a table's own scrolling wrapper.
- [ ] Confirm nothing is cut off, clipped, or overlapping and long content wraps.
- [ ] Do not use `overflow-x: hidden` to conceal a layout defect.
- [x] At 360 px, confirm standalone buttons and links are at least 44 px tall.
- [ ] Confirm each layout changes appropriately between phone and laptop rather than stretching one narrow column.

## Semantic HTML, accessibility, and design checks

- [x] Use `header`, `nav`, `main`, and `footer` appropriately on every page.
- [x] Give every page exactly one `h1` and no skipped heading level.
- [x] Use buttons for actions and anchors/form submissions for navigation.
- [x] Give every input a visible associated label whose text activates the control.
- [ ] Give every image an appropriate `alt` value.
- [ ] Check the final heading outline and semantics in the browser Accessibility pane.
- [x] Run the W3C checker on `index.html`, achieve zero errors, and save the actual result.
- [x] Run the W3C checker on `review.html`, achieve zero errors, and save the actual result.
- [x] Run the W3C checker on `scheduling.html`, achieve zero errors, and save the actual result.
- [x] Keep body text at least 16 px.
- [ ] Confirm body text and buttons meet 4.5:1 contrast in the browser colour picker.
- [x] Use the documented spacing scale consistently with only justified exceptions.
- [x] Use no more than one CSS framework and no `!important` in custom CSS.
- [x] Give each page one clearly dominant element or action.

## Required full-page screenshots with JavaScript disabled

- [x] `screenshots/index-360.png`
- [x] `screenshots/index-768.png`
- [x] `screenshots/index-1280.png`
- [x] `screenshots/review-360.png`
- [x] `screenshots/review-768.png`
- [x] `screenshots/review-1280.png`
- [x] `screenshots/scheduling-360.png`
- [x] `screenshots/scheduling-768.png`
- [x] `screenshots/scheduling-1280.png`

## W3C evidence

- [x] `checks/validator-index.png` or `checks/validator-index.txt`
- [x] `checks/validator-review.png` or `checks/validator-review.txt`
- [x] `checks/validator-scheduling.png` or `checks/validator-scheduling.txt`

## Required English documents and honest evidence

- [ ] Complete `PROTOTYPE.md` with Team, How to open it, Screens, Your design choices, Not wired yet, and CSS sections.
- [ ] In `PROTOTYPE.md`, list every member's full name/student ID, each page and destination, the selected plain-CSS approach, spacing scale, breakpoints, and network requirement.
- [ ] Keep `brief.md` as the actual prompts in chronological order, not a reconstructed summary.
- [ ] Keep one timely, factual root `AI-LOG.md` entry per assistant task/page, using Tool, Asked for, Kept, Changed, Rejected, and By hand.
- [ ] Record actual failed checks and corrections in `AI-LOG.md` when they occur; do not invent a failure to improve the log.
- [ ] Complete `SELF_ASSESSMENT_REPORT.md` criterion by criterion with evidence pointing to real files, screenshots, checks, or commits.
- [ ] Include honest “What we did not manage” and “What we would do differently” sections.
- [ ] Make the self-assessment total equal the total in the submission ZIP filename.

## Git history, packaging, and submission

- [ ] Preserve the initial rules/scaffold commit.
- [ ] Create at least one focused implementation commit per screen, under the author identity of the member who did the work.
- [ ] Create a responsive-pass commit after actual multi-width work.
- [ ] Ensure the final ZIP contains the hidden `.git` directory and excludes `node_modules`.
- [ ] Name the ZIP `<StudentID1>-<StudentID2>-<StudentID3>_<total>.zip`, with student IDs in ascending order.
- [ ] Submit from the team member's `@student.hcmus.edu.vn` Google account.
- [ ] If team membership changed from PA#1, tell the lecturer before implementation.
- [ ] Ensure every team member can explain the submitted work, including assistant-written lines and how they were checked.
- [ ] Submit by Monday, November 9, 2026, 22:00 Vietnam time.
