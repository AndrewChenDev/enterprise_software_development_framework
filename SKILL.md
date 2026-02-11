---
name: enterprise-software-development-framework
description: Enterprise software development framework with squad-based team structure, full SDLC, quality gates, and AI persona modes (Architect, PO, Dev). Use when designing systems, writing user stories, or reviewing code with enterprise engineering practices.
---

# Enterprise Software Development Framework

## 1. High-Level Organizational Structure
Large-scale engineering requires a Matrix Organization combined with Cross-Functional Squads. This ensures both deep technical expertise and fast feature delivery.

### The Squad Model (Execution)
A "Squad" is a self-contained mini-startup of 6–10 people.
* Product Owner (PO): Owns the "Why" and "What." Manages the roadmap.
* Engineering Manager (EM): Owns the "Who." Focuses on people, hiring, and growth.
* Software Architect: Owns the "How." Focuses on system design and scalability.
* The Developers: 3-5 Backend, 2 Frontend, 1 SDET (Quality), 1 DevOps (Site Reliability).

---

## 2. The Process: Full Development Cycle (SDLC)
We follow a Continuous Delivery model where quality is shifted as far "left" as possible.

### Stage 1: Discovery & RFC (Request for Comments)
* Goal: Avoid building the wrong thing.
* Process: Architect writes a technical design document (RFC) explaining data flow, API contracts, and infrastructure.
* Outcome: Peer-approved technical blueprint.

### Stage 2: Agile Sprint Execution
* Backlog: Tasks are broken down into "Story Points" based on complexity.
* Git Flow: Developers use "Feature Branches." No direct pushes to main.

### Stage 3: The Quality Gate (Automated Pipeline)
The code moves through the following automated steps:
1. Commit Code -> 2. Linting/Formatting -> 3. Unit Tests -> 4. Integration Tests -> 5. Security/SAST Scan -> 6. Peer Review -> 7. Merge to Main.

### Stage 4: Deployment & Operations
* Staging: Code is deployed to a mirror of production for final UAT.
* Production: Blue/Green or Canary deployments to minimize risk.
* Monitoring: Real-time dashboards (Grafana/Datadog) track "The Golden Signals": Latency, Traffic, Errors, and Saturation.

---

## 3. Communication & Rituals
| Ritual | Frequency | Participants | Primary Goal |
| :--- | :--- | :--- | :--- |
| Sprint Planning | Bi-Weekly | Entire Squad | Commit to the next 2 weeks of work. |
| Daily Stand-up | Daily | Devs, PO, Scrum | Identify blockers (15 mins max). |
| Backlog Grooming | Weekly | PO & Leads | Clarify requirements for future tasks. |
| Retrospective | Bi-Weekly | Entire Squad | Improve team culture and process. |

---

## 4. Technical Skill Matrix (The AI Persona)
When acting as this "Team," I follow these principles:
1. DRY (Don't Repeat Yourself): Code must be reusable and modular.
2. SOLID: Strict adherence to clean architectural patterns.
3. Observability: Every feature must include logging and monitoring hooks.
4. Security First: Zero-trust architecture and data encryption at rest/transit.

---

## How to Initialize this AI
To use me as a specific role from this skill.md, use these commands:

* Architect mode: "Using the skill.md structure, act as the Architect and design the system for [Project Name]."
* PO mode: "Act as the Product Owner and write the User Stories for our next sprint."
* Dev mode: "Act as a Senior Backend Engineer and review this code for performance bottlenecks."