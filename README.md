
# 🌐 KariPom Web

**インストール不要。ブラウザで開くだけ。**
KariPom Webは、PythonアプリとしてPC音声とのリアルタイム口パクを楽しめる **[KariPom Desktop](https://github.com/kariagepompadour/KariPom-Desktop)** をベースに、ブラウザだけで動くように移植したWeb版です。

Python・EXE・APIキーは一切不要です。対応ブラウザで `index.html` を開く（またはGitHub Pages版を開く）だけで、その場で動きます。

## 🚀 今すぐ試す（GitHub Pages）

**➡️ [KariPom Webを開く](#)**（公開後にURLを追記します）

インストール・ダウンロード不要で、上記リンクを開くだけですぐに使えます。

## 🐰 これは何？

かりポムは、元々M5Stack CoreS3で作った顔ロボットです。

実機がなくても「かりポム」を気軽に試してもらえるように、まずPC単体で動く KariPom Desktop（Pythonアプリ）を作りました。

でも、ちょっと試してみるためだけにアプリをダウンロードしてインストールするのは、意外とハードルが高いものです。

「それなら、ブラウザで開くだけで試せるようにしよう」

そうして作ったのが、この KariPom Web です。インストールもPythonもAPIキーも必要ありません。

ChatGPTなど、PCから再生される音声に合わせて、画面の「かりポム」がリアルタイムに口パクします。会話していないときも、瞬きしたり鼻をヒクヒクさせたりしながら画面の中で過ごします。

## ✨ Features

- **Character**：KariPom／Miss KariPom／None（顔を表示しない）の3種類
- **Visualizer**：口パクする通常の「Face」を含む、全9種類のオーディオビジュアライザー
- **Lighting**：レトロアーケード風スクリーンセーバーなどを含む、全25種類の背景演出（Noneを含む）
- 画面下の3ボタン操作（左1/3＝前へ、中央1/3＝無操作、右1/3＝次へ）でCharacter・Visualizer・Lightingをそれぞれ切り替え
- Visualizer Random／Lighting Randomで、3分ごとの自動切り替えもおまかせ可能

## 🎧 仕組み（PC音声の取得方法）

KariPom Webは、ChatGPT APIなどと直接連携しているわけではありません。

Chrome／Chromium系ブラウザの **「画面・タブ音声共有」機能**（`getDisplayMedia`）を使って、PC上で実際に再生されている音声（ChatGPTの声など）を取得し、その音声をブラウザ内の **Web Audio API** でリアルタイム解析して、口パク・EQ・各種Visualizerを動かしています。

**音声データを外部サーバーへ送信する処理は、現在のコードには存在しません。** 取得した音声はブラウザのメモリ上で解析されるだけで、どこにも送信・保存されません（コードは単一の `index.html` ファイルにすべて収まっており、内容はブラウザの「ページのソースを表示」でどなたでも確認できます）。

マイク入力には対応していません。PCの中で再生されている音声（タブ音声・システム音声）を共有する方式です。

## 🖥️ 使い方

1. Chrome／Chromium系ブラウザで、GitHub Pages版を開く（またはダウンロードした `index.html` を開く）。
2. 画面中央の「🔊 PC音声を開始」ボタンを押す。
3. 共有ダイアログで、かりポムに喋らせたい対象（ChatGPTのタブなど）を選び、**「タブの音声も共有する」を必ずONにする**。
4. 対象タブで音声を再生すると、その声に合わせてかりポムが口パクします。

## 🌏 対応ブラウザについて

PC音声の共有（タブ音声共有）は、現状では **Chrome／Chromium系ブラウザを推奨**します。Chromeであれば、ローカルに保存した `index.html` を直接開いた場合・GitHub Pagesなどのhttps環境で開いた場合のどちらでも動作します。

## 🐰 姉妹プロジェクト

- **[KariPom](https://github.com/kariagepompadour/KariPom)** — M5Stack CoreS3を使った、しゃべって動くデスクトップ・アニマトロニクスロボット本体
- **[KariPom Desktop](https://github.com/kariagepompadour/KariPom-Desktop)** — Pythonで動く、PCスタンドアロン版（Windows／macOS／Linux対応）
- **KariPom Web**（本リポジトリ）— ブラウザだけで動く、インストール不要のWeb版

## 📄 License

ソースコードは **MIT License** で公開しています。詳細は [LICENSE](LICENSE) をご覧ください。

Copyright (c) 2026 Kariage POMPADOUR Entertainment Corporation

### KariPom / かりポム ブランドについて

MIT Licenseは、このリポジトリに含まれるソフトウェアコードの利用条件を定めるものです。

**「KariPom」「かりポム」の名称、ロゴ、キャラクターその他のブランド要素について、MIT Licenseによる使用許諾を与えるものではありません。**

---

## Welcome to KariPom World!

ブラウザを開けば、あなたのPCにも、かりポムがやってきます。
