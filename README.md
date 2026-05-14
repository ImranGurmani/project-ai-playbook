# project-ai-playbook

A centralized AI workflow playbook for web projects that defines coding rules, UI guardrails, responsive checks, change templates, and prompt standards so assistants like Codex, Cursor, and Claude make safer and more accurate edits.

## Project Description

project-ai-playbook is a documentation scaffold for safer AI-assisted software work. It gives coding assistants and developers a shared set of project maps, rules, templates, prompts, and QA checks before implementation begins.

The repository currently contains documentation only. There is no runnable application, package manifest, frontend, backend, database schema, or build system yet.

## Why This Exists

AI coding tools are most useful when they have accurate project context. Without that context, they can guess the stack, invent architecture, make broad edits, or miss layout and data risks.

This repository exists to make AI-assisted work more disciplined by requiring:

- A clear project index before changes.
- An architecture summary before implementation assumptions.
- AI editing rules tied to the actual repository state.
- A component guide for UI-safe edits.
- A change-request template that reduces vague tasks.
- A reusable prompt pack organized by development phase.
- A QA checklist for reviewing every change.

## Features

- Repository documentation map for current structure and known unknowns.
- Architecture summary template for developers and AI coding assistants.
- AI-specific rules for safe editing and avoiding blind assumptions.
- UI/component guide for future pages, layouts, forms, tables, and sensitive UI areas.
- Change-request template with required fields for scope, constraints, QA, and acceptance criteria.
- Prompt pack for discovery, documentation, safe changes, QA, and maintenance.
- Reusable QA checklist for documentation, UI, responsiveness, backend, data, and regression checks.
- Practical safeguards for projects that are not yet implemented.

## Installation

No installation is required for the current repository.

This is a Markdown documentation project. To use it:

1. Clone or copy the repository.
2. Open the files in any Markdown editor, IDE, or GitHub.
3. Use the templates before starting AI-assisted implementation work.

There are currently no package manager commands such as `npm install`, `composer install`, or `pip install`.

## Usage

Start with the documentation files in this order:

1. Read `PROJECT-INDEX.md` to understand the current repository state.
2. Read `ARCHITECTURE-SUMMARY.md` to understand what architecture is verified or unclear.
3. Read `AI-RULES.md` before asking an AI assistant to edit files.
4. Use `PROMPT-PACK.md` to choose the right prompt chain.
5. Use `CHANGE-TEMPLATE.md` to define a concrete change request.
6. If UI exists or is added, update `COMPONENT-GUIDE.md`.
7. After any change, run through `QA-CHECKLIST.md`.

For a future implementation task, copy the change template, fill it in, then give it to the coding assistant with the relevant files or feature request.

## How This Works In Any Project

Use this repository as a repeatable method, not as an application dependency.

There are two practical ways to use it:

1. **Copy the files into another project**
   - Copy the Markdown files from this repository into the target project root.
   - Ask the AI assistant to scan that actual project.
   - Regenerate `PROJECT-INDEX.md`, `ARCHITECTURE-SUMMARY.md`, `AI-RULES.md`, `COMPONENT-GUIDE.md`, and `QA-CHECKLIST.md` based on that project's real code.
   - Keep `CHANGE-TEMPLATE.md` and `PROMPT-PACK.md` as reusable workflow files.

2. **Use this repo as a reference playbook**
   - Keep this repository separate.
   - Open `PROMPT-PACK.md`.
   - Pick the prompt chain that matches the task.
   - Paste the prompt into Codex, Cursor, Claude, or another assistant while working inside the real target project.
   - Save the generated docs in the target project.

Recommended process for any project:

1. Start in the target project, not this playbook repository.
2. Run the discovery prompts first:
   - Repository Structure Scan
   - Stack and Dependency Detection
   - Architecture Mapping
3. Generate or update the project docs:
   - `PROJECT-INDEX.md`
   - `ARCHITECTURE-SUMMARY.md`
   - `AI-RULES.md`
   - `COMPONENT-GUIDE.md`, if UI exists
   - `QA-CHECKLIST.md`
4. Before every future change, fill out `CHANGE-TEMPLATE.md`.
5. Use the right implementation prompt:
   - UI-Safe Edit Prompt for pages, layouts, components, forms, styles, or responsiveness.
   - Backend-Safe Edit Prompt for routes, APIs, validation, auth, permissions, data, jobs, or integrations.
6. After the change, run:
   - Strict Self-Review Prompt
   - Regression Risk Review
   - QA checklist
7. Update the docs again if files, stack, routes, components, data flow, config, or risks changed.

The core rule is simple: first make the AI understand the current project, then ask it to change the project. Do not start with implementation prompts before discovery and documentation are current.

## Workflow

Use this workflow from project scan to AI-assisted editing:

1. **Scan the project**
   - Inspect the folder structure.
   - Identify source files, config files, routes, components, models, and tests.
   - Mark anything unclear instead of guessing.

2. **Update project maps**
   - Keep `PROJECT-INDEX.md` current.
   - Keep `ARCHITECTURE-SUMMARY.md` aligned with actual app structure.
   - Keep `COMPONENT-GUIDE.md` current when UI code exists.

3. **Prepare the change**
   - Choose the right prompt chain from `PROMPT-PACK.md`.
   - Fill out `CHANGE-TEMPLATE.md`.
   - Define exact target behavior, involved files, constraints, forbidden mistakes, and QA checks.

4. **Implement narrowly**
   - Reuse existing patterns before creating new code.
   - Avoid unrelated rewrites.
   - Document any new dependencies, environment variables, or setup steps.

5. **Review and QA**
   - Use `QA-CHECKLIST.md`.
   - Check documentation accuracy.
   - For UI changes, verify layout, responsiveness, overflow, spacing, and alignment.
   - For backend changes, verify validation, errors, auth, permissions, and regressions.

## Generated Files

This repository includes these generated documentation files:

- `PROJECT-INDEX.md` - Current repository map, stack detection, known areas, sensitive areas, and recommended docs.
- `ARCHITECTURE-SUMMARY.md` - Concise architecture summary for developers and AI coding assistants.
- `AI-RULES.md` - Project-specific rules for AI assistants such as Codex, Cursor, and Claude.
- `COMPONENT-GUIDE.md` - Living guide for pages, layouts, shared components, forms, tables, and sensitive UI areas.
- `CHANGE-TEMPLATE.md` - Copy-paste change request template for safe implementation planning.
- `PROMPT-PACK.md` - Reusable prompt library organized by development phase.
- `QA-CHECKLIST.md` - Reusable review checklist after every AI-assisted change.

## Best Practices

- Keep documentation tied to verified repository facts.
- Label unknowns as `unclear`.
- Update documentation in the same change that introduces source structure.
- Do not infer a stack from the folder name or hosting location.
- Do not add dependencies without documenting why they exist and how to install them.
- For UI work, inspect parent layout, spacing, overflow, and responsive behavior before editing.
- For backend or data work, document validation, permissions, environment variables, and data migrations.
- Keep generated documentation readable as plain Markdown.

## Limitations

- This repository does not currently contain runnable application code.
- There is no detected frontend, backend, API, database, package manager, or test suite.
- jCodemunch currently reports `No source files found`.
- The documentation describes safe workflow and verified repository state, not an implemented product.
- Architecture, component, and QA guidance should be revisited after real source files are added.

## Future Roadmap

- Add actual application source files when the product scope is defined.
- Add a package manifest and setup instructions if a runtime stack is introduced.
- Add `.env.example` when environment variables are required.
- Add tests and document the test workflow.
- Expand `PROJECT-INDEX.md` with real folders, routes, models, and config.
- Expand `COMPONENT-GUIDE.md` with real pages, layouts, reusable components, and UI risks.
- Keep `AI-RULES.md` and `PROMPT-PACK.md` updated as project conventions emerge.
