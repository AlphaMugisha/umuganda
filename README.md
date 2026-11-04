# Clean Kigali — Community Sanitation Reporting

## Overview

Clean Kigali is a web service for reporting and managing public sanitation problems in Kigali. Residents can submit a report in Kinyarwanda, English, or French, receive a reference code, and check its status later. City staff use an authenticated dashboard to review and manage reports.

**Stack:** Node.js 20+, TypeScript, Express, EJS, MySQL/MariaDB (`mysql2`), bcryptjs, Helmet, and express-session.

## Mission

Make it easier for residents to report sanitation issues and help responsible teams track, prioritize, and resolve them.

## Goals

- Provide a multilingual public reporting portal.
- Give each submitted report a reference code for follow-up.
- Let authorized staff triage and update report statuses.
- Display meaningful public statistics without exposing reporter details.
- Protect administrative actions with authentication, session controls, and CSRF protection.
- Keep the service usable even when browser JavaScript is unavailable for core report submission.

## Technology and commands

Requirements: Node.js 20+ and a MySQL/MariaDB database.

```bash
npm install
npm run dev
npm run typecheck
npm run build
npm start
```

Configure the required environment variables using the provided `.env.example`. Keep real database passwords and session secrets in a private local environment file, never in Git.

## Repository structure

- `src/` — TypeScript server, routes, middleware, and shared logic
- `views/` — EJS templates
- `public/` — browser assets served to visitors
- `scripts/` — project scripts
- `reports.sql` — report-related SQL
- `PROJECT_SUMMARY.md` — detailed project history, routes, security notes, and architecture
- `_archive/` — archived legacy materials

## Development priorities

Maintain the privacy and security boundaries described in `PROJECT_SUMMARY.md`, test the report submission and tracking workflows, and keep the language strings consistent across all supported locales.
