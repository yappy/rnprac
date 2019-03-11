# 環境整備

# Node
Node.js のバージョンを柔軟に変えられるツールというかスクリプト nodenv を使う。
github から clone してパスを通すだけ。色々察するものがある。
node-build プラグインを入れる。これも plugins/ 以下に clone するだけ。
アップデートはリポジトリの中に入って `$ git pull`。
.bashrc を書き換えたらシェルを再起動する。

1. `$ git clone https://github.com/nodenv/nodenv.git ~/.nodenv`
1. `export PATH=$HOME/.nodenv/bin:$PATH` を .bashrc に追加。
1. `$ nodenv init` で指示された内容に従う。
今回は `eval "$(nodenv init -)"` を .bashrc に追加。
1. `$ git clone https://github.com/nodenv/node-build.git "$(nodenv root)"/plugins/node-build`
1. `$ nodenv install -l`
1. `$ nodenv install 10.15.3` 
Node.js の公式サイトに行って推奨バージョンを確認する。
間違って最新版を入れてはいけない。
1. インストールリストの確認やアンインストールは versions, uninstall コマンドで可能。
実体は ./nodenv/versions/ にあるので直接削除しても可。
1. nodenv 自体のアンインストールは .nodenv を削除すればOK。
versions/ 以下の Node も全部消える。あと .bashrc を元に戻すこと。
