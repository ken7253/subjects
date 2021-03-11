# ModernJavaScript

## description

このリポジトリは現代的なJavaScriptの基礎を学ぶための課題です。  
JavaScriptの基礎的な文法をマスターした方向けに開発をしています。  
環境構築から始まり、より高度な書き方を学び個人開発が行えるレベルまでのサポートを行います。

## npm環境構築

npmはjavascriptのパッケージマネージャーとしてNodejsのインストール時に付いてきます。  
Webサイトやサービスの表現力や機能の拡大に伴い開発に必須のツールとなっています。  
まずは、自力でnpmを利用できるようになるための準備を行います。  

まずはPowerShellやコマンドプロンプトなどでこのディレクトリを開きましょう。  
ちなみにVSCodeの場合は左のエクスプローラーから

1. 対象のフォルダを右クリック（今回は `modern-javascript` です）
2. 統合ターミナルで開くを選択

上記手順で選択すると下部に選んだディレクトリが開いた状態でターミナルが立ち上がります。  
ターミナルが下記のようになっていることを確認して  

```ps
PS **\subject\modern-javascript> 
```

（ >の左側が `\subject\modern-javascript>` となっていれば大丈夫です！ ）  

```shell
npm init -y
```

と打ち込みnpmを初期化しましょう。  
そうすると新しく `package.json` というファイルが生成されます。  

### package.json is 何？

package.jsonはその名の通りjsのパッケージ（モジュール）を管理するのファイルです。詳しくは[こちら](https://qiita.com/righteous/items/e5448cb2e7e11ab7d477)が参考になります。  
読むのめんどくさい人はjavascriptの環境を記録しておく場所とでも覚えてください｡  
後々パッケージを追加していくとこのファイルの記述が増えます。  

例えばサイトを作るとき下記のようなコードを(コピペで)head内に書いたことがあるかもしれませんが  

```html
<script type="text/javascript" src="https://code.jquery.com/jquery-***.min.js"></script>
```

npmを使った開発ではそんなことはせずpackage.jsonで管理します。  

## 実際にパッケージを使ってみる

では、試しに何かパッケージを入れてみましょう。  
ここではローカルサーバーを建てることのできる `http-server` というパッケージを利用します。  
開いているターミナルで下記のコマンドを打ちましょう。  

```npm
npm install --seve-dev http-server
```

これでプロジェクトに開発用サーバーが用意されました。  
今までだとローカルサーバーを立ち上げるのにはXAMPPというソフトをインストールして、設定をしてファイルを置いてApacheを起動して…  
という手順が必要かつ無駄な機能も多いのでこっちのほうが使いやすいですね、しかもパッケージの情報はpackage.jsonで管理されているので誰でも同じ環境ですぐに開発が始められます。  

インストールされたら、下記の内容をpackage.jsonに記載しましょう。

```json
"scripts": {
  "server": "http-server ."
}
```

そうすると `npm run server` というコマンドでサーバーが起動します。  

## 参考資料

- [http-server - npm](https://www.npmjs.com/package/http-server)
- [jspremier](https://jsprimer.net/)
