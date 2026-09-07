# Restore Hair Clinics — Private Redesign Concept

Private, unofficial redesign concept for Restore Hair Clinics by Dr Raghu Reddy
(Harley Street, London). This is a design exploration, not the live site, and it
is not affiliated with or endorsed by the clinic. Do not deploy it publicly or
present it as the official website.

## Project owner

The owner is not a developer. Handle technical implementation autonomously and
only surface decisions that genuinely need their input (scope, design
direction, content). Explain technical trade-offs in plain language.

## Working style

Operate in low-friction execution mode for routine setup tasks:

- On an explicit command or a request to install a known official
  package/plugin, execute directly — don't independently research or verify
  unless it fails, raises a security concern, or is ambiguous.
- Don't browse the web unless the task actually requires external research.
- Don't narrate intermediate steps; keep status updates to one short sentence.
- For routine repo changes: make the change, run only the minimum relevant
  check, and report the result.
- Ask the owner only when a decision materially affects design, cost, data,
  security, or production behaviour.

## Stack

- Next.js (App Router) with TypeScript — source in `src/`, alias `@/*`
- Tailwind CSS v4 (configured via `src/app/globals.css` and `postcss.config.mjs`)
- ESLint (`eslint.config.mjs`)
- npm as the package manager — do not switch to yarn/pnpm/bun

## Commands

- `npm run dev` — local dev server
- `npm run build` — production build
- `npm run lint` — ESLint

Run `npm run lint` and `npm run build` before committing code changes; both
must pass. Docs-only changes (markdown, `reference/`) don't need them.

## Repository layout

- `src/app/` — pages, layout, global styles
- `reference/` — project documentation (not shipped to the site):
  - `SOURCES.md` — links and citations for research material
  - `RESEARCH.md` — research notes about the clinic, competitors, market
  - `DECISIONS.md` — decision log; append an entry whenever a meaningful
    design or technical decision is made
- `public/demo-assets/` — images and media used by the demo site

## Constraints

- No database, CMS, booking system, or authentication unless the owner asks.
- Keep the site static/self-contained; avoid new runtime services.
- Medical/clinical claims in content must be traceable to a source recorded in
  `reference/SOURCES.md`.
- The site is marked `noindex` in metadata — keep it that way while private.

@AGENTS.md
