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

Goプロジェクトのディレクトリ構成
```
vscode ➜ /go/src $ tree gostudy
gostudy
├── cmd #実行バイナリ用のソースを配置
├── go.mod #依存管理ファイル
├── gostudy.go #ソースコード
├── gostudy_test.go #テストコード
├── type.go #typeを定義しているものなどはファイルを分ける
├── type_test.go
├── Makefile #ビルド定義のほかタスクランナー的にも利用
├── testdata #fixtureなどテストデータが配置
├── _tools #Go以外のシェルスクリプトなどを配置
└── version.go
```

依存管理
- `go mod init`により依存関係の定義と管理のファイルを作成する。
- `go get/test/build`の各種コマンド実行のたびに更新され、go.sumというファイルも作成される
  - go.sumはモジュールリストやそのスナップショットのハッシュ値情報を記録するバージョンロックのためのファイル
- ソースコード内にimportを追加しさえすればgo getでgo.mod/go.sumの更新ができる



