# 🎨 BeatStars アートワーク プロンプト生成ツール

[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deployed-success)](https://phonon-py.github.io/beatstars-artwork-generator/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)

**Microsoft Copilot企業版対応 - BeatStars向け動的プロンプト自動生成システム**

音楽プロデューサー向けの革新的なアートワーク生成ツール。楽曲情報を入力するだけで、Microsoft Copilotで使用できる最適化されたプロンプトを自動生成します。

## 🚀 デモ

**▶ [ライブデモを見る](https://phonon-py.github.io/beatstars-artwork-generator/)**

## 🎯 主要機能

- **🎵 ジャンル特化プロンプト**: 9つの音楽ジャンルに対応した専用テンプレート
- **⚡ BPM連動ビジュアル**: BPMに基づく動的エフェクト自動追加
- **🎨 インテリジェントキーワード抽出**: 楽曲タイトルから視覚要素を自動生成
- **📋 ワンクリックコピー**: 生成されたプロンプトを瞬時にクリップボードへ
- **🔄 複数バリエーション**: メイン + 3種類のスタイルバリエーション
- **📱 レスポンシブデザイン**: デスクトップ・モバイル完全対応

## 📸 スクリーンショット

![BeatStars Artwork Generator Main Interface](https://via.placeholder.com/800x600/667eea/ffffff?text=BeatStars+Artwork+Generator)

*メインインターフェース: 直感的な操作でプロ仕様のプロンプトを生成*

## 🛠️ 技術仕様

| 技術スタック | バージョン | 用途 |
|-------------|-----------|------|
| HTML5 | Latest | マークアップ・構造 |
| CSS3 | Latest | スタイリング・レスポンシブ |
| Vanilla JavaScript | ES6+ | ロジック・インタラクション |
| GitHub Pages | - | ホスティング・デプロイメント |

### システム要件
- モダンブラウザ (Chrome 80+, Firefox 75+, Safari 13+, Edge 80+)
- JavaScript有効
- インターネット接続 (初回読み込み時)

## 💡 使用方法

### ⚡ クイックスタート

1. **楽曲情報入力**
   ```
   楽曲タイトル: "Midnight Bass Trap Beat"
   ジャンル: RAGE/Dark Trap
   ムード: Dark
   BPM: 146 (オプション)
   ```

2. **プロンプト生成**
   - 「🎯 アートワーク プロンプト生成」ボタンクリック
   - 自動的に最適化されたプロンプトが4種類生成

3. **Microsoft Copilotで使用**
   - 📋アイコンをクリックしてプロンプトをコピー
   - Microsoft Copilot企業版にアクセス
   - プロンプトを貼り付けて送信

### 📋 詳細手順

1. **プロンプトコピー**: 生成されたプロンプトの📋アイコンをクリック
2. **Copilotアクセス**: Microsoft Copilot企業版を開く
3. **プロンプト送信**: コピーしたプロンプトを貼り付けて送信
4. **候補選択**: 生成された4つの候補から最適なものを選択
5. **微調整**: 必要に応じて「もっと暗く」「フォントを変えて」等の指示を追加

## 🎨 対応ジャンル一覧

| ジャンル | 特徴 | カラーパレット | 美学スタイル |
|---------|-----|-------------|------------|
| **RAGE/Dark Trap** | アンダーグラウンド・パンク | Black/White/Red | Underground Opium Gang |
| **Melodic Hip-Hop** | エレガント・洗練 | Purple/Gold Gradients | Luxury Minimalist |
| **R&B/Soul** | ソウルフル・上品 | Rich Purple/Gold | Soulful Elegant |
| **Electronic/EDM** | サイバーパンク・未来的 | Electric Blue/Cyan | Cyberpunk |
| **Lo-Fi/Chill** | ヴィンテージ・リラックス | Pastel Earth Tones | Vintage Analog |
| **Drill/UK Drill** | ストリート・攻撃的 | Monochrome/Blue | Gritty Street |
| **Trap** | モダン・アーバン | Purple/Black | Modern Street |
| **House** | クラブ・アップリフト | Vibrant Gradients | Modern Club |
| **Ambient** | ミニマル・幻想的 | Ethereal Gradients | Atmospheric Minimal |

## 🔧 カスタマイズ方法

### 新しいジャンルテンプレート追加

```javascript
// index.html の genreTemplates オブジェクトに追加
'new-genre': {
    template: '"[TRACK_TITLE]" custom genre album cover, [VISUAL_ELEMENTS], custom typography, color scheme, aesthetic style, [MOOD] energy, layout, 1024x1024 square format',
    colors: 'custom color palette',
    aesthetic: 'custom aesthetic',
    typography: 'custom typography'
}
```

### 視覚要素マッピング追加

```javascript
// visualElementsMap オブジェクトに新しいキーワードを追加
'custom-keyword': 'corresponding visual elements description'
```

### BPM範囲カスタマイズ

```javascript
// getBPMCategory 関数でBPM範囲を調整
function getBPMCategory(bpm) {
    if (bpm < 80) return 'slow';      // カスタム閾値
    if (bpm < 130) return 'medium';   // カスタム閾値
    return 'fast';
}
```

## 🚀 ローカル開発

```bash
# リポジトリクローン
git clone https://github.com/phonon-py/beatstars-artwork-generator.git

# ディレクトリ移動
cd beatstars-artwork-generator

# 開発サーバー起動 (Python)
python -m http.server 8000

# または Node.js
npx serve .

# ブラウザでアクセス
open http://localhost:8000
```

## 📝 ライセンス

このプロジェクトは[MIT License](LICENSE)の下で公開されています。

```
MIT License

Copyright (c) 2024 BeatStars Artwork Generator

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.
```

## 🤝 コントリビューション

コントリビューションを歓迎します！以下の方法で参加できます：

### 🐛 バグレポート
1. [Issues](https://github.com/phonon-py/beatstars-artwork-generator/issues)から新しいIssueを作成
2. バグレポートテンプレートに従って詳細を記入
3. 再現手順・環境情報を含める

### ✨ 機能提案
1. [Issues](https://github.com/phonon-py/beatstars-artwork-generator/issues)で機能リクエストを作成
2. 実装したい機能の詳細説明
3. 使用ケース・メリットを明記

### 🔧 コード貢献
1. このリポジトリをフォーク
2. 機能ブランチを作成 (`git checkout -b feature/new-feature`)
3. 変更をコミット (`git commit -m 'Add new feature'`)
4. ブランチにプッシュ (`git push origin feature/new-feature`)
5. Pull Requestを作成

### 📋 コーディング規約
- インデント: 4スペース
- セミコロン必須
- camelCase命名規則
- コメントは日本語または英語
- 関数・変数名は説明的に

## 📞 サポート・フィードバック

### 🆘 サポート
- **Issues**: [GitHub Issues](https://github.com/phonon-py/beatstars-artwork-generator/issues)
- **ディスカッション**: [GitHub Discussions](https://github.com/phonon-py/beatstars-artwork-generator/discussions)
- **Email**: フィードバック・質問は[こちら](mailto:support@example.com)

### 💬 フィードバック
このツールが音楽制作ワークフローにどのように役立っているか、ぜひお聞かせください：

- ⭐ GitHub でのスター
- 🐦 SNSでのシェア
- 📝 使用体験のレビュー
- 💡 新機能のアイデア

### 🎵 音楽プロデューサーコミュニティ
- BeatStarsでの作品シェア
- プロンプト改善提案
- ジャンル固有のフィードバック
- アートワーク生成事例の共有

---

## 🏆 プロジェクト統計

![GitHub stars](https://img.shields.io/github/stars/phonon-py/beatstars-artwork-generator?style=social)
![GitHub forks](https://img.shields.io/github/forks/phonon-py/beatstars-artwork-generator?style=social)
![GitHub issues](https://img.shields.io/github/issues/phonon-py/beatstars-artwork-generator)
![GitHub license](https://img.shields.io/github/license/phonon-py/beatstars-artwork-generator)

**🎵 音楽プロデューサーのために、音楽プロデューサーによって作られました 🎵**

---

*このツールはMicrosoft Copilot企業版の機能を最大限活用するよう設計されており、BeatStarsプラットフォームでの音楽配信に最適化されたアートワーク生成をサポートします。*