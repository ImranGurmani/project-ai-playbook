# PROMPT-PACK

Reusable prompt library for `project-ai-playbook` and other software repositories.

Use these prompts as a structured chain for project discovery, documentation, safe implementation, QA, and maintenance. Each prompt should be adapted with the current repository path, known constraints, and the exact task.

## Prompt Categories

### 1. Project Discovery

Prompts for understanding the repository before changing anything.

### 2. Documentation Generation

Prompts for creating living technical maps that future developers and AI assistants can reuse.

### 3. Safe Changes

Prompts for planning and implementing narrow, low-risk changes.

### 4. QA and Review

Prompts for checking correctness, layout safety, responsiveness, data safety, and regression risk.

### 5. Maintenance

Prompts for keeping documentation, rules, checklists, and project maps current as the codebase evolves.

## Prompt Names

| Phase | Prompt Name | Expected Output |
| --- | --- | --- |
| Project Discovery | Repository Structure Scan | Repository structure summary |
| Project Discovery | Stack and Dependency Detection | Stack summary |
| Project Discovery | Architecture Mapping | Architecture notes |
| Documentation Generation | Project Index Generator | `PROJECT-INDEX.md` |
| Documentation Generation | Architecture Summary Generator | `ARCHITECTURE-SUMMARY.md` |
| Documentation Generation | AI Rules Generator | `AI-RULES.md` |
| Documentation Generation | Component Guide Generator | `COMPONENT-GUIDE.md` |
| Documentation Generation | README Generator | `README.md` |
| Safe Changes | Change Request Builder | Filled change request |
| Safe Changes | Minimal Implementation Planner | Safe implementation plan |
| Safe Changes | UI-Safe Edit Prompt | UI change plan and edits |
| Safe Changes | Backend-Safe Edit Prompt | Backend/data change plan and edits |
| QA and Review | QA Checklist Generator | `QA-CHECKLIST.md` |
| QA and Review | Strict Self-Review Prompt | Review verdict |
| QA and Review | Regression Risk Review | Regression risk notes |
| Maintenance | Documentation Freshness Review | Docs update list |
| Maintenance | Prompt Pack Review | Prompt library updates |

## Purpose of Each Prompt

### Repository Structure Scan

- **Purpose:** Identify folders, files, app areas, and missing pieces before edits.
- **When to use:** At the start of work in any unfamiliar repository.
- **Required input:** Repository path, known project name, any existing agent rules.
- **Expected output:** Concise folder map, important files, unclear areas, and recommended next inspection targets.

### Stack and Dependency Detection

- **Purpose:** Detect languages, frameworks, package managers, build tools, runtime, and test tools.
- **When to use:** Before installation, build, testing, or architecture documentation.
- **Required input:** Dependency manifests, config files, lockfiles, source tree.
- **Expected output:** Verified stack summary with unknowns labeled `unclear`.

### Architecture Mapping

- **Purpose:** Explain app type, frontend/backend structure, routing, data flow, config flow, integrations, and risk areas.
- **When to use:** Before significant implementation or refactoring.
- **Required input:** Source structure, route files, entry points, config files, models, services, UI folders.
- **Expected output:** Architecture map suitable for developers and AI assistants.

### Project Index Generator

- **Purpose:** Create a complete technical map of the current repository.
- **When to use:** After initial scan or after major structure changes.
- **Required input:** Verified folder structure, stack, application areas, sensitive areas, unclear areas.
- **Expected output:** `PROJECT-INDEX.md`.

### Architecture Summary Generator

- **Purpose:** Create a concise architecture summary for fast onboarding.
- **When to use:** After architecture mapping or when source structure changes.
- **Required input:** App type, architecture pattern, frontend/backend structure, data flow, config flow, high-risk areas.
- **Expected output:** `ARCHITECTURE-SUMMARY.md`.

### AI Rules Generator

- **Purpose:** Define project-specific rules for Codex, Cursor, Claude, and similar assistants.
- **When to use:** Before asking AI tools to make changes.
- **Required input:** Project conventions, stack, folder structure, sensitive areas, known risks.
- **Expected output:** `AI-RULES.md`.

### Component Guide Generator

- **Purpose:** Map UI pages, layouts, shared components, forms, data tables, and sensitive UI areas.
- **When to use:** For UI-heavy projects or after adding frontend structure.
- **Required input:** Page files, layout files, component folders, style system, data dependencies.
- **Expected output:** `COMPONENT-GUIDE.md`.

### README Generator

- **Purpose:** Produce a practical GitHub-friendly project README.
- **When to use:** After the project purpose and workflow are clear.
- **Required input:** Project description, user audience, install steps, usage workflow, generated files, limitations, roadmap.
- **Expected output:** `README.md`.

### Change Request Builder

- **Purpose:** Convert vague requests into scoped implementation tasks.
- **When to use:** Before any code or documentation change.
- **Required input:** Feature name, current structure, problem, target behavior, involved files, constraints, forbidden mistakes, QA checks.
- **Expected output:** Filled change request based on `CHANGE-TEMPLATE.md`.

### Minimal Implementation Planner

- **Purpose:** Plan the smallest safe implementation that satisfies the request.
- **When to use:** After discovery and before editing.
- **Required input:** Filled change request, relevant files, constraints, existing patterns.
- **Expected output:** File-by-file implementation plan with risks and validation steps.

### UI-Safe Edit Prompt

- **Purpose:** Guide UI changes without breaking layout, responsiveness, spacing, or visual hierarchy.
- **When to use:** Before editing pages, layouts, components, forms, tables, or styles.
- **Required input:** Parent component, surrounding layout, width constraints, spacing rules, target change.
- **Expected output:** Inspected context, root cause, files to edit, safe plan, final changes, layout self-review.

### Backend-Safe Edit Prompt

- **Purpose:** Guide backend, API, validation, auth, permissions, and data changes.
- **When to use:** Before editing routes, controllers, services, models, schemas, migrations, jobs, or integrations.
- **Required input:** Current route/data flow, validation rules, auth requirements, persistence model, target behavior.
- **Expected output:** Safe backend plan, exact files, validation/error handling notes, regression checks.

### QA Checklist Generator

- **Purpose:** Create a reusable post-change checklist adapted to the repository type.
- **When to use:** During documentation setup or when project type changes.
- **Required input:** Project type, UI/backend/data presence, current QA tools, high-risk areas.
- **Expected output:** `QA-CHECKLIST.md`.

### Strict Self-Review Prompt

- **Purpose:** Audit proposed or completed changes like a strict senior engineer.
- **When to use:** Before finalizing any AI-generated change.
- **Required input:** Changed files, implementation summary, tests/checks run, known risks.
- **Expected output:** What looks correct, what looks risky, required fixes, final verdict.

### Regression Risk Review

- **Purpose:** Identify likely breakages from a change.
- **When to use:** For edits touching shared modules, auth, data, routing, layout, config, or dependencies.
- **Required input:** Changed files, dependent files, related tests, sensitive areas.
- **Expected output:** Regression risks, affected workflows, missing tests, recommended checks.

### Documentation Freshness Review

- **Purpose:** Keep docs synchronized with the actual repository.
- **When to use:** After adding files, changing stack, moving routes/components, or adding dependencies.
- **Required input:** Current file tree, changed files, existing docs.
- **Expected output:** Documentation files to update and exact stale statements.

### Prompt Pack Review

- **Purpose:** Improve the prompt library as project needs evolve.
- **When to use:** After repeated tasks reveal missing prompt coverage or weak instructions.
- **Required input:** Recent task types, failure modes, repeated review comments, new project conventions.
- **Expected output:** Updated prompt categories, names, input requirements, and expected outputs.

## Input Requirements

Every prompt should request only verified project facts and should label unknowns clearly.

Minimum reusable input block:

```text
Repository path:
Project name:
Current task:
Known stack:
Relevant files:
Files that must not change:
Constraints:
Forbidden mistakes:
Expected output:
Unknowns:
```

For UI work, also include:

```text
Parent layout/component:
Viewport requirements:
Spacing/layout constraints:
Responsive behavior:
Overflow risks:
Design system/components to reuse:
```

For backend/data work, also include:

```text
Route or entry point:
Validation rules:
Auth/permission requirements:
Data model or schema:
External services:
Error handling expectations:
Regression checks:
```

## Output Files

Recommended generated files:

- `PROJECT-INDEX.md`
- `ARCHITECTURE-SUMMARY.md`
- `AI-RULES.md`
- `COMPONENT-GUIDE.md`
- `CHANGE-TEMPLATE.md`
- `QA-CHECKLIST.md`
- `README.md`
- `PROMPT-PACK.md`

Optional future files:

- `API.md`
- `DATABASE.md`
- `ENVIRONMENT.md`
- `TESTING.md`
- `DEPLOYMENT.md`
- `SECURITY.md`
- `MAINTENANCE.md`

## Suggested Prompt Chain

Use this default chain for a new or unfamiliar repository:

1. Repository Structure Scan
2. Stack and Dependency Detection
3. Architecture Mapping
4. Project Index Generator
5. Architecture Summary Generator
6. AI Rules Generator
7. Component Guide Generator, if UI exists
8. QA Checklist Generator
9. README Generator

Use this default chain for a future code change:

1. Documentation Freshness Review
2. Change Request Builder
3. Minimal Implementation Planner
4. UI-Safe Edit Prompt or Backend-Safe Edit Prompt
5. Strict Self-Review Prompt
6. Regression Risk Review
7. Documentation Freshness Review

Use this default chain for ongoing maintenance:

1. Repository Structure Scan
2. Documentation Freshness Review
3. QA Checklist Generator, if project type changed
4. Prompt Pack Review
