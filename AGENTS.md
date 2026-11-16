# Portfolio project rules

## Who this is for
Miguel L. Manuel's personal developer portfolio. Audience: recruiters,
engineering managers, prospective clients.

## Facts (source of truth, do not embellish)
- Name: Miguel L. Manuel
- Public email: manuelmiguel0726@gmail.com
- GitHub: https://github.com/NoxLuminosity
- LinkedIn: https://www.linkedin.com/in/miguelmanuel0726/
- Resume file: /public/resume.pdf. Never publish my phone number anywhere.
- Education: B.S. Computer Engineering, Pamantasan ng Lungsod ng Maynila,
  Sep 2022 - Aug 2026, Cum Laude, Dean's List 2022-2026.
  GWA 1.56 (1.0 is the highest grade). Always include that clarification.
- Experience at S.P. Madrid and Associates Law Firm:
  - Full Stack Developer, Full-Time, Jul 2026 - Present
  - Full Stack Developer, Freelance/Contract, Mar 2026 - Jun 2026
  - AI Prompt Engineer / Full Stack Developer Intern, Jan 2026 - Feb 2026
- Resume summary of the work: I develop and maintain two production platforms,
  the Legal Monitoring System (legal case operations) and MailX (email
  campaign processing). Legal work: Pre-Legal, Filing, Compliance, Execution
  workflows, status transitions, document requirements, audit/revert
  histories, bulk operations, compliance reporting, hearing features, RBAC,
  PostgreSQL schema changes/migrations/indexes. MailX work: Celery, Redis,
  Kafka, ClickHouse, SendGrid for campaign execution, webhook/event
  ingestion, analytics, delivery monitoring, deduplication, sender routing.
  Also deployments, production incident support, GitHub Actions CI/CD,
  testing, SonarQube remediation, access-control fixes, performance work.
  Internship: Employee ID Registration and Automation System (FastAPI,
  Jinja2, JavaScript, Supabase PostgreSQL, SQLite) with HR review/approval,
  ID gallery, print-ready ID generation, integrating BytePlus Seedream AI,
  Cloudinary, background removal, and Lark auth/data services.
- Skills (resume-verified):
  Languages: Python, TypeScript, JavaScript, SQL, Bash/Shell, HTML/CSS
  Frontend/Backend: Next.js, React, Tailwind CSS, FastAPI, REST APIs, Celery
  Data/Messaging: PostgreSQL, Prisma, ClickHouse, Redis, Kafka, Supabase
  DevOps/Tools: Docker, Docker Compose, GitHub Actions, Git, Linux/SSH,
  Grafana, SonarQube, Vercel
  APIs/Services: SendGrid, Lark API, Cloudinary, OpenAI API, BytePlus AI
- Git identities that are all me (attribute work by email, not by name):
  - manuelmiguel0726@gmail.com
  - 148304460+NoxLuminosity@users.noreply.github.com
  - gmanuel@Miguels-MacBook-Pro.local
  Commits from any other author are someone else's work.

## Hard rules
- Only write inside this repo. All other projects under
  /Users/gmanuel/projects (LCMS, MAILX, Texxen Dubai, etc.) are READ-ONLY.
  Never edit, install, build, run, or migrate anything in them. Don't alter
  their branches, commits, config, or databases.
- Never open .env files, key files, secrets, or database dumps.
- Use other repos' git history only for stats and for commits authored by my
  three emails. Never put other people's names or emails, commit messages,
  client names, internal URLs, customer data, or proprietary code on the site
  or in docs.
- Never print any of my git emails on the site except
  manuelmiguel0726@gmail.com.
- Never invent metrics, features, clients, outcomes, testimonials, or dates.
  Anything unverified goes in docs/needs-confirmation.md, not on the site.
- Do not show total commit counts as a headline number on the site.
- Texxen Dubai: work out what it is from its source. Treat it as possibly
  client work; don't name the client or business on the site without my
  approval.
- Do not claim lint/typecheck/build/tests passed unless you actually ran them.
- Stop at the end of each stage and wait for my approval. Commit after each
  stage with a clear message.

## Stack and design
- Next.js App Router, TypeScript, Tailwind, Lucide, Motion (only if needed).
  If the existing portfolio uses a different suitable stack, tell me and
  recommend keep vs rebuild before changing anything.
- Dark only, no theme toggle. Background #0A0A0B, text #EDEDED, muted
  #8A8F98, single accent #5B8CFF. Geist for text, Geist Mono for tags and
  metadata. Reference feel: linear.app, vercel.com.
- One signature interaction: an animated architecture diagram on case-study
  pages. Everything else stays restrained.
- Avoid generic templates, neon, heavy gradients, 3D, skill progress bars,
  fake testimonials, and placeholder text disguised as finished content.
- Accessibility: semantic HTML, visible focus, keyboard nav, reduced-motion,
  SEO metadata, Open Graph, sitemap, robots.
- All content lives in typed data files (profile, skills, projects, case
  studies, experience, links). Adding a project = adding a data entry. No
  hardcoded per-project pages; use a reusable case-study template.
- Contact is links only. No forms, no fake success messages.
- Screenshots: you can't run my other projects, so use architecture diagrams
  and clearly labeled illustrations. If /assets-incoming exists, use the
  sanitized screenshots in it and label them as real.
