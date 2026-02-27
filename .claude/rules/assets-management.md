# Asset Management

- All static assets (images, audio, spritesheets, etc.) go in `public/assets/`
- Assets are served at the path `assets/` at runtime
- Always call `this.load.setPath('assets')` at the start of `preload()` before loading assets
- Preload assets in the scene's `preload()` method, not elsewhere
