# Lincroft Little League Field Requests

A standalone prototype for managing field-use requests and approvals for Lincroft Little League.

## Purpose

Managers submit requests for practices, games, makeups, clinics, or other field use. A designated field scheduler then approves or denies each request. Only approved reservations appear on the official field calendar.

The core policy supported by this project is:

> A submitted field request is not a reservation until the field scheduler approves it.

## Prototype features

- Manager-style field request form
- Team, event type, field, date/time, lights, opponent, and notes
- Approved reservation calendar grouped by field
- Scheduler request queue
- Approve and deny actions with optional decision notes
- Basic overlap checks against approved reservations
- Suggested same-time alternate fields
- Browser-local data persistence with `localStorage`
- Responsive layout for desktop and mobile browsers

## Run locally

This prototype has no installation or server requirement.

1. Clone or download this repository.
2. Open `index.html` in a modern browser.
3. Submit a request from **Request a Field**.
4. Review and decide it from **Scheduler Queue**.
5. View approved reservations under **Field Calendar**.

The prototype stores submitted requests only in the current browser's local storage. Different devices and browsers do not share data.

## Current limitations

This is an interactive prototype, not a production multi-user application. It intentionally does not yet include:

- User authentication or manager-specific permissions
- Shared cloud database
- Real notification delivery
- Configurable field availability, blackout dates, or maintenance closures
- Database-level locking to prevent simultaneous approval conflicts
- Production audit logs and reporting
- Sports Connect or other scheduling-system integration

## Production roadmap

1. Add a hosted database, authentication, roles, teams, and field administration.
2. Enforce field availability, division restrictions, booking windows, buffers, and blackout dates.
3. Add email and optional SMS notifications for submissions, approvals, denials, changes, and cancellations.
4. Add a manager portal for viewing and cancelling their own requests.
5. Add recurring practices, rainout workflows, alternate-time proposals, waitlists, and usage reports.
6. Add optional downstream schedule integrations after the internal field-approval workflow is proven.

## Suggested stack

- Frontend: React / Next.js
- API: FastAPI (Python) or Node.js / TypeScript
- Database and authentication: PostgreSQL with Supabase
- Calendar UI: FullCalendar
- Email notifications: Resend, Postmark, or SendGrid
- Hosting: Vercel plus Supabase

## Governance decisions to make

Before a production launch, league leadership should define the single final approver and backup, field-use priority order, booking window, cancellation rules, buffers, prime-time fairness approach, field blackouts, and weather/rainout procedures.

## License

Private internal project for Lincroft Little League.