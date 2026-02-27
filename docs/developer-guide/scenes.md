# シーンの管理

| ルール | 詳細 |
|--------|------|
| 配置場所 | `src/game/scenes/` に配置する |
| 登録 | `src/game/main.ts` の `scene` 配列に追加する |
| クラス名・ファイル名 | 一致させる（例: `Game.ts` → `export class Game`） |
| シーンキー | `super('SceneName')` のキーはファイル名と一致させる |

## 新しいシーンを追加する手順

1. `src/game/scenes/Menu.ts` を作成する（シーン名をファイル名にする）
2. `src/game/main.ts` の `scene` 配列に追加する
