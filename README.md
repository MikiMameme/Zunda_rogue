# ずんだローグ (プロトタイプ)

[![Rust](https://img.shields.io/badge/Rust-1.70%2B-black?logo=rust&logoColor=white)](https://www.rust-lang.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Made with Gemini](https://img.shields.io/badge/Made%20with-Gemini-blue?logo=google-gemini&logoColor=white)](https://gemini.google.com/)
[![Author](https://img.shields.io/badge/Author-Miki%20Mame-lightgrey)](https://github.com/MikiMameme)  



Rustと `macroquad` で作成された、ローグライクゲームのプロトタイプです。
プレイヤーは「東北ずん子」を操作し、「ずんだもん」を放って敵を倒しながら、ステージを進んでいきます。

## 遊び方・操作方法

- **矢印キー (↑↓←→)** : 移動
- **Z または Spaceキー** : 攻撃
  - 向いている方向へ「ずんだもん」を最大3マス飛ばします。敵に当たると倒すことができます。
- **Enterキー** : ターン経過（待機用）
- **Escapeキー** : ゲームを終了（ゲームオーバー時など）

## ゲームのルール

- **HPと残機**:
  - 画面左上のアイコンは「残機」です。
  - その下のずんだ餅アイコンは「HP」です（最大3）。
- **回復**: フィールドに落ちている「ずんだ餅」を拾うと、HPが全回復します。
- **ダメージとゲームオーバー**:
  - 敵とぶつかるとHPが1減ります、かわりにずん子は少しの間（約2秒間）無敵になります。
  - HPが0になると残機を1つ消費してHPが全回復します。
  - 残機が0の状態でHPが0になるとゲームオーバーになります。
- **ステージ進行**: 上り階段まで到達すると、次のステージへと進みます。

## インストールとビルド方法
- `zunda_rogue_release.zip` をダウンロードし展開してください。
- `zunda_rogue.exe` を実行します。

### MSVCR110.dll がないため、プログラムを開始できません。プログラムを再インストールすると、この問題が解決する場合があります。と出た場合  
Microsoft Visual C++ 再頒布可能パッケージをインストールすると解決できる場合があります。  
[サポートされている最新の Visual C++ 再頒布可能パッケージのダウンロード](https://learn.microsoft.com/ja-jp/cpp/windows/latest-supported-vc-redist?view=msvc-170)

## 動作環境
- Windows10/Windows11が正常動作するパソコン


## 使用技術
- 言語: Rust (Edition 2024)
- メインライブラリ: [macroquad](https://github.com/not-fl3/macroquad)

## クレジット・著作権・ガイドライン

### キャラクター・ガイドラインについて
- **「ずんだもん」「東北ずん子」は[SSS合同会社（東北ずん子・ずんだもんプロジェクト）](https://zunko.jp/)の登録商標です。**
- このアプリはSSS合同会社の二次創作ガイドラインに準拠して制作された二次創作ゲームです。
- 非商用かつSSS合同会社のガイドラインを守る場合に限り、プレイ動画の実況配信および収益化を許可します。

### 開発・素材に関する情報
- **開発**: K.N (2026)
- **開発協力 (AI)**: Google Antigravity, Claude, Gemini
- **画像素材**: [tohoku_pixel](https://zunko.jp/con_illust.html) 等
- **フォント**: Noto Sans JP
