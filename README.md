# Portfolio

公開している個人開発プロジェクトや開発環境をまとめています。

アプリケーションの実装だけでなく、要求整理、設計、責務分離、
開発・運用フロー、再現可能な開発環境まで含めて考えることを重視しています。

## Featured Projects

### [RAGScope](https://github.com/takashit16833/RAGScope)

現在開発中の、RAGシステムの検索結果、回答、引用、評価結果を観察し、
条件の異なる実験を比較・追跡するためのアプリケーションです。

検索から回答生成、評価までの途中結果と実験条件を記録し、
評価結果を根拠としてRAGシステムの設計判断を説明できることを目指しています。

RAGScopeアプリケーション本体はHaskell、
Embedding生成、reranking、回答生成などを担うAI推論サービスはPythonで実装しています。

また、コードだけでなく要求定義、ドメインモデル、システムアーキテクチャ、
機能設計、開発規約、ロードマップなども同じリポジトリで管理しています。

**見てほしいところ**

- RAGを「回答を生成する機能」だけでなく、実験・評価・比較まで含むシステムとして設計していること
- Haskellで実装するアプリケーションと、Pythonで実装するAI推論サービスの責務を分離していること
- アプリケーション、AI推論サービス、データベースなどの責務と依存関係を明示していること
- 要求、設計、実装、プロジェクト運用を継続的に整合させながら開発していること

---

### [Workbench-showcase](https://github.com/takashit16833/Workbench-showcase)

日常的に使用している非公開のWorkbenchから個人的な情報を除き、
ポートフォリオ向けに公開したバージョンです。

Workbenchは、Obsidian上で Task / Idea / Note / Project を扱う、自分とAI共用の作業基盤です。

単なるタスク管理ではなく、
アイデアから意思決定、実行、記録までをMarkdownを中心に扱えるようにしています。

以前はEmacsのOrg modeを使ってタスクや情報を管理していました。
そこで得た「テキストを中心に、自分の作業環境そのものを組み立てる」という感覚が、
Workbenchを作るきっかけの一つになっています。

TaskNotesなど既存のObsidianプラグインを活用しつつ、
Workbench固有の操作だけを自作プラグインとして追加しています。

**見てほしいところ**

- Task / Idea / Note / Project の役割とライフサイクルを明確に分けていること
- 既存プラグインの責務を尊重し、必要な機能だけを追加する設計
- AIエージェントが参加しても運用を壊さないためのルール、安全策、Git運用
- Markdownを正本とし、生成物やビューを再構築可能にしていること

---

### [.emacs.d](https://github.com/takashit16833/.emacs.d)

以前使用していたEmacsの設定です。
現在のメインエディタはVS Codeですが、当時はOrg modeでタスクや情報を管理したくて
Emacsを日常的な作業環境として使っていました。

`init.org` を設定の原本とするLiterate Configurationとして構成し、
Org Babelから `early-init.el` と `init.el` を生成します。

設定を単純に追加していくのではなく、
機能単位で責務を整理しながら管理しています。

Org modeを中心に自分の作業環境を組み立てていた経験は、
現在のWorkbenchの発想にもつながっています。

---

### [dotfiles](https://github.com/takashit16833/dotfiles)

macOSの開発・作業環境を再構築するためのdotfilesです。

設定ファイルだけでなく、インストール処理や各種ツールの設定も管理し、
新しい環境でもできるだけ同じ操作感を再現できるようにしています。

特にHammerspoonやRaycastを使い、
アプリケーションの起動、切り替え、ウィンドウ操作などを
できるだけキーボードから素早く行える環境にしています。

**見てほしいところ**

- HammerspoonやRaycastを利用したキーボード中心の操作環境
- 日常的な操作を小さな自動化の積み重ねで効率化していること
- 新しいMacでも同じ開発環境を再構築できるようにしていること
- 既存ファイルを無条件に上書きしないなど、セットアップ処理の安全性も考慮していること

## Other Public Repositories

### [obsidian-config-layer](https://github.com/takashit16833/obsidian-config-layer)

複数のObsidian Vaultで、
CSS、キーボードショートカット、必須community pluginを共有するための
desktop向けObsidianプラグインです。

Vault固有の設定を置き換えるのではなく、
共通設定をレイヤーとして重ねることを目的にしています。

共有設定はdotfilesなどVault外のディレクトリにも配置でき、
各Vault固有の設定と共存できます。

実装はAIに作成してもらっています。

---

### [QuickJump](https://github.com/takashit16833/QuickJump)

現在画面に見えているテキストへ、
キーボードだけですばやく移動するためのVS Code拡張です。

1文字または2文字を入力して移動候補を絞り込み、
表示されたhintを入力すると目的の位置へジャンプします。

複数のeditor groupに表示されているテキストにも対応しています。

実装はAIに作成してもらっています。

---

### [zmk-keyboard-torabo-tsuki-lp](https://github.com/takashit16833/zmk-keyboard-torabo-tsuki-lp)

Torabo Tsuki LP用のZMKファームウェア設定です。

左右分割キーボードのfirmwareとkeymapを管理しており、
キーマップには大西配列を採用しています。
