# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an **Enterprise Software Development Framework** — a methodology and AI-persona reference that defines how squads build enterprise software. The core document is `SKILL.md`, which establishes team structure, SDLC processes, quality gates, and technical principles.

There is no application source code yet. This repository serves as a framework template for projects that follow its methodology.

## Framework Architecture (SKILL.md)

The framework defines a complete development lifecycle:

- **Squad Model**: Self-contained teams of 6–10 (PO, EM, Architect, QA/SDET, 3-5 Backend, 2 Frontend, 1 DevOps/SRE)
- **QA Role**: First-class squad member — owns test plans, shift-left testing, QA sign-off on quality gate, and defect tracking
- **SDLC Stages**: Discovery/RFC → Sprint Execution → GitHub Workflow → Quality Gate → Deployment & Operations
- **GitHub Workflow**: Full branching strategy, PR lifecycle, PR templates, branch protection rules (see SKILL.md §2.5)
- **Quality Gate Pipeline**: Lint → Unit Tests → Integration Tests → Security/SAST → **QA Sign-off** → Peer Review → Merge
- **Git Worktree + PR Comments**: Agents use worktrees for parallel feature work and post decisions as GitHub PR/issue comments for traceability (see SKILL.md §4)
- **Agent Teams Mode (default)**: AI always operates as a full squad — launching parallel Task agents for Architect, QA, Dev, Security, and Code Review roles (see SKILL.md §6)
- **AI Persona Modes**: Team mode (default), Architect mode, PO mode, Dev mode, QA mode (see SKILL.md §"How to Initialize this AI")

## Key Principles

- DRY and SOLID are mandatory architectural patterns
- Observability: all features must include logging and monitoring hooks
- Security-first: zero-trust architecture, encryption at rest and in transit
- Shift-left quality: catch issues as early as possible in the pipeline

## Git Workflow

- All work happens on feature branches; `main` is protected
- Peer review + QA sign-off required before merge
- Follow conventional commit format: `<type>: <description>`
- Use git worktrees for parallel feature development
- Document decisions via GitHub PR/issue comments with role tags (`**[Architect]**:`, `**[QA]**:`, etc.)