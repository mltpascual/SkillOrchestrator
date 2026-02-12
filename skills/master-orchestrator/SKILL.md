---
name: master-orchestrator
description: "Master orchestrator for full project setup. Automatically detects what the project needs and runs the appropriate sub-orchestrators. Use when the user says: 'initialize master orchestrator', 'initialize', 'initialize project', 'initialize everything', 'full project setup', or 'full setup'."
---

# Master Orchestrator

The master orchestrator that intelligently sets up your entire project. It automatically detects the project state and decides which sub-orchestrators to run — so you only need one command.

## When to Use This Skill

- User says "initialize master orchestrator"
- User says "initialize" or "initialize project" or "initialize everything"
- User says "full project setup" or "full setup"

## Path Resolution

> All skill paths in this document are relative to the skills directory. In Manus, the full path is `/home/ubuntu/skills/<skill-name>/SKILL.md`. In other environments, resolve relative to wherever the skills are installed.

## Smart Detection Workflow

When the user triggers this skill, follow this decision process:

### Step 1: Analyze the Project State

Inspect the project directory and determine:

| Check | How to Detect | Result |
|---|---|---|
| Is there existing source code? | Look for `src/`, `app/`, `lib/`, `package.json`, `requirements.txt`, `go.mod`, or similar | **Brownfield** (existing project) or **Greenfield** (new project) |
| Does `DEVELOPMENT_GUIDELINES.md` already exist? | Check project root | If yes, dev orchestrator may be skipped |
| Do documentation artifacts already exist? | Check for `conductor/`, `DESIGN.md`, `C4-Documentation/`, `README.md` | If yes, docs orchestrator will regenerate (update) them |

### Step 2: Decide What to Run

Based on the analysis:

| Project State | What to Run | Reasoning |
|---|---|---|
| **New project, no code yet** | `dev-orchestrator` only | No codebase to document yet. Set the rules first. |
| **New project, has initial code** | Both `dev-orchestrator` → `docs-orchestrator` | Code exists but no guidelines or docs. Full setup needed. |
| **Existing project, no guidelines or docs** | Both `dev-orchestrator` → `docs-orchestrator` | Foreign codebase needs both rules and documentation. |
| **Existing project, has `DEVELOPMENT_GUIDELINES.md` but no docs** | `docs-orchestrator` only | Dev rules exist, just need documentation. |
| **Existing project, has docs but no `DEVELOPMENT_GUIDELINES.md`** | `dev-orchestrator` only | Docs exist, just need dev rules. |
| **Existing project, has both** | Both (regenerate/update) | Refresh everything to capture latest state. |

### Step 3: Notify the User

Before running, inform the user of the plan:

> "I've analyzed the project. Here's what I'll do:"
> - [List which orchestrators will run and why]
>
> "Proceeding now."

### Step 4: Execute

#### If running Dev Orchestrator:

Read `dev-orchestrator/SKILL.md` and follow its instructions completely. This will synthesize 8 development skills into a `DEVELOPMENT_GUIDELINES.md` file.

**Notify:** "Dev setup complete — `DEVELOPMENT_GUIDELINES.md` created."

#### If running Docs Orchestrator:

Read `docs-orchestrator/SKILL.md` and follow its instructions completely. This will run 4 documentation skills in sequence to generate:
- `conductor/` directory (project context)
- `DESIGN.md` (design system)
- `C4-Documentation/` directory (architecture)
- `README.md` (project manual)

**Notify:** "Documentation generation complete."

### Step 5: Final Summary

After all steps are complete, provide a summary:

> "Project initialization complete. Here's what was created:"
>
> | Artifact | Location | Description |
> |---|---|---|
> | Dev Guidelines | `DEVELOPMENT_GUIDELINES.md` | Coding standards, UI/UX, security, testing |
> | Project Context | `conductor/` | Vision, tech stack, workflows, conventions |
> | Design System | `DESIGN.md` | Colors, typography, components, spacing |
> | Architecture | `C4-Documentation/` | C4 model from code to system context |
> | README | `README.md` | Setup, usage, and deployment guide |
>
> "Any AI agent taking over this project should start by reading these files."
