# みんなのGo言語

## 第１章
Goの環境構築
- OS: Mac
- Editor: Visual Studio Code
- Runtime: Docker

ライブラリ(Homebrewを使用)
- tree: ディレクトリ構造の視覚化
- vim: ファイルの編集
- ghq: 階層構造でソースコードリポジトリを取得・管理するためのツール
- peco: ターミナル上で標準出力をインクリメンタルにフィルタするUIを提供するツール

パッケージ導入(VScodeのターミナル上でgo getを使用)
- gore: Goの代表的なREPL(対話的にプログラムを実行し評価を出力する環境)
  - Hello World実行
- gocode: Goのコード補完ソフトウェア
- pp: pp.Print()を使うと任意の型のオブジェクトを色付きでpretty print(整形表示)してくれる
- goimports: コードフォーマット、パッケージを読み込むimport文の挿入と削除を自動で行なってくれるライブラリ
- golint: Goらしくないコーディングスタイルに対して警告してくれる静的解析ツール(現在は[こちら](https://zenn.dev/sanpo_shiho/articles/09d1da9af91998)の理由により非推奨)
  - cf. govet: 標準でGoに同梱されている静的解析ツール
- godoc: ブラウザでのドキュメント閲覧を可能にするツール

