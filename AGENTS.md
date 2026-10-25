# AGENTS.md: Atlas

_Part of Tessera Atlas. Project context and rules live in the docs vault and are not copied here._

## Project context (read first)
@../../Vaults/Tessera/Atlas/AGENTS.md
@../../Vaults/Tessera/Atlas/project-concept.md
If those files are missing, tell the user and stop; do not guess project context.
For tools that do not expand `@` imports: read those two files before any other work.
Before building or changing a feature, read the spec that owns it (see the Doc Map in the vault AGENTS.md) and build from the spec.

## This codebase
- Purpose: Atlas, the first product of Tessera (what it is: the vault `project-concept.md`).
- Stack: owned by `../../Vaults/Tessera/Atlas/tech-stack.md`; tools and checks by `../../Vaults/Tessera/Atlas/tooling.md`. Read them before choosing a library or command.
- Layout: `server/` and `web/` as described in the vault `tech-stack.md` section 3. Not created yet.
- Build, run and test commands: not defined yet. They are created during the stack spike (T-028); record them here when they exist.
- Conventions: cite decisions, to-dos and feedback by ID (D-, T-, F-) in commit messages; never copy their content into this repo.

## Rules specific to this repo
(None yet. Everything else is owned by the vault AGENTS.md.)
