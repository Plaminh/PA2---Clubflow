# ClubFlow Figma Wireframe Plan

Status: historical pre-implementation plan. The approved raster references now live in `docs/design/`, and the implemented alignment status is recorded in `docs/design/README.md`. The unchecked review list below preserves the original planning record rather than asserting current incompleteness.

## Purpose

Prepare a responsive, reviewable wireframe for the three PA#2 Executive screens before implementation: Create Recruitment Campaign, Application Review, and Interview Scheduling. The wireframe will make the main flow and the information hierarchy clear while staying within the course brief and the repository's static HTML5 and plain CSS constraints.

## Source decisions

- Follow the three-screen sequence: Create Recruitment Campaign → Application Review → Interview Scheduling.
- Keep one Executive, one club, one active campaign, and one interview date throughout the frames.
- Use a single coherent timeline: application closing happens before the interview date.
- Represent realistic sample data and visible states; do not imply backend behavior or add screens outside PA#2.
- Preserve the existing plain CSS direction and responsive checks at 360 px, 768 px, and 1280 px.
- Use the course brief's required features and avoid all eight “Fix these” problems.

## Figma file structure

Create one Figma page named `PA2 Wireframes` with sections in flow order. Use three frame groups, one per screen. Each group contains a 360 px mobile frame, a 768 px tablet frame, and a 1280 px desktop frame. Name frames consistently, for example `01 Campaign / 360`, `01 Campaign / 768`, and `01 Campaign / 1280`.

Add a compact flow strip above the groups linking the three screen names in order. Add an annotation area for decisions and non-functional controls. Keep wireframe styling grayscale with one restrained accent for primary actions and status chips; defer detailed visual branding until the structure is approved.

## Screen content and layout

### 1. Create Recruitment Campaign

- Shared application shell and campaign context; title the screen clearly.
- Campaign form: campaign name, host club, description, opening and closing dates, and application instructions.
- Recruitment setup: departments with their positions, each showing quota, job description, and requirements.
- Interview preparation area: one interview date and the available slots applicants may select, consistent with the later schedule.
- Clearly distinguish `Save as Draft`, `Preview Campaign`, and `Publish Campaign`.
- Add an annotated invalid-publish state showing required-field/date feedback while preserving entered values and keeping the Executive on this screen.
- Add a published state with an `Applications` link to Screen 2. Label sample applications as later submissions; navigation itself does not create or approve them.

### 2. Application Review

- Correct page title: `Application Review`.
- Campaign identity and consistent close date, then summary statistics whose totals reconcile with the sample records.
- Search and filter/sort controls, a paginated application list, and CSV export affordance.
- Keep the list and selected application details visible together on desktop and tablet. On mobile, stack the list and details as readable sections; do not use an overlay that hides most of the list.
- Details include applicant, position, submission time, status, CV representation, and motivation statement.
- Show an Executive-only internal note area and annotate its restricted audience.
- Provide `Shortlist Candidate` and `Reject` actions. Include a sample student with applications to two positions to communicate that each record has an independent decision.
- Annotate the closed-details/list state as retaining current filters.
- Show `Continue to Interview Scheduling` when at least one sample application is Shortlisted.

### 3. Interview Scheduling

- Campaign identity, interview date, time window, and one shared duration choice of 15, 20, or 30 minutes.
- Show scheduling inputs/context: qualified interviewers, their availability, applicant availability, and existing rooms.
- Schedule table with application/applicant, position, time, interviewer, room, and status. Ensure status totals equal the rows.
- Wireframe a valid `Proposed` assignment, an `Unassigned` row with its concrete reason, and a genuine `Conflict` example identifying the overlapping assignments.
- Include `Generate Schedule`, `Edit`, `Resolve`, `+ Assign Slot`, `Save Changes`, and schedule export controls.
- Add an approval summary and `Approve & Confirm Schedule` gate. Annotate that confirmation is blocked until applications are closed, every application is reviewed, every Shortlisted application has a valid assignment, and no Unassigned or Conflict rows remain.
- Add a separate `Confirmed` state that is read-only. State that schedule confirmation is not the final recruitment result announcement.

## Responsive behavior to draw

- **360 px:** one-column content, compact but readable campaign sections, stacked review list/details, and a schedule table shown in an explicitly labeled horizontal-scroll region if needed. Buttons and standalone links need room for a 44 px minimum target in implementation.
- **768 px:** use a two-column form or review composition where content remains readable; keep schedule controls and table from colliding.
- **1280 px:** use the available width for a clear form/detail split and a readable schedule table; keep one dominant action per screen.
- Include one deliberately long Vietnamese name or title in sample data and show its wrapping behavior.
- Wireframe layout changes by breakpoint rather than stretching the mobile column.

## Shared data to establish before drawing detailed states

Use one campaign name/club and a common date set across all three screens. Define departments and positions, application IDs and applicants, submission timestamps and decisions, qualified interviewers and their availability, existing rooms, and the schedule rows. Reconcile applicant/application statistics and Proposed/Unassigned/Conflict counts against the visible records. Keep applicant names distinct from interviewer names. Where project-owner sources leave product behavior undefined, flag the question for clarification instead of inventing scope.

## Review checklist

- [ ] All three frames describe the same campaign and coherent timeline.
- [ ] The three screens appear in the required main-flow order.
- [ ] Required content and controls for each screen are represented.
- [ ] Review details never obscure most of the application list.
- [ ] Scheduling examples demonstrate genuine constraints and reconciled counts.
- [ ] No frame implies student verification, out-of-scope features, or final results at schedule confirmation.
- [ ] No template footer items appear.
- [ ] The 360, 768, and 1280 layouts have intentional responsive differences.
- [ ] Long Vietnamese content wraps inside the frame.

## Handoff

Review this plan before creating the Figma wireframes. After approval, create the frames and annotate their sample data and static prototype states. The Figma artifact is a design reference; implementation remains three static HTML pages with the existing plain CSS approach.
