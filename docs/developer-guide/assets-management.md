# アセットの管理

- 画像・音声などの静的ファイルはすべて `public/assets/` に置く
- ゲーム内では `assets/ファイル名` というパスでアクセスできる
- 各シーンの `preload()` メソッドの先頭で `this.load.setPath('assets')` を呼ぶ
- アセットの読み込みは必ず `preload()` 内で行う
