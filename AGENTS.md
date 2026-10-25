# AGENTS.md: Atlas

_Part of Tessera Atlas. Project context and rules live in the docs vault and are not copied here._

## Project context (read first)
@../../../Vaults/Tessera/Atlas/AGENTS.md
@../../../Vaults/Tessera/Atlas/project-concept.md
If those files are missing, tell the user and stop; do not guess project context.
For tools that do not expand `@` imports: read those two files before any other work.
Before building or changing a feature, read the spec that owns it (see the Doc Map in the vault AGENTS.md) and build from the spec.

## This codebase
- Purpose: Atlas, the first product of Tessera (what it is: the vault `project-concept.md`).
- Stack: owned by `../../../Vaults/Tessera/Atlas/tech-stack.md`; tools and checks by `../../../Vaults/Tessera/Atlas/tooling.md`. Read them before choosing a library or command.
- Layout: `server/` (a uv project, Python package `atlas` under `src/atlas/`) and `web/` (Vite, React, TypeScript), as described in the vault `tech-stack.md` section 3. The `schema/`, `domain/`, `storage/` and `api/` folders are created as the stack spike (T-028) builds them.
- Build, run and test commands (Windows PowerShell; scaffold only, the lint, format and `check` commands are not set up yet):
  - Server install: from `server/`, `uv sync`.
  - Server run: from `server/`, `uv run uvicorn atlas.main:app --reload` (serves on `http://127.0.0.1:8000`).
  - Server tests: from `server/`, `uv run pytest`.
  - Web install: from `web/`, `npm install`.
  - Web run: from `web/`, `npm run dev`. Production build: `npm run build`.
- Known issue: do not add `fastapi[standard]`. On Windows with Python 3.15 it pulls in `pyyaml`, which has to be built from source and fails without the C++ Build Tools. Use plain `fastapi` and `uvicorn`.
- Conventions: cite decisions, to-dos and feedback by ID (D-, T-, F-) in commit messages; never copy their content into this repo.

## Rules specific to this repo
(None yet. Everything else is owned by the vault AGENTS.md.)
