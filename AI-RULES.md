# AI-RULES

These rules apply to AI coding assistants working in `C:\xampp\htdocs\aiplaybookforprojects`.

## Project Context

This repository is currently documentation-only.

Verified current state:

- jCodemunch cannot build a source index because it reports `No source files found`.
- The repository currently has project documentation, including `PROJECT-INDEX.md` and `ARCHITECTURE-SUMMARY.md`.
- No frontend app, backend app, API service, database schema, package manifest, build config, or test suite is currently detectable.

Do not infer a framework, runtime, app type, or architecture from the folder name. Treat all implementation details as unclear until actual source files and dependency manifests exist.

## Stack-Aware Rules

- Current detectable stack: Markdown documentation only.
- Do not claim the project uses PHP, Laravel, React, Vue, Node, Composer, npm, Vite, XAMPP conventions, MySQL, or any other stack unless corresponding files are present.
- If adding the first implementation files, add the matching dependency manifest and setup documentation in the same change.
- If adding a frontend, document the chosen framework, route structure, component structure, build command, and local run command.
- If adding a backend, document the server entry point, routing layer, validation layer, persistence layer, and local run command.
- If adding database behavior, include schema or migration files and update documentation with connection and migration instructions.

## Safe Edit Rules

- Preserve the accuracy of `PROJECT-INDEX.md` and `ARCHITECTURE-SUMMARY.md`; update them whenever the repository structure changes.
- Mark unknowns as `unclear` instead of guessing.
- Keep Markdown files readable, ASCII-safe, and free of null bytes or binary content.
- Do not replace existing documentation with broad boilerplate that hides the current empty / documentation-only state.
- Before editing a file, check whether the change affects the documented project state.
- Keep changes scoped to the requested file unless the user asks for repository-wide updates.
- Do not introduce generated lockfiles, dependencies, vendor folders, or build outputs without a clear implementation reason.

## UI / Layout Rules

No UI currently exists in this repository.

If UI code is added later:

- Define the UI framework and styling approach before adding components.
- Keep layout components separate from page-specific content.
- Reuse existing components once they exist; do not create duplicate button, card, form, modal, or layout primitives.
- Avoid hardcoded one-off spacing, colors, and typography if the project has or gains shared design tokens.
- Keep text from overflowing buttons, navigation, cards, and narrow mobile containers.
- Document where shared UI components live in `PROJECT-INDEX.md`.

## Responsive Rules

No responsive behavior currently exists because no UI code is present.

If responsive UI is added later:

- Build mobile and desktop behavior intentionally; do not assume desktop-only layouts.
- Use stable layout constraints for grids, toolbars, forms, dashboards, and repeated cards.
- Avoid fixed widths that break narrow screens.
- Ensure long labels, file names, prices, IDs, and user-generated text wrap or truncate predictably.
- Test key views at common mobile and desktop widths before finalizing UI work.

## Backend / Data Safety Rules

No backend or data layer currently exists.

If backend or data code is added later:

- Keep request routing, validation, business logic, and persistence concerns clearly separated.
- Validate all external input at the route or boundary layer.
- Do not store secrets directly in source files.
- Add `.env.example` when environment variables are introduced.
- Document required environment variables and local services.
- Use migrations or schema files for database changes; do not leave schema changes implicit.
- Treat auth, admin permissions, payment, checkout, file upload, and database writes as high-risk areas requiring focused review.

## Reuse Before Creating New Code

- Reuse existing documentation terms and facts from `PROJECT-INDEX.md` and `ARCHITECTURE-SUMMARY.md`.
- When source code is added, search for existing modules, components, helpers, and config patterns before creating new ones.
- Prefer extending established project patterns over introducing new libraries or architectural layers.
- Add new abstractions only when they remove real duplication or clarify a repeated responsibility.
- Keep project maps current so future assistants know what to reuse.

## Forbidden Mistakes

- Do not invent an app architecture that is not present.
- Do not describe frontend, backend, routing, database, APIs, auth, dashboard, cart, checkout, or admin areas as implemented unless source files prove it.
- Do not silently ignore unreadable or corrupt files.
- Do not add dependencies without documenting why they are needed and how to install them.
- Do not commit generated artifacts, caches, build output, or local environment files unless the project explicitly requires them.
- Do not make blind edits across unknown files or assume conventions from neighboring projects under `C:\xampp\htdocs`.
- Do not overwrite user-created documentation without preserving verified facts.

## Required Self-Check Before Finalizing

Before finalizing any change in this repository, confirm:

- The change reflects only verified repository facts.
- New unknowns are labeled as `unclear`.
- Markdown renders as readable text and contains no null-byte corruption.
- Any added source code includes matching setup or dependency documentation.
- Any added environment requirement is documented and represented in `.env.example` when appropriate.
- `PROJECT-INDEX.md` is updated if files, folders, stack, app areas, or sensitive areas changed.
- `ARCHITECTURE-SUMMARY.md` is updated if app type, architecture pattern, frontend/backend structure, data flow, or risk areas changed.
