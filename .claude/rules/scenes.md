# Scene Management

- All scenes must be placed in `src/game/scenes/`
- All scenes must be registered in `src/game/main.ts` under the `scene` array in the Phaser config
- The scene key passed to `super('SceneName')` must match the filename (e.g., `Game.ts` → `super('Game')`)
- Each scene file exports a named class that extends `Phaser.Scene`

## Adding a New Scene

1. Create `src/game/scenes/Menu.ts` (use the scene name as the filename)
2. Add the class to the `scene` array in `src/game/main.ts`
3. Update the Architecture section of `CLAUDE.md`
