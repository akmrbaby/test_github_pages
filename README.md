# test_html

GitHub Pagesで静的サイトを公開してみる。

## node.jsを使ってみる

事前準備 (npmとnode.jsのバージョン確認)
```sh
// npmを最新版に
sudo npm install -g npm@9.7.1

// nのインストール
sudo npm install -g n

// 安定版のnode.jsのインストール
sudo npm stable

// nコマンドを実行して、現時点で安定版のv18.16.0を選択
sudo n
```

プロジェクトの作成
```sh
// package.jsonの作成とexpressのインストール
npm init -y
sudo npm install -g express
sudo npm install -g express-generator

// expressアプリの作成 (アプリ名：express_app)
express express_app
cd express_app
npm install

// 依存関係に問題があれば無理やり解決
npm audit fix --force
```

git周りのメモ
```sh
// .gitignoreファイルの生成 (node_modules以下を無視)
echo "**/node_modules/" > .gitignore

// 開発用ブランチを切る
git checkout -b dev

// 編集結果をリモートリポジトリに反映
git add *
git commit -m "コメント"
git push origin dev

