# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

- `npm run dev` — Start dev server at http://localhost:8080 (includes Phaser analytics logging)
- `npm run build` — Production build to `dist/` (includes analytics logging)

No test or lint commands are configured.

## Architecture

**Entry flow**: `index.html` → `src/main.ts` (DOM bootstrap) → `src/game/main.ts` (Phaser config) → `src/game/scenes/Game.ts`

**`src/game/main.ts`** — Creates the Phaser.Game instance with config: 1024×768, auto-renderer (WebGL/Canvas), FIT scale mode centered both axes, background `#028af8`. Registers all scenes here.

**`src/game/scenes/`** — Each scene extends Phaser's `Scene` class. Currently contains one scene (`Game.ts`). Add new scenes in this directory and register them in `src/game/main.ts`.

**`public/assets/`** — Static game assets (images, audio, etc.) served at `assets/` path. Preload them in scene's `preload()` method.

**Vite config**: `vite/config.dev.mjs` (dev) and `vite/config.prod.mjs` (prod). Phaser is split into its own chunk for both configs. Prod uses Terser for minification.

## Rules

Detailed rules are in `.claude/rules/index.md`. Key points:
- Update this file on any architecture or convention change
- Scenes go in `src/game/scenes/` and must be registered in `src/game/main.ts`
- Assets go in `public/assets/`; preload in each scene's `preload()` method
- Do not relax TypeScript strict settings
- Use gitmoji commit prefixes (`:sparkles:`, `:bug:`, `:memo:`, etc.)
