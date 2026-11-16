# Project inventory

Internal discovery notes prepared 2026-11-16. These notes are not site copy. The scan was read-only; no other project was installed, built, run, or changed.

## Scope and counting method

The projects root contains three related Legal Monitoring System checkouts, separate MailX frontend and backend repositories, and one confidential CRM/contact-center application. The three Legal Monitoring System checkouts have identical histories, so their statistics are reported once. No local employee ID system checkout was found; the user later provided its public GitHub repository, which was reviewed read-only.

Contribution counts use all reachable Git refs. For the GitHub-hosted employee ID repository, all four branches were checked and no tags were present; local repositories were counted with all refs. In each repository, commits from the three identities supplied in `AGENTS.md` were combined and deduplicated by commit hash. Shares are the credited commits divided by that repository's distinct reachable commits. Contribution areas below come from paths in those commits, not commit messages. Other author identities are not credited.

| Project / repository grouping | My commits / total | Share | Latest checked-out HEAD | Additional uncredited identities with 10+ commits |
| --- | ---: | ---: | --- | ---: |
| Legal Monitoring System (three identical-history checkouts) | 870 / 5,122 | 17.0% | 2026-11-12–13 | 8 |
| MailX backend | 246 / 1,302 | 18.9% | 2026-11-03 | 5 |
| MailX frontend | 149 / 915 | 16.3% | 2026-11-03 | 7 |
| Confidential CRM/contact-center application (name withheld) | 173 / 1,662 | 10.4% | 2026-11-12 | 21 |
| Employee ID registration system (GitHub repository) | 139 / 139 | 100.0% | 2026-02-24 | 0 |

The extra-identity counts are an author-statistic only. Their identities are omitted, and their commits are excluded from Miguel's totals under the supplied attribution rule. Do not add the three Legal Monitoring System checkout rows together: their commit histories are the same.

## Legal Monitoring System

- **Category:** Production legal case operations platform; company work.
- **Purpose and business problem:** Coordinates cases through staged legal workflows, with required documents, status transitions, access controls, and operational history in one system.
- **Verified stack:** Next.js App Router, React, TypeScript, Tailwind CSS, PostgreSQL, Node.js services, Vitest, Testing Library, and Playwright. The repository documents Lark authentication/calendar services and S3-compatible object storage.
- **Main features:** Pre-Legal, Filing, Compliance, and Execution workflows; stage-specific document requirements; case imports; audit and status history; bulk operations; operational/compliance reporting; hearing/calendar support; role-aware access.
- **Architecture:** Next.js pages and API routes call shared domain, workflow, and database services. PostgreSQL is authoritative. A separate report-export worker and integrations handle background/export or external-service work.
- **Integrations:** Lark SSO and calendar/notification services; S3-compatible storage. PostgreSQL schema evolution is maintained through migration files.
- **Engineering complexity:** High. Multiple workflow stages share authorization, policy, audit, persistence, and document boundaries while supporting different product profiles.
- **Verifiable contributions:** 870 of 5,122 commits (17.0%) in each of the three identical-history checkouts. Paths show work across UI, API/domain services, migrations/schema, tests and end-to-end checks, CI, integrations, and report-worker tooling.
- **Problems solved:** Makes workflow progression, required information, access decisions, and case history more consistent and traceable; supports bulk and reporting work for legal operations.
- **Status guess:** Active. The three checked-out HEADs are dated 2026-11-12–13, and the workflow catalog has a review date of 2026-11-13. This is repository activity, not a live deployment check.
- **Public-safe summary proposal:** “Contributed to a legal operations platform spanning case intake, filing, compliance, and execution. Built workflow, document-readiness, access-control, history, and reporting features.”
- **Privacy and naming:** This is employer/company work. Keep bank, client, court, borrower, and case names or data private, along with internal URLs, real screenshots/documents, deployment details, credentials, and proprietary implementation details. Confirm permission before naming the employer or specific product publicly.

## MailX

- **Category:** Production email-campaign processing and delivery analytics; company work.
- **Purpose and business problem:** Supports campaign execution and processes delivery events so operators can monitor campaign state, delivery, and analytics.
- **Verified stack:** Backend: Python, FastAPI, Celery, Redis, Kafka, ClickHouse, PostgreSQL, and SendGrid integration. Frontend: Next.js, React, TypeScript, Tailwind CSS, Ant Design, and charting libraries. Docker Compose and Grafana are present in the repository documentation/configuration.
- **Main features:** Campaign execution and scheduling, webhook/event ingestion, background processing, delivery monitoring, analytics, deduplication, sender routing, and dashboard views.
- **Architecture:** The Next.js frontend calls backend APIs. A webhook receiver sends provider events to Kafka; background services process campaigns and events; ClickHouse serves analytics and PostgreSQL retains raw event data. Grafana is available for operational views.
- **Integrations:** SendGrid, Kafka, ClickHouse, PostgreSQL, Redis, and Grafana.
- **Engineering complexity:** High. The platform spans user-facing workflows, asynchronous campaign work, event ingestion, message buffering, multiple data stores, and operational monitoring.
- **Verifiable contributions:** Backend: 246 of 1,302 commits (18.9%); paths show backend APIs/services, worker and webhook code, schema/data work, tests, and CI. Frontend: 149 of 915 commits (16.3%); paths show UI/API and integration areas plus CI.
- **Problems solved:** Connects campaign operations with asynchronous sending and delivery-event visibility, while supporting analytics and processing reliability.
- **Status guess:** Active. Both repositories' checked-out HEADs are dated 2026-11-03. This does not independently verify current production status.
- **Public-safe summary proposal:** “Developed features across an email-campaign platform, including campaign workflows, event processing, delivery monitoring, and analytics.”
- **Privacy and naming:** This is employer/company work. Keep recipient and lead data, email addresses, event payloads, sender configuration, internal analytics, service URLs, credentials, and proprietary processing rules private. Confirm permission before publicly naming the product or employer.

## Confidential CRM/contact-center application (name withheld)

- **Category:** Internal CRM and contact-center workflow application; may be company or client work.
- **Purpose and business problem:** The repository describes a web system for account work, calling-system handoff, call dispositions, imports, and operational reports.
- **Verified stack:** Next.js, React, TypeScript, Tailwind CSS, FastAPI, PostgreSQL, SQLAlchemy, Alembic, Celery, Redis, MinIO, and Nginx. The backend includes a read-only adapter to an existing contact-center database.
- **Main features:** Role-based account and call workflows, dialer handoff, inbound-call and callback handling, dispositions, messaging, imports, and reporting. These details are source-derived and are not approved site copy.
- **Architecture:** Next.js frontend and FastAPI backend use PostgreSQL for application state; Celery/Redis provide background processing; MinIO stores files; Nginx routes the containerized application. A separate read-only adapter connects to the calling system's database.
- **Integrations:** Existing contact-center/calling system, PostgreSQL, Redis, MinIO, and Lark authentication services.
- **Engineering complexity:** High. This is a multi-service application with several user roles, call workflows, background jobs, migrations, file storage, and an external system boundary.
- **Verifiable contributions:** 173 of 1,662 commits (10.4%). Paths show frontend, backend/API, worker/integration, and migration/schema work.
- **Problems solved:** Brings account and calling workflows, disposition tracking, imports, and reporting into a role-aware application integrated with an existing calling system.
- **Status guess:** Active. The checked-out HEAD is dated 2026-11-12. This is repository activity, not a live deployment check.
- **Public-safe summary proposal:** “Built role-based CRM and contact-center workflows that connect a web application to calling infrastructure, background processing, and reporting.”
- **Privacy and naming:** The source describes an internal CRM, but local evidence does not establish whether it is company-owned or client work. Treat it as potentially confidential. Do not name the project, client, or business without approval. Keep account/agent/customer information, exact disposition and report definitions, internal URLs/hosts, deployment details, credentials, sample records, and proprietary code private.

## Employee ID registration and automation system

- **Category:** Internal HR workflow project built during an internship; company work.
- **Source:** [Public GitHub repository](https://github.com/NoxLuminosity/Employee-ID-Registration-System). The README describes the project as confidential; a public repository does not establish permission to reuse its details in a portfolio.
- **Purpose and business problem:** Automates employee ID requests, HR review, image preparation, and print-ready card delivery.
- **Verified stack:** FastAPI and Uvicorn; Jinja2 templates and vanilla JavaScript; Supabase PostgreSQL with SQLite for local development; Cloudinary; BytePlus Seedream; Lark OAuth and data/messaging services; Vercel serverless configuration. The dependency manifest confirms FastAPI, Jinja2, Supabase, and Cloudinary; the README and deployment config document the other integrations.
- **Main features:** Employee submission and status tracking, HR review/approval, an ID gallery, image processing, card/PDF generation, and routed delivery/notifications. These are source-derived internal details, not approved site copy.
- **Architecture:** FastAPI application with server-rendered templates, static frontend assets, API modules, and a serverless entry point. SQLite supports local development; Supabase PostgreSQL is the documented production database. External services handle identity/data sync, image processing, AI image work, and notifications.
- **Integrations:** Lark identity/data/messaging, Cloudinary image handling, BytePlus Seedream, Supabase, and Vercel.
- **Engineering complexity:** Medium to high by the documented scope: one web application spans employee and HR workflows, role checks, several integrations, image handling, document generation, and multiple database modes. Runtime behavior was not tested.
- **Verifiable contributions:** 139 of 139 commits reachable from four GitHub branches (100.0% by the three supplied author identities). Changed-file paths in 138 commits show backend/API, Jinja/static frontend, schema, automation scripts, and tests. One commit's file list was unavailable, so this area list may omit a touched path category. No high-volume unfamiliar author identities were found. The README describes a team project; commit share does not imply sole authorship.
- **Problems solved:** Brings employee ID intake, review, image preparation, and delivery into a tracked workflow, based on the repository description.
- **Status guess:** Archived/dormant. GitHub does not mark the repository archived, but its latest commit is dated 2026-02-24 in Asia/Manila; current use and deployment were not checked.
- **Public-safe summary proposal:** “Contributed to an internal HR tool for employee ID applications, review, image preparation, and print-ready output.” Use only after employer approval; the source README labels the project confidential.
- **Privacy and naming:** Treat as high-risk company work. Do not name the employer or expose employee records, headshots, completed IDs, department/branch routing rules, internal setup details, credentials, third-party contributor identities, README outcome claims, or proprietary implementation details without explicit approval.

## Portfolio app audit

- The portfolio directory contains the supplied `AGENTS.md` and `public/resume.pdf`; no application source, package manifest, or existing UI was found.
- No current framework or design system exists to keep, so there is no existing stack to rebuild. Recommendation: after approval, create the portfolio in this directory with the requested Next.js App Router, TypeScript, and Tailwind stack.
- No `assets-incoming` directory exists. Use clearly labeled architecture illustrations until sanitized real screenshots are provided.
- `public/resume.pdf` contains a phone number. Do not expose or link this PDF as-is; a sanitized resume is needed before anything is deployed.

## Resume skills cross-check

“Repo-backed” below means the technology appears in project manifests, project documentation, configuration, or source structure. This confirms repository evidence, not proficiency level.

| Resume skill | Evidence in scanned projects |
| --- | --- |
| Python, TypeScript, JavaScript, SQL, Bash/Shell, HTML/CSS | Repo-backed across backend and frontend source/configuration. |
| Next.js, React, Tailwind CSS, FastAPI, REST APIs, Celery | Repo-backed across the LCMS, MailX, and confidential CRM source/configuration. |
| PostgreSQL, ClickHouse, Redis, Kafka | Repo-backed in manifests, architecture docs, and database/configuration layout. |
| Docker, Docker Compose, Git, Linux/SSH, Grafana, SonarQube | Repo-backed in deployment/configuration docs and project tooling. |
| GitHub Actions | Workflow configuration exists in the scanned repositories; contributions are also visible in CI paths. |
| SendGrid, Lark API | Repo-backed in integration docs, manifests, and architecture. |
| Prisma | No evidence found in the scanned project repositories; this skill appears only in the resume/authoritative project facts. |
| OpenAI API | Listed as a backend dependency, but an active integration was not verified; treat actual use as resume-supported only. |
| Supabase, Cloudinary, BytePlus AI | Repo-backed in the employee ID system's dependency manifest, README, and deployment configuration. |
| Vercel | Repo-backed by the employee ID system's deployment config and instructions; an actual live deployment was not verified. |

Education and employment dates are supplied as authoritative facts in `AGENTS.md`. The resume prints the GWA as 1.56 / 1.0 without explaining the scale direction; whenever used, include the supplied clarification that 1.0 is the highest grade.
