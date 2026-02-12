---
name: dev-orchestrator
description: "Development environment orchestrator. Sets up coding standards, UI/UX guidelines, security policies, and testing strategies by synthesizing 8 specialized development skills into a single DEVELOPMENT_GUIDELINES.md file. Use when the user says: 'initialize dev orchestrator', 'initialize dev', 'setup dev', 'setup dev environment', 'dev guidelines', or 'create development guidelines'. Can also be called automatically by the master-orchestrator."
---

# Dev Orchestrator

Sets up a project's development environment by synthesizing the core principles from 8 specialized development skills into a single `DEVELOPMENT_GUIDELINES.md` file. This gives any developer or AI agent a single reference for how to build the app correctly.

## When to Use This Skill

- User says "initialize dev orchestrator"
- User says "initialize dev" or "setup dev" or "setup dev environment"
- User says "dev guidelines" or "create development guidelines"
- User wants to establish coding standards for a project

## Do Not Use This Skill When

- User wants full project setup (use `master-orchestrator` instead)
- User only wants documentation (use `docs-orchestrator` instead)

## Workflow

**Goal:** Create a `DEVELOPMENT_GUIDELINES.md` file in the project root.

1.  **Read the `SKILL.md` file for each of the following 8 skills:**
    - `frontend-design/SKILL.md`
    - `ui-ux-pro-max/SKILL.md`
    - `web-design-guidelines/SKILL.md`
    - `code-reviewer/SKILL.md`
    - `find-bugs/SKILL.md`
    - `clean-code/SKILL.md`
    - `api-security-best-practices/SKILL.md`
    - `e2e-testing-patterns/SKILL.md`

    > **Note:** These paths are relative to the skills directory. In Manus, the full path is `/home/ubuntu/skills/<skill-name>/SKILL.md`. In other environments, resolve relative to wherever the skills are installed.

2.  **Synthesize and write the `DEVELOPMENT_GUIDELINES.md` file.** The file should have a clear structure with sections for each category:
    - **UI/UX & Frontend:** Principles from `frontend-design`, `ui-ux-pro-max`, and `web-design-guidelines`.
    - **Code Quality & Best Practices:** Principles from `clean-code` and `code-reviewer`.
    - **Security:** Principles from `api-security-best-practices` and `find-bugs`.
    - **Testing:** Principles from `e2e-testing-patterns`.

3.  **Notify the user upon completion:**
    > "Development Setup Complete. The project's development best practices have been synthesized into `DEVELOPMENT_GUIDELINES.md`. All developers and AI agents should refer to this file throughout the development lifecycle."
