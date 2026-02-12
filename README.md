# AI Agent Skill Pack: Full Project Initialization

A curated set of **15 AI agent skills** designed to provide a comprehensive, one-shot project initialization and documentation workflow. Compatible with **any AI agent or coding assistant** — Manus, Cursor, Windsurf, Claude, Codex, and more. Just clone this repo into your project or global skills directory, and you're ready to go.

---

## Quick Start

| What You Want | Prompt | What Runs |
| --- | --- | --- |
| **Smart Initialization** | `"Initialize master orchestrator"` | `master-orchestrator` |
| **Dev setup only** | `"Initialize dev orchestrator"` | `dev-orchestrator` |
| **Docs only** | `"Initialize docs orchestrator"` | `docs-orchestrator` |

That's it. One prompt, and the orchestrator handles the rest.

---

## The Three Orchestrators

### `master-orchestrator` (The Smart One)

The top-level orchestrator that **intelligently detects** what your project needs and runs the appropriate sub-orchestrators. It's the only command you need.

**Trigger prompts:** `"Initialize master orchestrator"`, `"Initialize"`, `"Initialize project"`, `"Initialize everything"`, `"Full project setup"`

**What it does:**

1.  **Analyzes** the project: Is it a new or existing codebase? Do docs or guidelines already exist?
2.  **Decides** what to run: `dev-orchestrator`, `docs-orchestrator`, or both.
3.  **Executes** the plan.

### `dev-orchestrator`

Sets up a project's development environment by synthesizing the core principles from 8 specialized development skills into a single `DEVELOPMENT_GUIDELINES.md` file.

**Trigger prompts:** `"Initialize dev orchestrator"`, `"Initialize dev"`, `"Setup dev"`, `"Dev guidelines"`

### `docs-orchestrator`

Generates a complete, multi-layered documentation suite by running 4 specialized documentation skills in sequence.

**Trigger prompts:** `"Initialize docs orchestrator"`, `"Initialize docs"`, `"Generate docs"`, `"Full docs"`, `"Document this entire project"`

---

## Project Lifecycle Guide

### New Project (Greenfield)

```
Day 1: Project Created
  │
  ├─→ "Initialize dev orchestrator"
  │    Creates DEVELOPMENT_GUIDELINES.md
  │    (So you and your AI agents know the rules before writing any code)
  │
  ├─→ Start coding...
  │
  ├─→ UI is stable
  │    (Optional: "Initialize docs orchestrator" for early documentation)
  │
  ├─→ Major milestone / MVP done
  │    "Initialize docs orchestrator"
  │    (Captures the current state of the project)
  │
  ├─→ Project complete / Ready for handoff
  │    "Initialize master orchestrator"
  │    (Full refresh — dev guidelines + complete docs suite)
  │
  └─→ Done. Any AI agent can now take over.
```

### Existing Project (Brownfield / Forked Repo)

```
Day 1: Cloned or forked the repo
  │
  ├─→ "Initialize master orchestrator"
  │    (One shot — generates everything based on existing codebase)
  │
  └─→ Done. Full context captured. Ready to work or hand off.
```

### When to Use Each Orchestrator

| Project Phase | What's Happening | Which Orchestrator | Why |
|---|---|---|---|
| **Day 1 — New project** | Just created the project, no code yet | `dev orchestrator` | Set coding standards before anyone writes a single line. The `DEVELOPMENT_GUIDELINES.md` becomes the team's rulebook. |
| **Day 1 — Existing project** | Forked or cloned a repo you didn't build | `master orchestrator` | You need both dev guidelines AND full documentation to understand the codebase. One shot, gets everything. |
| **During development** | Actively coding, things are changing | None | Don't generate docs yet — they'll be outdated by tomorrow. Focus on building. |
| **UI is stable** | Frontend is mostly done, not changing much | `docs orchestrator` | Good time to capture the design system in `DESIGN.md` while it's fresh. |
| **MVP / Major milestone** | Feature-complete for this phase | `docs orchestrator` | Capture the current state before moving to the next phase. |
| **Before handoff** | Another dev or AI agent will take over | `master orchestrator` | Full refresh — ensures dev guidelines + all docs are up to date. |
| **Project complete** | Ready for deployment / delivery | `master orchestrator` | Final documentation pass. Everything is captured for posterity. |
| **Onboarding** | New team member or AI agent joining | `master orchestrator` | They get the full picture — how to build (dev) and what was built (docs). |

### The Golden Rule

> **Dev orchestrator** = Run ONCE at the start. It sets the rules.
>
> **Docs orchestrator** = Run at MILESTONES. It captures the state.
>
> **Master orchestrator** = Run for HANDOFFS. It does everything.

---

## All 15 Skills

### Orchestrators (3)

| Skill | Description |
| --- | --- |
| `master-orchestrator` | Intelligently runs dev and/or docs workflows based on project state |
| `dev-orchestrator` | Synthesizes 8 dev skills into `DEVELOPMENT_GUIDELINES.md` |
| `docs-orchestrator` | Runs 4 doc skills to generate full documentation suite |

### Development Skills (8)

| Skill | Category | Source | Description |
| --- | --- | --- | --- |
| `frontend-design` | Frontend | [anthropics/skills](https://skills.sh/) | Production-grade frontend interfaces |
| `ui-ux-pro-max` | UI/UX | [nextlevelbuilder/ui-ux-pro-max-skill](https://skills.sh/) | 50 styles, 21 palettes, 50 font pairings, 9 stacks |
| `web-design-guidelines` | UI/UX Review | [vercel-labs/agent-skills](https://skills.sh/) | Web Interface Guidelines compliance |
| `code-reviewer` | Code Quality | [anthropics/skills](https://skills.sh/) | Elite code review for quality, performance, reliability |
| `find-bugs` | Security/QA | [getsentry/skills](https://skills.sh/) | Bug and security vulnerability scanning |
| `clean-code` | Code Quality | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | Robert C. Martin's Clean Code principles |
| `api-security-best-practices` | Security | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | API security: auth, rate limiting, injection prevention |
| `e2e-testing-patterns` | Testing | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | Playwright/Cypress E2E testing patterns |

### Documentation Skills (4)

| Skill | Category | Source | Description |
| --- | --- | --- | --- |
| `context-driven-development` | Project Context | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | Project vision, tech stack, workflows, conventions |
| `design-md` | Design System | [anthropics/skills](https://skills.sh/) (modified) | Synthesizes a `DESIGN.md` from any web project |
| `c4-architecture-c4-architecture` | Architecture | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | C4 architecture documentation (code to system level) |
| `readme` | README | [anthropics/skills](https://skills.sh/) | Comprehensive README generation |

---

## Installation

### Global Install (available across all projects)

Clone this repo and copy the `skills/` folder to your AI agent's global skills directory:

| Platform | Global Skills Directory |
| --- | --- |
| Manus | `/home/ubuntu/skills/` |
| Cursor | `~/.cursor/skills/` or project root |
| Windsurf | Project root `./skills/` |
| Other AI agents | Wherever your agent reads skill definitions |

### Project-Level Install (committed to repo)

Clone this repo directly into your project root so any AI agent that opens the project can immediately access the skills:

```bash
git clone https://github.com/<your-username>/manus-ai-skill-pack.git ./skills
```

This way, the skills travel with the project — any AI agent that opens the repo will find them automatically.

---

## Credits

Skills in this pack are sourced from the [**Open Agent Skills Ecosystem**](https://skills.sh/) and community repositories:

| Source | Skills |
| --- | --- |
| [anthropics/skills](https://skills.sh/) | `frontend-design`, `code-reviewer`, `design-md`, `readme`, `skill-creator` |
| [vercel-labs/agent-skills](https://skills.sh/) | `web-design-guidelines` |
| [nextlevelbuilder/ui-ux-pro-max-skill](https://skills.sh/) | `ui-ux-pro-max` |
| [getsentry/skills](https://skills.sh/) | `find-bugs` |
| [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) | `clean-code`, `api-security-best-practices`, `e2e-testing-patterns`, `context-driven-development`, `c4-architecture-c4-architecture` |
| Custom | `master-orchestrator`, `dev-orchestrator`, `docs-orchestrator` |

Browse more skills at [skills.sh](https://skills.sh/).
