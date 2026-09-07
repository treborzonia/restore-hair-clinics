# Restore Hair Clinics — Private Redesign Concept

Private, unofficial redesign concept for Restore Hair Clinics by Dr Raghu Reddy
(Harley Street, London). This is a design exploration, not the live site, and it
is not affiliated with or endorsed by the clinic. Do not deploy it publicly or
present it as the official website.

## Project owner

The owner is not a developer. Handle technical implementation autonomously and
only surface decisions that genuinely need their input (scope, design
direction, content). Explain technical trade-offs in plain language.

## Stack

- Next.js (App Router) with TypeScript — source in `src/`, alias `@/*`
- Tailwind CSS v4 (configured via `src/app/globals.css` and `postcss.config.mjs`)
- ESLint (`eslint.config.mjs`)
- npm as the package manager — do not switch to yarn/pnpm/bun

## Commands

- `npm run dev` — local dev server
- `npm run build` — production build
- `npm run lint` — ESLint

Run `npm run lint` and `npm run build` before committing only when the change
touches application code, dependencies, build-affecting configuration, or
deployment behaviour; both must pass in those cases. Documentation-only
changes do not require lint/build.

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
