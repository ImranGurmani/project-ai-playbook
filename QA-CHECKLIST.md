# QA-CHECKLIST

Use this checklist after every AI-assisted change in `C:\xampp\htdocs\aiplaybookforprojects`.

Current project state: documentation-only. jCodemunch reports `No source files found`, so UI and backend checks apply only when implementation files are added.

## General Checks

- [ ] The change matches the requested scope.
- [ ] No unrelated files were changed.
- [ ] Unknowns are marked as `unclear` instead of guessed.
- [ ] Markdown files render as readable text.
- [ ] Files contain no null bytes or accidental binary content.
- [ ] File names and links referenced in documentation are accurate.
- [ ] `PROJECT-INDEX.md` is updated if files, folders, stack, app areas, or sensitive areas changed.
- [ ] `ARCHITECTURE-SUMMARY.md` is updated if app type, structure, data flow, config, or risk areas changed.
- [ ] `COMPONENT-GUIDE.md` is updated if UI pages, layouts, components, forms, tables, or sensitive UI areas changed.
- [ ] `AI-RULES.md` still reflects current project conventions.
- [ ] Any new implementation files include matching setup or dependency documentation.

## UI Checks

Use this section when UI code exists or was changed.

- [ ] All changed pages/components render without visible errors.
- [ ] Text does not overflow buttons, cards, navigation, form fields, modals, or tables.
- [ ] Spacing and alignment are consistent with nearby UI.
- [ ] Layouts do not shift unexpectedly when content changes.
- [ ] Empty, loading, success, and error states are handled where relevant.
- [ ] Interactive controls have clear hover, focus, disabled, and active states where relevant.
- [ ] Reusable UI primitives are reused instead of duplicating one-off components.
- [ ] No public UI control implies access that backend permissions do not enforce.
- [ ] Sensitive UI flows such as auth, admin, checkout, payment, and file upload receive focused review.

## Responsive Checks

Use this section when UI code exists or was changed.

- [ ] Key screens work at mobile, tablet, and desktop widths.
- [ ] Navigation remains usable on narrow screens.
- [ ] Tables, grids, and repeated cards do not create uncontrolled horizontal overflow.
- [ ] Long labels, names, IDs, prices, URLs, and user-generated text wrap or truncate predictably.
- [ ] Forms remain usable on small screens.
- [ ] Fixed-width elements have responsive constraints.
- [ ] Modals, menus, and overlays fit within the viewport.
- [ ] Touch targets are large enough for mobile use.
- [ ] Important content is not hidden behind sticky headers, footers, or sidebars.

## Functional Checks

Use this section when executable application code exists or was changed.

- [ ] The changed behavior works in the primary expected path.
- [ ] Failure paths are handled clearly.
- [ ] Error messages are useful and do not expose secrets or internal details.
- [ ] Existing related behavior still works.
- [ ] Route, controller, handler, or component ownership remains clear.
- [ ] New behavior is documented in the relevant project map.
- [ ] Any new command, script, route, or endpoint has a clear purpose.
- [ ] If checks cannot be run locally, the reason is documented.

## Data / Validation Checks

Use this section when backend, API, form, database, or persistence logic exists or was changed.

- [ ] External input is validated at the boundary.
- [ ] Required fields, optional fields, and defaults are handled intentionally.
- [ ] Invalid data receives predictable errors.
- [ ] Authenticated and unauthenticated cases are checked where relevant.
- [ ] Role and permission behavior is checked where relevant.
- [ ] Database writes are intentional and documented.
- [ ] Schema or migration changes are included when data shape changes.
- [ ] Secrets are not hardcoded.
- [ ] New environment variables are added to `.env.example` and documentation.
- [ ] Payment, checkout, admin, auth, and file upload flows receive focused review when present.

## Regression Checks

- [ ] Existing documentation still matches the repository.
- [ ] Existing links and file references still resolve.
- [ ] No existing documented facts were removed without replacement.
- [ ] No generated artifacts, caches, build outputs, or local environment files were added accidentally.
- [ ] No unrelated formatting churn was introduced.
- [ ] If application code exists, relevant tests, build, lint, or manual checks were run.
- [ ] If no automated checks exist, manual verification steps are recorded.
- [ ] High-risk areas touched by the change are listed in the final review.

## Final Review Questions

- [ ] What exact files changed?
- [ ] Does the change reflect verified repository facts?
- [ ] Did any source structure, stack, app area, component, or config change?
- [ ] Were the relevant documentation files updated?
- [ ] Are there any remaining unknowns that should be labeled `unclear`?
- [ ] Could the change break future AI assistants by making the docs inaccurate?
- [ ] If UI was changed, was responsive behavior checked?
- [ ] If backend or data logic was changed, were validation, errors, auth, permissions, and regression risks checked?
- [ ] If tests or checks were not run, is the reason documented?
- [ ] Is the final response concise and clear about what was changed and what was not verified?
