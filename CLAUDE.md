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

Run `npm run lint` and `npm run build` before committing; both must pass.

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

## Low-friction execution

The owner uses Claude as an implementation agent and wants to minimise
unnecessary token use and tool calls.

For routine, reversible development tasks:

- Execute directly rather than researching the instruction first.
- Do not browse the web to verify packages, commands, or tools the owner
  explicitly asks you to use unless the command fails or there is a genuine
  security concern.
- Do not narrate routine intermediate steps.
- Keep progress updates extremely brief.
- Do not inspect unrelated repository state.
- Do not run elaborate smoke tests unless needed to establish that something
  works.
- Do not repeat checks that have already passed unless relevant files changed.
- Run lint/build only when application code, dependencies, configuration
  affecting the build, or deployment behaviour changed.
- Documentation-only changes do not require lint/build.
- Prefer the minimum number of tool calls necessary to complete the task.
- Do not add documentation or log decisions for trivial implementation details
  unless they materially affect future development.
- Ask the owner only about decisions affecting design, functionality, cost,
  security, patient data, production behaviour, or business requirements.

When the owner provides an explicit implementation instruction, treat it as
authorised and proceed unless it is unsafe or impossible.

@AGENTS.md
