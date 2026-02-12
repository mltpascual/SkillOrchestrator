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

### Step 1: Read All 8 Dev Skills

Read the `SKILL.md` file for each of the following 8 skills:
- `frontend-design/SKILL.md`
- `ui-ux-pro-max/SKILL.md`
- `web-design-guidelines/SKILL.md`
- `code-reviewer/SKILL.md`
- `find-bugs/SKILL.md`
- `clean-code/SKILL.md`
- `api-security-best-practices/SKILL.md`
- `e2e-testing-patterns/SKILL.md`

> **Note:** These paths are relative to the skills directory. In Manus, the full path is `/home/ubuntu/skills/<skill-name>/SKILL.md`. In other environments, resolve relative to wherever the skills are installed.

### Step 2: Synthesize and Write `DEVELOPMENT_GUIDELINES.md`

Create the `DEVELOPMENT_GUIDELINES.md` file with the following structure. For each section, synthesize the core principles from the specified skills.

```markdown
# Development Guidelines

This document outlines the coding standards, UI/UX principles, security policies, and testing strategies for this project. All developers and AI agents must adhere to these guidelines.

## 1. UI/UX & Frontend

*Synthesize principles from `frontend-design`, `ui-ux-pro-max`, and `web-design-guidelines` here. Cover topics like:
- Visual identity and aesthetics
- Color palette and typography
- Component library and design system
- Layout, spacing, and responsiveness
- Accessibility standards (WCAG)
- Animation and interaction design*

## 2. Code Quality & Best Practices

*Synthesize principles from `clean-code` and `code-reviewer` here. Cover topics like:
- Naming conventions
- Function and class design
- Error handling and logging
- Code commenting and documentation
- Production reliability and performance*

## 3. Security

*Synthesize principles from `api-security-best-practices` and `find-bugs` here. Cover topics like:
- Authentication and authorization
- Input validation and output encoding
- Rate limiting and throttling
- Common vulnerability prevention (OWASP Top 10)
- Dependency scanning*

## 4. Testing

*Synthesize principles from `e2e-testing-patterns` here. Cover topics like:
- End-to-end testing strategy (Playwright/Cypress)
- Test suite structure and organization
- Selector strategies and locators
- Handling flaky tests
- CI/CD integration*
```

### Step 3: Verification

Verify that `DEVELOPMENT_GUIDELINES.md` was created successfully and contains all 4 sections. If the file is empty or incomplete, retry Step 2.

### Step 4: Notify User

Once verified, notify the user:

> "Development Setup Complete. The project's development best practices have been synthesized into `DEVELOPMENT_GUIDELINES.md`. All developers and AI agents should refer to this file throughout the development lifecycle."
