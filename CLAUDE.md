# ライフリッジゲーム LP 公開プロジェクト（Claude Codeへの引き継ぎ）

## このフォルダの中身
- `index.html` … ライフリッジゲームのLP（体験会の申込ページ）。スクロールで文字や写真が現れる演出つき。
- `link/index.html` … Instagramのプロフィールに貼るリンク先ページ（スマホ用）。申込・LP・公式LINEのボタンをまとめたもの。
- `images/` … 両ページで使う写真とイラスト（体験会の写真5枚、結婚式カードのイラスト、家族のイラスト）。
- 外部から読み込むのは Google Fonts だけ。ビルド不要の静的サイト。

## やること（この順番で1つずつ）
1. GitHub アカウント `tshk10416-hub` に、公開リポジトリ `liferidge-lp` があるか確認する。
   - なければ作る（Public、README などは追加しない）。`gh` が使えるなら `gh repo create tshk10416-hub/liferidge-lp --public`。
2. このフォルダで `git init` → `main` ブランチで全ファイルをコミットして、`liferidge-lp` に push する。
3. GitHub Pages を有効にする（Settings → Pages → Source: Deploy from a branch → `main` / `(root)`）。
   - `gh` が使えるなら `gh api -X POST repos/tshk10416-hub/liferidge-lp/pages -f "source[branch]=main" -f "source[path]=/"`。
4. 公開URLが開けることを確認する。
   - LP: `https://tshk10416-hub.github.io/liferidge-lp/`
   - Instagram用リンク先ページ: `https://tshk10416-hub.github.io/liferidge-lp/link/`
5. 確認できたら、上の2つのURLをユーザーに伝える。

## 差し替えが必要な仮の値（ユーザーから値をもらったら一括置換する）
- 申込フォームURL: `https://forms.gle/your-form-url`（`index.html` と `link/index.html` の両方）
- `[曜日・時間を記入]` `[日付・時間を記入]` `[会場名・住所を記入]` `[会場名を記入]` `[参加費を記入]` `[所要時間を記入]` `[回答を記入]`
- 公式LINEは `https://line.me/R/ti/p/%40480gjare`（ゲームアプリと同じアカウント）。
- リンク先ページの「ゲームについて、くわしく見る」は `../`（同じサイト内のLP）につないである。

## 守ること
- ゲーム本体のリポジトリ `lifegame-v266` には触らない。
- デザインは確定済み。文言・色・レイアウトは、ユーザーに頼まれたとき以外変えない。
- 作業はユーザーが合意した手順どおり、1ステップずつ進める。
