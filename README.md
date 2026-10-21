# StudyPilot AI — NEURA X 2026 Prototype

StudyPilot AI is a mobile-friendly academic task-agent prototype. It demonstrates the workflow **collect → extract → verify → plan → act → adapt**.

## Features in this prototype
- Responsive dashboard and mobile navigation
- Task list with priorities, due dates, completion and delete actions
- Academic inbox with a sample notice and editable extracted-task review
- Local `.txt` notice parsing for candidate tasks (dates must be checked by the user)
- Draft study planner with adjustable daily availability
- Rule-based demo assistant for priorities, plans and upcoming deadlines
- Progress dashboard, settings, JSON export, and local browser persistence

## Run it
This is a static website with no build step:
1. Download or clone this repository.
2. Open `index.html` in a browser, or serve this folder with any static web server.
3. For GitHub Pages: open repository **Settings → Pages**, choose **Deploy from a branch**, select `main` and `/ (root)`, then save.

## Important prototype limits
- PDF and image extraction are not connected to an AI backend yet. The upload UI explains this; `.txt` parsing and the sample notice work locally.
- The assistant is rule-based demo logic, not a live LLM.
- Tasks are stored in this browser's `localStorage`; they are not synced between devices.
- Notifications are in-app only. No emails, phone notifications, or college integrations are sent.
- The extraction parser is a convenience demo, not a reliable date parser. Verify every extracted field before saving.

## Next implementation stage
Add a Python FastAPI backend with secure file handling, PDF/OCR extraction, structured-output LLM integration, source offsets, date-conflict checks, authenticated persistence, and tests. Keep AI-generated actions behind server-side validation and explicit user approval.

## Tech
HTML, CSS, vanilla JavaScript, browser `localStorage`, no third-party runtime dependencies. Google Fonts are optional; the app falls back to system fonts if unavailable.

## Competition
Problem statement: **AI Task Agent**. This repository is an original prototype scaffold for NEURA X 2026 and should be expanded, tested, and documented with the team's own contributions before submission.
