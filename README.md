# 田村明宏 — 職務経歴書サイト

転職用の1ページ完結型 Web 職務経歴書です。  
IT系営業職（ソリューション営業/プリセールス）への応募を想定しています。

## 起動方法

ビルド不要です。`index.html` をブラウザで直接開くだけで表示されます。

```bash
# 方法1: ファイルを直接開く
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux

# 方法2: ローカルサーバーで開く（任意）
python3 -m http.server 8000
# → http://localhost:8000 にアクセス
```

## 内容の編集方法

すべてのコンテンツは **`index.html`** 1ファイルに集約されています。  
HTMLのセクションごとにコメントで区切られているため、該当箇所を直接編集してください。

| セクション | 検索キーワード | 変更内容の例 |
|---|---|---|
| HERO（最上部） | `class="hero"` | 氏名・肩書き・キャッチコピー |
| Summary | `id="summary"` | 経歴要約・強み3つ |
| Skills | `id="skills"` | スキルタグの追加・削除 |
| Work Experience | `id="experience"` | 職歴の追加・期間の変更 |
| Case Study | `id="case-study"` | 提案事例の内容 |
| Education | `id="education"` | 学歴・研修歴 |
| Self PR | `id="selfpr"` | 自己PR文 |
| Contact | `id="contact"` | メールアドレス・各種リンク |

### よく変更する箇所

- **メールアドレス**: `id="emailText"` の中身を変更
- **GitHub / LinkedIn リンク**: `href="https://github.com/"` 等のURLを差し替え
- **デモリンク（提案事例）**: Case Study セクション下部の `case-links` 内のURLを差し替え
- **最終更新日**: `class="contact-updated"` の日付を変更

## 機能

- レスポンシブデザイン（スマホ・タブレット対応）
- 印刷対応（Ctrl+P / Cmd+P で職務経歴書として印刷可能）
- スムーズスクロールナビゲーション
- メールアドレスのコピーボタン
- 短期離職歴の折りたたみ表示（details/summary）
- モバイル用ハンバーガーメニュー

## 技術構成

- HTML / CSS / JavaScript（素のバニラ実装、フレームワーク不使用）
- 外部依存なし（CDN・npm パッケージ不要）
- 1ファイル完結（`index.html` のみ）
