# Decision Log

A running record of meaningful design and technical decisions, newest first.
Each entry: date, decision, reasoning, alternatives considered.

## 2026-09-07 — Playwright MCP server (project-scoped)

- **Decision:** Add the official Microsoft Playwright MCP server
  (`@playwright/mcp`) as a project-scoped MCP configuration in `.mcp.json`,
  so Claude Code sessions (including cloud sessions) can drive a browser to
  view and verify the site.
- **Reasoning:** The config runs the server via `npx @playwright/mcp@latest`
  in headless mode and points it at the Chromium binary pre-installed in
  Claude Code cloud environments (`/opt/pw-browsers/chromium`), because the
  package's bundled Playwright expects a newer browser build than the cloud
  image ships and cannot download one there. `--no-sandbox` is required since
  cloud sessions run as root. Verified working end-to-end in a cloud session
  (server start + page navigation).
- **Trade-off:** The executable path is specific to Claude Code cloud
  environments. On a machine without that path, remove the
  `--executable-path` arguments (and optionally `--no-sandbox`) from
  `.mcp.json` and Playwright will use its own downloaded browser.
- **Also:** `.playwright-mcp/` (session snapshots/traces the server writes
  into the project) added to `.gitignore`.

## 2026-09-07 — Initial project setup

- **Decision:** Next.js (App Router) + TypeScript + Tailwind CSS + ESLint,
  npm as package manager, `src/` directory layout.
- **Reasoning:** Modern, well-supported stack suited to a static design
  concept that can later grow into a full site if needed.
- **Also decided:** Site metadata marked `noindex` because this is a private,
  unofficial concept. No database, CMS, booking, or auth at this stage.
