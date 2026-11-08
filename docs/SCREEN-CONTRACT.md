# ClubFlow PA#2 Screen Contract

This contract translates the five course sources in `docs/requirements/` into a shared implementation boundary for the two developers. It defines required content and consistency, not the final visual design or the actual sample values.

## Screen and file map

| File | Required ClubFlow screen | Executive's goal |
|---|---|---|
| `index.html` | Create Recruitment Campaign | Configure, preview, save, validate, and publish one recruitment campaign. |
| `review.html` | Application Review | Review each submitted application independently and decide whether it proceeds to interviews. |
| `scheduling.html` | Interview Scheduling | Generate, inspect, correct, approve, and confirm a valid schedule for Shortlisted applications. |

The three files represent one Executive, one club, and the same active campaign.

## `index.html` — Create Recruitment Campaign

Required UI content and states:

- Campaign name, host club, description, opening date, closing date, and application instructions.
- Departments and positions with quotas, job descriptions, and requirements.
- Controls for Save as Draft, Preview Campaign, and Publish Campaign.
- A visible representation of required-field and date validation that keeps valid entered information and keeps the Executive on the page when publication data is invalid.
- A Preview representation of what applicants would see.
- After the published state, an Applications link to `review.html` for the same campaign.
- Clear wording that publication enables later applicant submissions; navigating to Screen 2 does not create applications or approve them.

## `review.html` — Application Review

Required UI content and states:

- Application/applicant statistics that agree with the displayed records.
- An application list with applicant, position, submission time, and status.
- Search, filters, sorting, pagination, and basic CSV export controls.
- A Review control and a visible application-details area beside the list; the list and details must both remain readable at every required width.
- The selected applicant's CV representation, application details, and motivation statement.
- An Executive-only internal note, not presented as visible to Applicants or Interviewers.
- Shortlist Candidate and Reject controls for the selected application.
- Independent records and decisions for each application, including when one student applies to multiple positions.
- A representation of closing details while retaining the current filters.
- When at least one application is Shortlisted, a Continue to Interview Scheduling link to `scheduling.html`.

## `scheduling.html` — Interview Scheduling

Required UI content and states:

- Only Shortlisted applications from the same campaign. Shortlisted means passed CV screening, not finally accepted or already confirmed.
- Configured interviewers, the positions they can interview, interviewer availability, applicant availability, and existing rooms.
- One interview date, a time window, and one campaign-wide duration of 15, 20, or 30 minutes.
- A Generate Schedule control and a draft produced from the first available valid combination of time, qualified interviewer, and room.
- A schedule table with applicant/application, position, time, interviewer, room, and status.
- Proposed assignments, Unassigned applications with specific reasons, and genuine Conflict assignments with the affected overlap identifiable.
- Status totals that equal the visible rows.
- Edit, Resolve, and + Assign Slot controls, with a representation that people, time, and room are rechecked after changes.
- Save Changes for the draft and a schedule-table export control.
- An approval summary and Approve & Confirm Schedule control.
- Confirmation eligibility only after applications close, all applications are reviewed, every Shortlisted application has a valid assignment, and no Unassigned or Conflict item remains.
- A Confirmed state in which campaign configuration, applications, and schedule are read-only.
- Wording that schedule confirmation does not announce final recruitment results.

Scheduling constraints represented by the sample data:

- An interviewer must be qualified for the position.
- Applicant, interviewer, and room availability must overlap.
- A room hosts at most one interview at a time.
- An applicant, interviewer, or room cannot be assigned to overlapping interviews.
- Separate applications belonging to one student cannot have overlapping interviews.
- Missing valid combinations remain Unassigned; they are not rejected automatically.

## Relative navigation contract

- Shared navigation on every page uses relative anchors to `index.html`, `review.html`, and `scheduling.html`.
- The main-flow Applications action on `index.html` opens `review.html`.
- The main-flow Continue to Interview Scheduling action on `review.html` opens `scheduling.html`.
- `scheduling.html` is the end of the PA#2 flow; any back/navigation links still use the three real relative filenames.
- Main-flow navigation must not use absolute `/page.html` paths, directory routes, `href="#"`, or `onclick`-only buttons.
- Navigation is an `<a href>` or a form submission with a real relative `action` so it works when files are opened directly and JavaScript is disabled.

## Eight “Fix these” problems that must not appear

1. Dates do not fit together: use one timeline, with applications closing before interviews and all dates agreeing across the three pages.
2. Screen 2 has the wrong title: identify it as Application Review, not Create Recruitment Campaign or Draft Mode.
3. The Screen 2 details drawer covers most of the list: keep both readable at every required width.
4. Screen 3 counts do not add up: make summary/status totals equal the displayed table rows.
5. The Screen 3 conflict is not a real conflict: show an identifiable overlap between affected assignments.
6. Sample people overlap roles: do not use the same person as both an applicant and an interviewer.
7. “Verified” contradicts scope: do not claim verified students, attachments, credentials, or university verification.
8. The footer is template text: do not include “© 2025 ClubFlow”, Privacy Policy, Terms of Service, or Support Center.

## Static prototype versus working application

PA#2 uses the repository's selected static HTML5/plain-CSS stack. The pages must show all assessed content when opened directly with JavaScript disabled. Main-flow links must actually open the destination files.

The static prototype must visibly represent the required controls, information, states, validation messages, decision outcomes, scheduling eligibility, conflicts, confirmation gates, and read-only result using coherent sample content. It must not claim that data was really stored, generated, uploaded, exported, sent, or authenticated.

Working backend behavior is not required or implemented here, including persistence, authentication/role enforcement, file upload, live search/filter/sort/pagination, CSV/timetable generation, drawer scripting, validation processing, independent decision storage, schedule generation/conflict calculation, confirmation locking, notifications, or a database. These are represented by static UI and sample states only.

## Shared data agreement required before coding

The two developers must record and agree on these items before parallel implementation. The visual design and actual sample values remain their choice.

| Shared area | Agreement required |
|---|---|
| Campaign identity | One campaign ID/name, one host club, description, instructions, and consistent Draft/Published context. |
| Timeline | Opening date, closing date, submission times, one interview date after closing, and a schedule time window. |
| Departments and positions | Department/position names, quotas, job descriptions, requirements, and which interviewers qualify for each position. |
| Applications | Application IDs, applicants, position per record, submission times, screening status, motivation/CV details, and at least one student with separate applications to demonstrate independent decisions. |
| Interviewers | People distinct from applicants, qualified positions, and availability that supports the intended Proposed/Conflict/Unassigned examples. |
| Rooms | Existing room names and availability; no room may host overlapping interviews. |
| Counts | Campaign quotas, application/applicant statistics, Shortlisted inputs, schedule row count, and Proposed/Conflict/Unassigned totals must reconcile across pages. |
| Stress-test content | At least one long Vietnamese name or long title that must wrap without causing page overflow. |

Implementation status: the final shared values and visual direction are represented consistently in the three HTML pages and summarized in `PROTOTYPE.md`. The repository does not record an authoritative per-developer ownership allocation, so none is inferred here.
