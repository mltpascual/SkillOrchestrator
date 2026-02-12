# AI Agent Skill Pack: Full Project Initialization

<p align="center">
  <img src="https://img.shields.io/badge/AI_Agents-Ready-blueviolet?style=for-the-badge" alt="AI Agents Ready"/>
  <img src="https://img.shields.io/badge/Skills-15-informational?style=for-the-badge" alt="15 Skills"/>
  <img src="https://img.shields.io/badge/Orchestrators-3-success?style=for-the-badge" alt="3 Orchestrators"/>
</p>

A curated set of **15 AI agent skills** designed to provide a comprehensive, one-shot project initialization and documentation workflow. Compatible with **any AI agent or coding assistant** — just clone this repo into your project or global skills directory, and you're ready to go.

---

## How to Use

This pack is built around three orchestrator skills that automate development environment setup and full documentation generation — individually or together.

| What You Want | Prompt | What Runs |
| --- | --- | --- |
| **Smart Initialization** | `"Initialize master orchestrator"` | `master-orchestrator` |
| **Dev setup only** | `"Initialize dev orchestrator"` | `dev-orchestrator` |
| **Docs only** | `"Initialize docs orchestrator"` | `docs-orchestrator` |

That's it. One prompt, and the orchestrator handles the rest.

---

## Installation & Usage by Platform

### <img src="https://img.shields.io/badge/Manus-000?logo=manus&logoColor=fff" alt="Manus"/> Manus

1.  **Add Skills:** After this task, click the **"Add to my skills"** button for each of the 15 skills.
2.  **Usage:** In any project, just use the trigger prompts.

### <img src="https://img.shields.io/badge/Cursor-000?logo=cursor&logoColor=fff" alt="Cursor"/> Cursor

1.  **Install:** Clone this repo into your project root:
    ```bash
    git clone https://github.com/mltpascual/SkillOrchestrator.git ./.cursor/skills
    ```
2.  **Usage:** Use `@` to reference the skills in chat (e.g., `@master-orchestrator Initialize the project`).

### <img src="https://img.shields.io/badge/Windsurf-000?logo=windsurf&logoColor=fff" alt="Windsurf"/> Windsurf

1.  **Install:** Clone this repo into your project root:
    ```bash
    git clone https://github.com/mltpascual/SkillOrchestrator.git ./skills
    ```
2.  **Usage:** Reference the skills in your Windsurf prompts.

### <img src="https://img.shields.io/badge/Claude-000?logo=claude&logoColor=fff" alt="Claude"/> Claude / <img src="https://img.shields.io/badge/OpenAI-000?logo=openai&logoColor=fff" alt="OpenAI"/> OpenAI / Other Agents

1.  **Install:** Clone this repo into your project root:
    ```bash
    git clone https://github.com/mltpascual/SkillOrchestrator.git ./skills
    ```
2.  **Usage:** Provide the `skills/` directory as context to your agent and ask it to follow the instructions in the `SKILL.md` files.

---

## Project Lifecycle Guide

### New Project (Greenfield)

```
Day 1: Project Created
  │
  ├─→ "Initialize dev orchestrator"
  │    Creates DEVELOPMENT_GUIDELINES.md
  │
  ├─→ Start coding...
  │
  ├─→ Major milestone / MVP done
  │    "Initialize docs orchestrator"
  │
  └─→ Project complete / Ready for handoff
       "Initialize master orchestrator"
```

### Existing Project (Brownfield / Forked Repo)

```
Day 1: Cloned or forked the repo
  │
  ├─→ "Initialize master orchestrator"
  │    (One shot — generates everything based on existing codebase)
  │
  └─→ Done. Full context captured.
```

---

## The 15 Skills

### Orchestrators (3)

| Skill | Description |
| --- | --- |
| `master-orchestrator` | Intelligently runs dev and/or docs workflows based on project state |
| `dev-orchestrator` | Synthesizes 8 dev skills into `DEVELOPMENT_GUIDELINES.md` |
| `docs-orchestrator` | Runs 4 doc skills to generate full documentation suite |

### Development Skills (8)

| Skill | Category | Source |
| --- | --- | --- |
| `frontend-design` | Frontend | [anthropics/skills](https://skills.sh/) |
| `ui-ux-pro-max` | UI/UX | [nextlevelbuilder/ui-ux-pro-max-skill](https://skills.sh/) |
| `web-design-guidelines` | UI/UX Review | [vercel-labs/agent-skills](https://skills.sh/) |
| `code-reviewer` | Code Quality | [anthropics/skills](https://skills.sh/) |
| `find-bugs` | Security/QA | [getsentry/skills](https://skills.sh/) |
| `clean-code` | Code Quality | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) |
| `api-security-best-practices` | Security | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) |
| `e2e-testing-patterns` | Testing | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) |

### Documentation Skills (4)

| Skill | Category | Source |
| --- | --- | --- |
| `context-driven-development` | Project Context | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) |
| `design-md` | Design System | [anthropics/skills](https://skills.sh/) (modified) |
| `c4-architecture-c4-architecture` | Architecture | [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills) |
| `readme` | README | [anthropics/skills](https://skills.sh/) |

---

## Credits

Skills in this pack are sourced from the [**Open Agent Skills Ecosystem**](https://skills.sh/) and community repositories. Browse more skills at [skills.sh](https://skills.sh/).
