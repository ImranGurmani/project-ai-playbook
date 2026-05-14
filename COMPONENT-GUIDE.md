# COMPONENT-GUIDE

Generated: 2026-05-14

This file is a living UI/component map for future AI edits in `C:\xampp\htdocs\aiplaybookforprojects`.

## Main Pages

No main application pages are currently present.

Verified state:

- jCodemunch indexing was attempted and returned `No source files found`.
- The repository currently contains documentation files only.
- No page files, route files, templates, views, or app entry points were found.

Current files involved:

- `PROJECT-INDEX.md`
- `ARCHITECTURE-SUMMARY.md`
- `AI-RULES.md`
- `COMPONENT-GUIDE.md`

Manual review required when source code is added:

- Identify page routes and their owning feature areas.
- Document each page's purpose, data dependencies, layout sensitivity, and common edit risks.

## Layouts

No layout system is currently present.

Not found:

- App shell
- Header / navigation layout
- Sidebar
- Footer
- Dashboard layout
- Auth layout
- Admin layout
- Commerce layout
- Responsive grid or container primitives

Layout sensitivity: unclear because no UI layout code exists.

Common risks when editing later:

- Creating one-off page layouts before a shared layout pattern exists.
- Adding responsive behavior without documenting expected breakpoints.
- Introducing duplicated navigation or container logic across pages.

## Shared Components

No shared UI components are currently present.

Not found:

- Buttons
- Cards
- Inputs
- Modals
- Tabs
- Menus
- Toasts / alerts
- Icons
- Typography primitives
- Reusable content sections

Related components: none detected.

Data dependencies: none detected.

Manual review required when components are added:

- Record component file paths.
- Record intended reuse boundaries.
- Document styling and accessibility assumptions.
- Note whether components are purely presentational or contain state / side effects.

## Forms

No forms are currently present.

Not found:

- Login forms
- Registration forms
- Contact forms
- Checkout forms
- Admin edit forms
- Search or filter forms
- Validation schemas
- Form submission handlers

Data dependencies: unclear / not present.

Common risks when editing later:

- Adding form fields without validation rules.
- Mixing validation, API calls, and UI rendering in one place.
- Failing to document required and optional fields.
- Handling secrets, credentials, or payment data without explicit safeguards.

## Data Tables

No data table components are currently present.

Not found:

- Table components
- List views
- Pagination
- Sorting
- Filtering
- Bulk actions
- Empty states
- Loading states

Data dependencies: unclear / not present.

Common risks when editing later:

- Adding table UI without defining data ownership.
- Implementing sorting or filtering inconsistently across tables.
- Omitting empty, loading, and error states.
- Breaking narrow-screen behavior with wide columns or unwrapped content.

## Commerce Components (if present)

Commerce components are not present.

Not found:

- Product cards
- Product detail pages
- Cart
- Checkout
- Payment forms
- Order summary
- Pricing display
- Inventory or variant selectors

Data dependencies: unclear / not present.

Common risks when editing later:

- Treating price, tax, discount, shipping, or inventory logic as display-only.
- Duplicating cart state across components.
- Editing checkout or payment flows without tests and documentation.

## Auth Components (if present)

Auth components are not present.

Not found:

- Login UI
- Registration UI
- Forgot-password UI
- Session controls
- User menu
- Protected route wrappers
- Role or permission UI

Data dependencies: unclear / not present.

Common risks when editing later:

- Hiding UI elements without enforcing backend authorization.
- Mixing auth state with unrelated page state.
- Storing tokens or secrets in unsafe browser-accessible locations.
- Failing to document protected routes and role requirements.

## Admin Components (if present)

Admin components are not present.

Not found:

- Admin dashboard
- Admin navigation
- User management screens
- Settings screens
- Content management screens
- Audit or activity views

Data dependencies: unclear / not present.

Common risks when editing later:

- Reusing public components in admin flows without permission checks.
- Adding destructive admin actions without confirmation and error handling.
- Failing to document role-based visibility and backend enforcement.

## Sensitive UI Areas

No sensitive UI areas can be identified from current source because no UI source exists.

When UI is added, treat these areas as sensitive by default:

- Authentication and account flows
- Admin and permissioned workflows
- Payment, checkout, cart, and order flows
- Forms that collect personal data
- File upload flows
- Search, filtering, and bulk actions on user or business data
- Navigation that controls access to protected areas

Required documentation for sensitive UI:

- Purpose
- Files involved
- Related components
- Data dependencies
- Validation rules
- Authorization assumptions
- Layout constraints
- Common editing risks

## Undocumented / Needs Review

Needs review because no source files are currently present:

- App type
- Routing model
- UI framework
- Styling system
- Component hierarchy
- Shared layout model
- State management
- API integration pattern
- Form validation approach
- Accessibility conventions
- Responsive breakpoints
- Test coverage expectations

When implementation files are added, update this guide immediately with:

- Main pages grouped by feature area
- Layout files and page ownership
- Shared component paths
- Form and table patterns
- Data dependencies for each important component group
- High-risk UI areas and safe editing notes
