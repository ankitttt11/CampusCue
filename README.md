# CampusCue — Make Room to Think

**Challenge:** DevOps Department Web Design Challenge  
**Selected track:** Track 03 — Micro-service Design for a Unique Idea  
**Project title:** CampusCue — Make Room to Think

## Problem statement
College students often track assignments, lab work, projects, and exam preparation across scattered chats and notes. CampusCue gives them one simple place to capture deadlines and see what needs attention first.

## Target user
College students managing several coursework deadlines at once, especially students who want a lightweight planner without creating an account.

## What makes it useful
CampusCue is deliberately narrow: capture a deadline, see the work ordered by due date and priority, and choose a next step. It requires no account, backend, API key, or third-party library. Tasks persist in the current browser using `localStorage`.

## Core journey
1. Enter a task title, due date, category, and priority.
2. Add it to the plan and receive visible confirmation.
3. Review the task list, deadline labels, summary counts, and suggested next steps.
4. Filter between all, active, and completed tasks.
5. Mark a task complete, undo completion, delete it, or clear completed tasks.
6. Refresh the page to confirm that tasks remain in the same browser profile.

## Key states and feedback
- **Empty state:** explains how to get started.
- **Success feedback:** toast message after adding, completing, undoing, or deleting a task.
- **Error/limitation feedback:** storage failure message if browser storage cannot be written.
- **Completed state:** completed tasks are visually subdued and can be restored to active.
- **Overdue state:** overdue dates are allowed and shown with an overdue label.
- **Filtered states:** All, Active, and Done have an accessible pressed state.

## Technology stack
- HTML5
- CSS3 (responsive layout, focus-visible styles, reduced-motion support)
- Vanilla JavaScript
- Browser `localStorage`
- No package installation or external runtime dependencies

## Run locally
From this directory, open a terminal and run:

```bash
python -m http.server 8000
```

Then open <http://localhost:8000>. Stop the server with `Ctrl+C`.

You can also open `index.html` directly in a modern browser. A local server is preferable for consistent browser behaviour.

## Deployment
See [PUBLISHING.md](PUBLISHING.md) for step-by-step GitHub repository and GitHub Pages instructions. The project is a static site and can also be hosted by another static hosting provider.

## Walkthrough
See [WALKTHROUGH.md](WALKTHROUGH.md) for a short screen-recording script and screenshot checklist.

## Known limitations
- Tasks are saved only in the current browser profile on the current device; there is no cross-device sync, account, or cloud backup.
- Clearing browser site data can remove saved tasks.
- Suggestions use due date and priority only; they are not an AI-generated timetable and do not know course workload or estimated task duration.
- No reminders, notifications, or calendar integration are included.
- Browser interaction testing and public deployment must be completed and verified before final submission; see `TEST_REPORT.md` for the checks performed in this working environment.

## Assets and credits
The visual illustration is made with CSS and text. No external images, fonts, or third-party UI libraries are required.

## AI assistance disclosure
AI assistance was used to help develop and refine the code and documentation. The candidate should review the code, run the application, test the interactions, and be ready to explain the implementation and design decisions, as required by the challenge guidelines.
