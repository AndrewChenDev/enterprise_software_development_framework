# Enterprise Software Development Framework

## Description
This repository defines a reusable framework for building enterprise software with
cross-functional squads. The core artifact is `SKILL.md`, which documents team
structure, SDLC stages, quality gates, and role-based AI operating modes.

## Available Skills
The current framework exposes three primary role modes from `SKILL.md`:
- **Architect mode**: system design, RFCs, and scalability planning
- **Product Owner mode**: user stories, backlog shaping, and sprint direction
- **Senior Backend Engineer mode**: implementation and performance-focused review

## Installation (`npx skill add`)
Install this framework as a skill source with the Skills CLI:

```bash
npx skills add AndrewChenDev/enterprise_software_development_framework
```

Example (explicit GitHub source):

```bash
npx skills add github:AndrewChenDev/enterprise_software_development_framework
```

## Usage
After installation, load the framework and invoke a role directly in your prompt:

- `Using the skill.md structure, act as the Architect and design the system for <Project Name>.`
- `Act as the Product Owner and write the User Stories for our next sprint.`
- `Act as a Senior Backend Engineer and review this code for performance bottlenecks.`

## Skill Structure
Current repository layout:

```text
.
├── SKILL.md    # framework definition and role prompts
├── AGENTS.md   # contributor guidelines
└── CLAUDE.md   # assistant-facing repository context
```

## License
This project is licensed under the MIT License. See `LICENSE` for details.
