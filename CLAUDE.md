# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is an **Enterprise Software Development Framework** — a methodology and AI-persona reference that defines how squads build enterprise software. The core document is `SKILL.md`, which establishes team structure, SDLC processes, quality gates, and technical principles.

There is no application source code yet. This repository serves as a framework template for projects that follow its methodology.

## Framework Architecture (SKILL.md)

The framework defines a complete development lifecycle:

- **Squad Model**: Self-contained teams of 6–10 (PO, EM, Architect, 3-5 Backend, 2 Frontend, 1 SDET, 1 DevOps)
- **SDLC Stages**: Discovery/RFC → Sprint Execution → Quality Gate → Deployment & Operations
- **Quality Gate Pipeline**: Lint → Unit Tests → Integration Tests → Security/SAST → Peer Review → Merge
- **Git Flow**: Feature branches only — no direct pushes to `main`
- **AI Persona Modes**: Architect mode, PO mode, Dev mode (see SKILL.md §"How to Initialize this AI")

## Key Principles

- DRY and SOLID are mandatory architectural patterns
- Observability: all features must include logging and monitoring hooks
- Security-first: zero-trust architecture, encryption at rest and in transit
- Shift-left quality: catch issues as early as possible in the pipeline

## Git Workflow

- All work happens on feature branches; `main` is protected
- Peer review is required before merge
- Follow conventional commit format: `<type>: <description>`