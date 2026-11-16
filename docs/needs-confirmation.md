# Needs confirmation

Internal review list prepared 2026-11-16. No website content was changed during this discovery stage.

## Required before anything is published

- **Sanitized resume:** `public/resume.pdf` contains a phone number. Do not serve or link the current file. Replace it with a sanitized copy before deployment.
- **Confidential CRM project:** The source describes an internal CRM/contact-center application, but does not establish ownership or public-release permission. Keep its name and business unnamed unless Miguel approves public naming.
- **Company product names:** Confirm that the Legal Monitoring System, MailX, and associated employer/product names may be named publicly. The proposed summaries can stay generic until that is clear.
- **Employee ID system:** The source repository was not found. Confirm that the project and its workflow/integration details may be described publicly before adding it to the site.

## Evidence gaps

- No source checkout for the employee ID system was found under the projects root. Its stack, features, and contribution claims are resume-supported only; no code or Git history was available to cross-check.
- No portfolio application source or package manifest exists in this directory. There is no current framework to keep or rebuild; the recommended starting point is the requested Next.js App Router stack, after approval.
- No `assets-incoming` directory exists. No sanitized product screenshots were available.
- Active/archived labels are guesses based on checked-out HEAD dates, not checks of deployed services: Legal Monitoring System (2026-11-12–13), MailX repositories (2026-11-03), confidential CRM (2026-11-12).
- Several repositories contain additional unrecognized author-email identities with at least 10 commits. No addresses or names are recorded here; these commits were not credited, and totals use only the three identities supplied in `AGENTS.md`.
- No measured performance, adoption, delivery, or business-impact metrics were verified. Omit such claims unless separate evidence is provided.
- Prisma, Supabase, Cloudinary, and BytePlus AI were not found in the scanned project repositories. OpenAI is present as a dependency but active use was not verified. Vercel appears in starter/analytics material, but an actual deployment was not verified.
- The resume does not explain whether 1.0 or a larger number is the highest GWA. `AGENTS.md` supplies the authoritative clarification: 1.0 is the highest grade. Preserve that wording whenever the GWA is displayed.

## Naming and privacy review

- Legal case and client/bank names, court or borrower details, real records, and actual system screenshots must remain private.
- Mail campaign recipient/lead details, raw event payloads, sender settings, and internal analytics must remain private.
- The confidential CRM project's client/business name, account and agent records, exact report/disposition definitions, internal hosts, credentials, and source code must remain private.
- Employee data, headshots, completed IDs, HR decisions, and internal service configuration from the employee ID system must remain private.
- Do not put unapproved client names, internal URLs, customer data, commit messages, other contributors' names/emails, or proprietary code in the site or these docs.
