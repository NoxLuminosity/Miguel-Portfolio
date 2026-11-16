# Needs confirmation

Internal review list prepared 2026-11-16. No website content was changed during this discovery stage.

## Required before anything is published

- **Sanitized resume:** `public/resume.pdf` contains a phone number. Do not serve or link the current file. Replace it with a sanitized copy before deployment.
- **Confidential CRM project:** The source describes an internal CRM/contact-center application, but does not establish ownership or public-release permission. Keep its name and business unnamed unless Miguel approves public naming.
- **Company product names:** Confirm that the Legal Monitoring System, MailX, and associated employer/product names may be named publicly. The proposed summaries can stay generic until that is clear.
- **Employee ID system:** The linked repository labels the project confidential. Confirm employer permission before publishing even a generic description; do not copy its reported metrics or organization-specific setup details.

## Evidence gaps

- No local checkout for the employee ID system was found. Its public GitHub source was reviewed read-only. The README labels the project confidential and includes outcome claims without supporting measurement evidence; do not reuse those claims in portfolio copy.
- The linked employee ID repository has 139 distinct commits reachable from four branches, all authored under one of the three supplied identities. File-path contribution areas were checked for 138 commits; one commit's file list was unavailable. The README describes a team effort, so commit share must not be presented as sole authorship. Current deployment status was not checked.
- No portfolio application source or package manifest exists in this directory. There is no current framework to keep or rebuild; the recommended starting point is the requested Next.js App Router stack, after approval.
- No `assets-incoming` directory exists. No sanitized product screenshots were available.
- Active/archived labels are guesses based on checked-out HEAD dates, not checks of deployed services: Legal Monitoring System (2026-11-12–13), MailX repositories (2026-11-03), confidential CRM (2026-11-12), employee ID system (2026-02-24, GitHub archive flag is false).
- Several repositories contain additional unrecognized author-email identities with at least 10 commits. No addresses or names are recorded here; these commits were not credited, and totals use only the three identities supplied in `AGENTS.md`.
- No measured performance, adoption, delivery, or business-impact metrics were verified. Omit such claims unless separate evidence is provided.
- Prisma was not found in the scanned project repositories. Supabase, Cloudinary, and BytePlus AI are backed by the employee ID repository. OpenAI is present as a dependency but active use was not verified. Vercel configuration exists, but a live deployment was not verified.
- The resume does not explain whether 1.0 or a larger number is the highest GWA. `AGENTS.md` supplies the authoritative clarification: 1.0 is the highest grade. Preserve that wording whenever the GWA is displayed.

## Naming and privacy review

- Legal case and client/bank names, court or borrower details, real records, and actual system screenshots must remain private.
- Mail campaign recipient/lead details, raw event payloads, sender settings, and internal analytics must remain private.
- The confidential CRM project's client/business name, account and agent records, exact report/disposition definitions, internal hosts, credentials, and source code must remain private.
- Employee data, headshots, completed IDs, HR decisions, and internal service configuration from the employee ID system must remain private.
- Do not put unapproved client names, internal URLs, customer data, commit messages, other contributors' names/emails, or proprietary code in the site or these docs.
