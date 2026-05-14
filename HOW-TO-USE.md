# HOW-TO-USE

Use this file when you clone or download `project-ai-playbook` and want to apply it to another real software project.

## When To Use This

Use this prompt after you copy the playbook Markdown files into a target project or when you open a target project in Codex and want Codex to generate project-specific AI documentation.

Use it when:

- A project does not have clear AI rules yet.
- You want Codex to analyze the actual codebase before making changes.
- You want `PROJECT-INDEX.md`, `ARCHITECTURE-SUMMARY.md`, `AI-RULES.md`, `COMPONENT-GUIDE.md`, and `QA-CHECKLIST.md` to match the real project.
- You are onboarding Codex, Cursor, Claude, or another assistant to a new codebase.

Do not use this prompt inside `project-ai-playbook` itself unless you are maintaining the playbook docs.

## Basic Method

1. Clone or download this repository.
2. Copy the Markdown files into the root of the target project.
3. Open the target project in Codex.
4. Paste the prompt below into Codex.
5. Let Codex inspect the real project and update the documentation files.
6. Review the generated docs before asking Codex to implement features.

## Codex Prompt

Copy and paste this entire prompt into Codex while Codex is opened in the target project root:

```text
You are Codex working inside this repository.

Use the project-ai-playbook files in this repository as the required workflow standard:
- PROJECT-INDEX.md
- ARCHITECTURE-SUMMARY.md
- AI-RULES.md
- COMPONENT-GUIDE.md
- CHANGE-TEMPLATE.md
- QA-CHECKLIST.md
- PROMPT-PACK.md
- README.md

Goal:
Analyze this real project and regenerate the playbook documentation so future AI coding work is accurate, safe, and project-specific.

Important rules:
1. Do not guess the stack, architecture, routes, components, APIs, database, or business logic.
2. Inspect the actual repository structure and source files before writing conclusions.
3. If something is unclear, write `unclear`.
4. Preserve useful existing documentation, but replace generic placeholder content with verified project-specific facts.
5. Do not edit application code in this task. Only update documentation/playbook files.
6. Keep output practical for Codex, Cursor, Claude, and human developers.
7. Mark risky areas clearly.
8. If this project has UI, analyze layout, pages, shared components, forms, tables, responsiveness, and sensitive UI areas.
9. If this project has backend/data logic, analyze routes, controllers, services, validation, auth, permissions, models, database, config, and integrations.
10. After updating docs, run a self-review against QA-CHECKLIST.md.

Tasks:
1. Inspect the full folder structure.
2. Detect technology stack:
   - languages
   - frameworks
   - package managers
   - build tools
   - runtime
   - database
   - testing tools
   - deployment/config tools
3. Identify important application areas:
   - frontend pages/views
   - layouts
   - shared UI/components
   - forms
   - data tables
   - auth
   - dashboard
   - admin
   - product/commerce areas if present
   - cart/checkout if present
   - APIs/routes
   - backend services
   - database/models/migrations
   - config/environment files
   - tests
4. Update PROJECT-INDEX.md with:
   - Project Overview
   - Tech Stack
   - Folder Structure Summary
   - Main Application Areas
   - Shared Components / Reusable Modules
   - Sensitive Areas
   - Incomplete or Unclear Areas
   - Recommended Next Documentation Files
5. Update ARCHITECTURE-SUMMARY.md with:
   - App Type
   - Architecture Pattern
   - Frontend Structure
   - Backend Structure
   - Data Flow
   - Configuration and Environment
   - High-Risk Change Areas
   - Safe Editing Advice
6. Update AI-RULES.md with project-specific rules:
   - Project Context
   - Stack-Aware Rules
   - Safe Edit Rules
   - UI / Layout Rules
   - Responsive Rules
   - Backend / Data Safety Rules
   - Reuse Before Creating New Code
   - Forbidden Mistakes
   - Required Self-Check Before Finalizing
7. Update COMPONENT-GUIDE.md:
   - Main Pages
   - Layouts
   - Shared Components
   - Forms
   - Data Tables
   - Commerce Components if present
   - Auth Components if present
   - Admin Components if present
   - Sensitive UI Areas
   - Undocumented / Needs Review
8. Update QA-CHECKLIST.md so it matches this project type:
   - General Checks
   - UI Checks
   - Responsive Checks
   - Functional Checks
   - Data / Validation Checks
   - Regression Checks
   - Final Review Questions
9. Update README.md only if it still describes the playbook generically and needs a short note explaining how to use these docs inside this specific project.
10. Leave CHANGE-TEMPLATE.md and PROMPT-PACK.md unchanged unless they contain incorrect project-specific claims.

Required final response:
- What you inspected
- Files updated
- Key project facts discovered
- Unclear areas
- Recommended next steps
- Checks performed
```

If the target project has an `AGENTS.md` file, add this line at the top of the prompt:

```text
Also follow all AGENTS.md instructions that apply to this repository.
```

## After The Prompt Runs

Review the files Codex updated:

- `PROJECT-INDEX.md`
- `ARCHITECTURE-SUMMARY.md`
- `AI-RULES.md`
- `COMPONENT-GUIDE.md`
- `QA-CHECKLIST.md`
- `README.md`, if Codex changed it

If the docs look accurate, use `CHANGE-TEMPLATE.md` for the next feature request. Do not ask Codex to make code changes until the project docs are accurate.

## Repository Access Policy

This repository is intended as a read-only reference for most users.

Allowed for general users:

- Read the files on GitHub.
- Clone the repository.
- Download the repository.
- Copy the Markdown files into their own projects.

Maintainer-only actions:

- Push commits.
- Merge pull requests.
- Change prompt standards.
- Change AI rules.
- Change templates and checklist files.

Important: GitHub write restrictions are controlled from GitHub repository settings, not from Markdown files. To make this repository read-only for everyone except the owner/admin, configure GitHub permissions:

1. Open the GitHub repository.
2. Go to `Settings`.
3. Go to `Collaborators and teams` or `Manage access`.
4. Remove write access for non-admin users.
5. Go to `Branches`.
6. Add branch protection for `main`.
7. Require pull requests before merging, or restrict who can push to `main`.
8. Allow only the owner/admin account to push or merge.
