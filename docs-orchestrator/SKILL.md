---
name: docs-orchestrator
description: "Documentation generation orchestrator. Generates a complete, multi-layered documentation suite by running 4 specialized documentation skills in sequence. Use when the user says: 'initialize docs orchestrator', 'initialize docs', 'generate docs', 'generate all docs', 'full docs', 'document this entire project', 'project handoff docs', or wants to create a comprehensive documentation package for AI agent handoff. Can also be called automatically by the master-orchestrator."
---

# Docs Orchestrator

Generates a complete, multi-layered documentation suite for a project by orchestrating 4 specialized documentation skills in the correct sequence.

## When to Use This Skill

- User says "initialize docs orchestrator"
- User says "initialize docs" or "generate docs" or "generate all docs"
- User says "document this entire project" or "full docs"
- User says "project handoff docs"
- User wants a complete documentation package for AI agent handoff

## Do Not Use This Skill When

- User wants full project setup (use `master-orchestrator` instead)
- User only wants dev guidelines (use `dev-orchestrator` instead)
- User only wants a single document (e.g., just a README)

## The 4-Layer Documentation Strategy

| Phase | Skill | Output | Purpose |
|---|---|---|---|
| 1 | `context-driven-development` | `conductor/` directory | Project vision, tech stack, workflows, conventions |
| 2 | `design-md` | `DESIGN.md` | Visual design system (colors, fonts, components) |
| 3 | `c4-architecture-c4-architecture` | `C4-Documentation/` directory | Deep architecture mapping (code to system level) |
| 4 | `readme` | `README.md` | Setup, usage, deployment manual |

## Path Resolution

> All skill paths in this document are relative to the skills directory. In Manus, the full path is `/home/ubuntu/skills/<skill-name>/SKILL.md`. In other environments, resolve relative to wherever the skills are installed.

## Workflow

Execute these phases sequentially. Do not skip any phase. Notify the user upon completion of each phase before starting the next.

### Phase 1: Project Context

**Skill:** Read `context-driven-development/SKILL.md` and follow its instructions.

Determine if the project is Brownfield (existing) or Greenfield (new). Generate the `conductor/` directory with all context files (`product.md`, `tech-stack.md`, `workflow.md`, etc.). Verify that `conductor/product.md` exists before proceeding.

**Notify:** "Docs Phase 1/4 complete — project context files generated in `conductor/`."

### Phase 2: Design System

**Skill:** Read `design-md/SKILL.md` and follow its instructions.

Analyze the codebase and generate `DESIGN.md`. If the project has no UI (e.g., a pure backend API or CLI tool), skip this phase and notify the user accordingly. Verify that `DESIGN.md` exists or was intentionally skipped.

**Notify:** "Docs Phase 2/4 complete — design system documented in `DESIGN.md`."

### Phase 3: Architecture Blueprint

**Skill:** Read `c4-architecture-c4-architecture/SKILL.md` and follow its instructions.

Perform a full C4 bottom-up analysis and generate the `C4-Documentation/` directory. Verify that `C4-Documentation/c4-context.md` exists before proceeding.

**Notify:** "Docs Phase 3/4 complete — C4 architecture documentation generated in `C4-Documentation/`."

### Phase 4: README

**Skill:** Read `readme/SKILL.md` and follow its instructions.

Generate a comprehensive `README.md` that links to all the documentation created in the previous steps: `conductor/product.md` for product context, `DESIGN.md` for design system, and `C4-Documentation/c4-context.md` for architecture overview. Verify that `README.md` exists and contains these links.

**Notify:** "Docs Phase 4/4 complete — `README.md` generated."

### Post-flight Summary

After all phases are complete, provide a summary of all artifacts created.
