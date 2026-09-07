# Decision Log

A running record of meaningful design and technical decisions, newest first.
Each entry: date, decision, reasoning, alternatives considered.

## 2026-09-07 — Initial project setup

- **Decision:** Next.js (App Router) + TypeScript + Tailwind CSS + ESLint,
  npm as package manager, `src/` directory layout.
- **Reasoning:** Modern, well-supported stack suited to a static design
  concept that can later grow into a full site if needed.
- **Also decided:** Site metadata marked `noindex` because this is a private,
  unofficial concept. No database, CMS, booking, or auth at this stage.
