# nodeのバージョン確認
$ node -v

# TypeScriptのインストール

typescriptのグローバルインストール
$ npm install -g typescript@5.2.2
グローバルにインストールされた場合はどのディレクトリからでもアクセスできる。


# typescriptのバージョン確認

$ tsc -v
ts -vじゃないので注意

# ファイルの拡張子
sample.ts
.tsをつけるとtypescriptのファイルになる


# tscコマンドによるJavaScriptへの変換
$ tsc sample.ts
tsc = TypeScriptCompile


# tscコマンド実行時のJavaScriptファイルの出力先
/ts-practice
 sample.ts
 sample.js

同一ディレクトリに作成される。

# jsファイルの実行
$ node sample.js

// Hello, TypeScript!

# ts-nodeについて
通常はtscコマンドによるコンパイルを行いjsファイルにしてからnodeコマンドで実行する必要があるが
ts-nodeコマンドを利用する場合コンパイルしてjsファイルを生成することなく、tsファイルのまま実行ができる。
学習環境や開発環境で重宝する。

# ts-nodeをインストール

$ npm install -g ts-node@10.9.1

このコマンドもグローバルでインストールするとコマンドライン上でディレクトリを気にすることなく利用できる

# ts-nodeによる.tsファイルの実行

$ ts-node sample.ts

// Hello, TypeScript!
// sample.jsは生成されない

# tsconfig.jsonの作成
このファイルにはTypeScriptコンパイラの設定を記述する。
$ tsc --init
でtsconfig.jsonが作成される。

# tsconfig.jsonの出力先
/ts-practice
 sample.ts
 tsconfig.json
 
# tsconfig.jsonのコンパイラオプションの設定
"target"は変換されたjsのバージョンを指定する
moduleオプションは、変換後のJavaScriptのモジュールシステムを指定する（CommonJSなど）

outDirはコンパイルされたjsファイルを出力するディレクトリを指定する。デフォルトではカレントディレクトリになっている。

