# AI Agent Skill Pack: Full Project Initialization

> **15 AI agent skills with 3 orchestrators for one-shot project initialization and documentation — compatible with any AI coding assistant.**

[![Claude Code](https://img.shields.io/badge/Claude%20Code-Anthropic-purple)](https://claude.ai)
[![Gemini CLI](https://img.shields.io/badge/Gemini%20CLI-Google-blue)](https://github.com/google-gemini/gemini-cli)
[![Codex CLI](https://img.shields.io/badge/Codex%20CLI-OpenAI-green)](https://github.com/openai/codex)
[![Cursor](https://img.shields.io/badge/Cursor-AI%20IDE-orange)](https://cursor.sh)
[![GitHub Copilot](https://img.shields.io/badge/GitHub%20Copilot-VSCode-lightblue)](https://github.com/features/copilot)
[![OpenCode](https://img.shields.io/badge/OpenCode-CLI-gray)](https://github.com/opencode-ai/opencode)
[![Antigravity](https://img.shields.io/badge/Antigravity-DeepMind-red)](https://github.com/sickn33/antigravity-awesome-skills)
[![AdaL CLI](https://img.shields.io/badge/AdaL%20CLI-SylphAI-pink)](https://sylph.ai/)
[![Windsurf](https://img.shields.io/badge/Windsurf-IDE-teal)](https://windsurf.com)
[![Manus](https://img.shields.io/badge/Manus-AI%20Agent-blueviolet)](https://manus.im)

## Table of Contents

- [How to Use](#how-to-use)
- [Installation](#installation)
- [Project Lifecycle Guide](#project-lifecycle-guide)
  - [New Project (Greenfield)](#new-project-greenfield)
  - [Existing Project (Brownfield / Forked Repo)](#existing-project-brownfield--forked-repo)
  - [When to Use Each Orchestrator](#when-to-use-each-orchestrator)
  - [The Golden Rule](#the-golden-rule)
- [The 15 Skills](#the-15-skills)
  - [Orchestrators (3)](#orchestrators-3)
  - [Development Skills (8)](#development-skills-8)
  - [Documentation Skills (4)](#documentation-skills-4)
- [Credits](#credits)

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

## Installation

Clone this repo into your project using the path that matches your tool:

```bash
# Universal (works with most tools)
git clone https://github.com/mltpascual/SkillOrchestrator.git .agent/skills

# Claude Code specific
git clone https://github.com/mltpascual/SkillOrchestrator.git .claude/skills

# Gemini CLI specific
git clone https://github.com/mltpascual/SkillOrchestrator.git .gemini/skills

# Codex CLI specific
git clone https://github.com/mltpascual/SkillOrchestrator.git .codex/skills

# Cursor specific
git clone https://github.com/mltpascual/SkillOrchestrator.git .cursor/skills

# Antigravity specific
git clone https://github.com/mltpascual/SkillOrchestrator.git .gemini/antigravity/skills

# OpenCode specific (Universal path)
git clone https://github.com/mltpascual/SkillOrchestrator.git .agent/skills
```

### Manus

Click the **"Add to my skills"** button for each of the 15 skills, then use the trigger prompts in any project.

After cloning, just use the trigger prompts — each skill has a `SKILL.md` file with full instructions.

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

### When to Use Each Orchestrator

| Project Phase | Which Orchestrator | Why |
|---|---|---|
| **Day 1 — New project** | `dev orchestrator` | Set coding standards before writing any code |
| **Day 1 — Existing project** | `master orchestrator` | Need both dev guidelines AND full documentation |
| **During development** | None | Focus on building — docs will be outdated tomorrow |
| **UI is stable** | `docs orchestrator` | Capture the design system while it's fresh |
| **MVP / Major milestone** | `docs orchestrator` | Capture the current state before the next phase |
| **Before handoff** | `master orchestrator` | Full refresh — dev guidelines + all docs up to date |
| **Project complete** | `master orchestrator` | Final documentation pass for posterity |

### The Golden Rule

> **Dev orchestrator** = Run ONCE at the start. It sets the rules.
>
> **Docs orchestrator** = Run at MILESTONES. It captures the state.
>
> **Master orchestrator** = Run for HANDOFFS. It does everything.

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

Skills in this pack are sourced from the [**Open Agent Skills Ecosystem**](https://skills.sh/) and community repositories. Compatible agent badges inspired by [antigravity-awesome-skills](https://github.com/sickn33/antigravity-awesome-skills). Browse more skills at [skills.sh](https://skills.sh/).
