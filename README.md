# 早稲田政経 合格ロードマップ（PWA）

## GitHub Pages で公開する手順（Todoクエストと同じ）
1. GitHub に新しいリポジトリを作る（例: `seikei-road`）
2. この4ファイル＋アイコン2枚を全部リポジトリ直下にアップ
   - index.html / manifest.json / sw.js / icon-192.png / icon-512.png
3. Settings → Pages → Branch を `main` / `(root)` にして Save
4. 発行された URL（https://ユーザー名.github.io/seikei-road/）を開く

## ホーム画面に追加（アプリ化）
- iPhone: Safari で開く → 共有ボタン → 「ホーム画面に追加」
- Android: Chrome で開く → メニュー → 「アプリをインストール」

## 機能
- 今日の日付から現在フェーズ／今週の目標を自動ハイライト
- 共テまでのカウントダウン
- 到達チェックは端末に自動保存（localStorage）
- 一度開けばオフラインでも動く（Service Worker）

## 更新するとき
index.html を書き換えて push するだけ。キャッシュを確実に更新したい時は
sw.js の `CACHE = 'seikei-road-v1'` の数字を v2, v3… と上げる。
