# Documentation Rules

## File Placement

| Document type | Location |
|---------------|----------|
| Rules for Claude (AI) | `.claude/rules/` |
| Rules for humans (Japanese) | `docs/developer-guide/` |

Both locations must be kept in sync. When a rule is added or changed, update the corresponding file in both directories.

## Sync Policy

- Every rule file in `.claude/rules/` must have a corresponding Japanese counterpart in `docs/developer-guide/`
- When splitting a rule into its own file, add a cross-reference in the parent file (e.g., `See .claude/rules/commit-message.md`)
- Human-facing docs link with relative markdown: `[commit-message.md](./commit-message.md)`

## Scope Differences

The human-facing docs (`docs/developer-guide/`) are for developers working on the codebase. Do NOT include the following in human-facing docs:

- Rules about maintaining `CLAUDE.md` — that is an instruction for Claude, not for humans
- Any other content that exists solely to instruct the AI

## Language

- `.claude/rules/` — English only
- `docs/developer-guide/` — Japanese only

## Style

- Keep documents concise and factual — not tutorial-style
- Use tables for structured rules (e.g., mapping filenames to purposes)
- Use numbered lists for ordered procedures
- Use bullet lists for unordered rules

## Others (for AI)
- Update `CLAUDE.md` whenever any of the following changes occur:
  - A new scene is added or removed from `src/game/scenes/`
  - A new npm script is added to `package.json`
  - The architecture or entry flow changes
  - New conventions are established
- Keep CLAUDE.md concise and factual — it is a reference, not a tutorial.
