# ClubFlow Prototype Notes

## 1. Team

- TODO — Full name — Student ID
- TODO — Full name — Student ID
- TODO — Full name — Student ID

## 2. How to open it

Open `index.html` directly in a browser. The prototype uses local static HTML and CSS and needs no build step, server, or network connection.

## 3. Screens

| File | Source screen | User goal | Main-flow link |
|---|---|---|---|
| `index.html` | Create Recruitment Campaign | Prepare one campaign, recruitment positions, application dates, and interview availability. | `review.html` opens Application Review. |
| `review.html` | Application Review | Inspect sample applications and make an independent screening decision for one application. | `scheduling.html` opens Interview Scheduling. |
| `scheduling.html` | Interview Scheduling | Review a schedule draft, resolve its sample conflicts/unassigned item, and see the confirmation gate. | `review.html` returns to Application Review. |

## 4. Your design choices

- The Executive workflow uses one club and one recruitment campaign across all pages.
- The same timeline is used throughout: applications open 12/10/2026, close 30/10/2026, and interviews take place 05/11/2026.
- Application review keeps the selected details beside the list; the mobile layout stacks the sections.
- Scheduling shows a real same-applicant overlap and an Unassigned reason. The visible totals match the four shortlisted sample records.
- A restrained neutral palette, deep-blue actions, and reusable cards, fields, status labels, and table styles create a consistent administration interface.

## 5. Not wired yet

- Campaign draft saving, preview, publication, and form validation. The visible invalid and published panels are labelled static state examples; navigation does not create, approve, or persist application records.
- Live application search/filter/sort/pagination, CSV export, closing the detail panel, note saving, and application decision updates. The CF-026 fictional sample CV is the one wired local document link on this screen.
- Schedule generation, assignment edits, conflict recalculation, schedule export, and confirmation/read-only behavior. The confirmed panel is a labelled alternate-state example.
- Authentication, data persistence, back-end behavior, and actions outside the three PA#2 screens.

## 6. CSS

Plain CSS, with no framework or dependency. The shared spacing scale is 4, 8, 12, 16, 24, 32, 48, and 64 px. The layout is mobile-first, with breakpoints at 768 px and 1280 px. The local stylesheet provides the color and type tokens, responsive shell, form controls, cards, action buttons, status badges, alerts, and a contained scrolling table wrapper.
