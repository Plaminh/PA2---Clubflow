# PA#2 Completion Checklist

The five course sources in `docs/requirements/` control this checklist. Check an item only after completing it and saving factual evidence where required.

## Course sources and fixed project decisions

- [x] Read `docs/requirements/requirement.txt`.
- [x] Read `docs/requirements/ClubFlow-final-project-brief.pdf`.
- [x] Read `docs/requirements/PA2-rubric-responsive-prototype.pdf`.
- [x] Read `docs/requirements/AI-LOG.md` as the course AI-log template.
- [x] Read `docs/requirements/SELF_ASSESSMENT_REPORT template.pdf` as the course self-assessment template.
- [x] Keep the selected implementation stack: static HTML5 and plain CSS, with no build step or new dependency.
- [x] Keep the prototype to one club, one active campaign, and one interview date for the campaign.
- [x] Use the Executive main flow in this order: Create Recruitment Campaign → Application Review → Interview Scheduling.
- [x] Keep all three screens tied to the same campaign and use coherent, realistic ClubFlow placeholder data rather than lorem ipsum.
- [x] Include at least one deliberately long item, such as a long Vietnamese name or title, to test wrapping.

## Screen 1 — Create Recruitment Campaign (`index.html`)

- [x] Provide campaign name, host club, description, opening date, closing date, and application instructions.
- [x] Provide departments and positions with quotas, job descriptions, and requirements.
- [x] Provide Save as Draft, Preview Campaign, and Publish Campaign actions.
- [x] Show required-field and date validation behavior without discarding valid entered information.
- [x] Keep the user on Screen 1 when publication data is invalid.
- [x] After publication, provide a real relative Applications link to `review.html` for the same campaign.
- [x] Do not imply that moving to Screen 2 creates applicants or approves applications.

## Screen 2 — Application Review (`review.html`)

- [x] Show application/applicant statistics that agree with the visible sample records.
- [x] Show applications, applicants, positions, submission times, and statuses.
- [x] Provide the required search, filtering, sorting, pagination, and basic CSV export controls.
- [x] Provide a Review control and a visible application-details representation beside the list.
- [x] Keep both the list and details readable at every required width; the details do not cover most of the list.
- [x] Show the selected CV, application details, and motivation statement.
- [x] Provide an Executive-only internal note that is not presented as visible to Applicants or Interviewers.
- [x] Provide Shortlist Candidate and Reject actions for the selected application.
- [x] Represent decisions as application-specific; the same student's other application remains independent.
- [x] Document filter preservation and detail closing as not wired in this static prototype rather than claiming dynamic behavior.
- [x] Provide a real relative Continue to Interview Scheduling link to `scheduling.html` when at least one application is Shortlisted.

## Screen 3 — Interview Scheduling (`scheduling.html`)

- [x] Include only Shortlisted applications from the same campaign; Shortlisted is not presented as finally accepted or already confirmed.
- [x] Use configured interviewers, position assignments, interviewer availability, applicant availability, and existing rooms.
- [x] Provide an interview date, time window, and one campaign-wide slot duration of 15, 20, or 30 minutes.
- [x] Represent draft assignments using coherent time, qualified-interviewer, and room data; generation logic is documented as not wired.
- [x] Ensure each room hosts no more than one interview at a time in the sample states.
- [x] Identify applicant/interviewer/room overlap constraints, including separate applications belonging to the same student.
- [x] Label valid draft assignments Proposed.
- [x] Label unscheduled applications Unassigned and show the actual reason; do not reject them automatically.
- [x] Label genuine scheduling overlaps Conflict and identify the affected interviews.
- [x] Ensure every status count agrees with the table rows.
- [x] Provide Edit, Resolve, and + Assign Slot controls; dynamic rechecking is documented as not wired.
- [x] Provide Save Changes for the draft only and a schedule-table export control.
- [x] Block the represented confirmation state while a Pending Review, Conflict, or Unassigned condition remains.
- [x] Provide a confirmation-condition summary before the disabled confirmation control.
- [x] Show a separate Confirmed/read-only state with disabled editing controls.
- [x] Do not present schedule confirmation as the announcement of final recruitment results.

## The brief's eight “Fix these” requirements

- [x] Use one coherent timeline; applications close before interviews, and dates agree across all three screens.
- [x] Give Screen 2 the correct Application Review page title; do not retain Screen 1/Draft wording.
- [x] Keep the Screen 2 list and details/drawer readable together at every width.
- [x] Make every Screen 3 status count equal the visible schedule rows.
- [x] Show only real scheduling conflicts whose overlapping assignments can be identified.
- [x] Do not use the same sample person as both an applicant and an interviewer.
- [x] Remove “Verified” student/attachment/credential claims because university account verification is out of scope.
- [x] Do not include template footer content such as “© 2025 ClubFlow”, Privacy Policy, Terms of Service, or Support Center.

## Scope boundaries

- [x] Do not add multiple clubs, simultaneous campaigns, self-service account registration/recovery, university verification, university SSO, or multi-level administration.
- [x] Do not add dynamic room creation, capacity/booking management, external schedule checks, or large-scale schedule optimization.
- [x] Do not add AI CV screening/ranking, advanced analytics, audit trails, or customizable application forms.
- [x] Do not add post-recruitment events/member/task management, chat, video calls, payments, or a mobile application.
- [x] Keep applicant submission/results and interviewer assessment views outside these three PA#2 screens; document visible static controls and states as not wired yet.

## Links, static content, and realistic behavior

- [x] Use relative file links such as `review.html`, never `/review.html`, a directory route, `href="#"`, or an `onclick`-only navigation button.
- [x] Use an anchor or a form submission with a real relative action for every main-flow transition.
- [x] Open all pages directly from the folder and confirm all content remains visible with JavaScript disabled.
- [x] Confirm no external resource is required and the pages work without a network connection.
- [x] Confirm every visible action/state is an honest static prototype representation and is not described as implemented application functionality when it is not.

## Responsive checks at 360, 768, and 1280 px

- [x] Check every page at 360 px.
- [x] Check every page at 768 px.
- [x] Check every page at 1280 px.
- [x] At each width, confirm `window.innerWidth` equals the selected viewport width; account for the browser's vertical-scrollbar gutter when interpreting `document.documentElement.clientWidth`.
- [x] At each width, confirm `document.documentElement.scrollWidth > document.documentElement.clientWidth` returns `false`.
- [x] At each width, confirm the rubric's protruding-element query returns `[]`, except content intentionally contained by a table's own scrolling wrapper.
- [x] Confirm nothing is cut off, clipped, or overlapping and long content wraps.
- [x] Do not use `overflow-x: hidden` to conceal a layout defect.
- [x] At 360 px, confirm standalone buttons and links are at least 44 px tall.
- [x] Confirm each layout changes appropriately between phone and laptop rather than stretching one narrow column.

## Semantic HTML, accessibility, and design checks

- [x] Use `header`, `nav`, `main`, and `footer` appropriately on every page.
- [x] Give every page exactly one `h1` and no skipped heading level.
- [x] Use buttons for actions and anchors/form submissions for navigation.
- [x] Give every input a visible associated label whose text activates the control.
- [x] Give every image an appropriate `alt` value (the implementation pages contain no content images).
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

- [x] Complete `PROTOTYPE.md` with Team, How to open it, Screens, Your design choices, Not wired yet, and CSS sections; the Team section lists all three committed names and student IDs.
- [x] In `PROTOTYPE.md`, list every member's full name/student ID, each page and destination, the selected plain-CSS approach, spacing scale, breakpoints, and network requirement.
- [x] Keep `brief.md` as the actual prompts in chronological order, not a reconstructed summary.
- [x] Keep one timely, factual root `AI-LOG.md` entry per assistant task/page, using Tool, Asked for, Kept, Changed, Rejected, and By hand.
- [x] Record actual failed checks and corrections in `AI-LOG.md` when they occur; do not invent a failure to improve the log.
- [x] Complete `SELF_ASSESSMENT_REPORT.md` criterion by criterion with evidence pointing to real files, screenshots, checks, or commits.
- [x] Include honest “What we did not manage” and “What we would do differently” sections.
- [ ] Make the self-assessment total equal the total in the submission ZIP filename (team IDs are available; ZIP intentionally not created yet).

## Git history, packaging, and submission

- [x] Preserve the initial rules/scaffold commit.
- [ ] Create at least one focused implementation commit per screen, under the author identity of the member who did the work.
- [ ] Create a responsive-pass commit after actual multi-width work.
- [ ] Ensure the final ZIP contains the hidden `.git` directory and excludes `node_modules` (repository structure checked; ZIP intentionally not created yet).
- [ ] Name the ZIP `<StudentID1>-<StudentID2>-<StudentID3>_<total>.zip`, with student IDs in ascending order.
- [ ] Submit from the team member's `@student.hcmus.edu.vn` Google account.
- [ ] If team membership changed from PA#1, tell the lecturer before implementation.
- [ ] Ensure every team member can explain the submitted work, including assistant-written lines and how they were checked.
- [ ] Submit by Monday, November 9, 2026, 22:00 Vietnam time.
