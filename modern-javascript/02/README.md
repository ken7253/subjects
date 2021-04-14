# ModernJavaScript-02

## description

このリポジトリは現代的なJavaScriptの基礎を学ぶための課題です。  
JavaScriptの基礎的な文法をマスターした方向けに開発をしています。  
環境構築から始まり、より高度な書き方を学び個人開発が行えるレベルまでのサポートを行います。

ブラウザで見たい場合は[こちら](https://github.com/ken7253/subjects/blob/master/modern-javascript/02/README.md)

## 開発に使うパッケージについて

### 開発用パッケージと本番用パッケージ

前回 `http-server` のインストール時に書きのようなコマンドを実行しました。  

```npm
  npm install --save-dev http-server
```

その際に `package.json` にこのような記述が追加されたかと思われます。  

```json
  ...
  "devDependencies": {
    "http-server": "^0.12.3"
  }
  ...
```

前回のドキュメントでも下記のように解説していますが `package.json` はパッケージの依存関係を記録しているため、パッケージのインストール時にその内容が自動的に記載されます。  

> package.jsonはその名の通りjsのパッケージ（モジュール）を管理するのファイルです。詳しくは[こちら](https://qiita.com/righteous/items/e5448cb2e7e11ab7d477)が参考になります。  
> 読むのめんどくさい人はjavascriptの環境を記録しておく場所とでも覚えてください｡  
