# TypeScript Conventions

- Do not relax `tsconfig.json` settings (strict mode must remain on)
- Do not leave unused variables or parameters — `noUnusedLocals` and `noUnusedParameters` are enforced
- Target: ES2020 — do not use features beyond this unless the tsconfig target is updated
- All new source files belong under `src/`
