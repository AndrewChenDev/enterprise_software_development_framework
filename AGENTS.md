# Repository Guidelines

## Project Structure & Module Organization
This repository is currently documentation-first. The primary artifact is `SKILL.md` at the repo root, which defines the enterprise software development framework and role behaviors.

Keep the top level minimal:
- Core guides at root (`SKILL.md`, `AGENTS.md`)
- Longer references in `docs/` (create when needed)
- Automation or validation helpers in `scripts/` (create when needed)

Use descriptive file names and keep related content grouped by purpose rather than by date.

## Build, Test, and Development Commands
There is no compiled application or CI test suite yet. Use these commands for local quality checks:
- `rg --files` to inspect tracked files quickly
- `markdownlint SKILL.md AGENTS.md` to lint Markdown (if `markdownlint` is installed)
- `git diff -- SKILL.md AGENTS.md` to review documentation edits before commit

If you add tooling, document new commands here and prefer one-step commands over multi-step manual flows.

## Coding Style & Naming Conventions
For Markdown contributions:
- Use ATX headings (`#`, `##`, `###`) with clear section hierarchy
- Keep sections concise and action-oriented
- Prefer `-` for bullets and fenced code blocks for commands
- Wrap lines for readability (target ~100 chars max)

Naming:
- Keep canonical guide files uppercase when intended as root-level standards (`AGENTS.md`, `SKILL.md`)
- Use kebab-case for supplemental docs (example: `docs/release-process.md`)

## Testing Guidelines
No formal test framework is configured yet. Treat contribution validation as documentation QA:
- Run Markdown linting
- Verify headings, internal consistency, and command accuracy
- Confirm examples are copy/paste runnable

When scripts or code are introduced, add a `tests/` directory and document how to run the suite in this file.

## Commit & Pull Request Guidelines
This repository currently has no commit history, so use Conventional Commits going forward:
- `docs: refine quality gate section`
- `chore: add markdown lint config`

Pull requests should include:
- A concise summary of what changed
- The reason for the change
- Any follow-up work or open questions
- Linked issue/task when available

Keep PRs focused; separate structural rewrites from content tweaks.

## Security & Configuration Tips
Do not commit secrets, credentials, or internal URLs. Respect `.gitignore` (currently excludes `.idea/`) and avoid editor-specific artifacts in commits.
