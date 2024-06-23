# PythonWEB演習2

## 静的ファイルの取り扱い
動的要素のない静的なファイルの取り扱いを学びます。
CSSファイル(css/style.css)をリンクさせてましょう。

```python main.py
#....中略....
# Flaskインスタンスを生成
app = Flask(__name__,static_folder='static')
#....中略....
```

```html:test.html
    <!-- 中略 -->
    <title>Flask Test</title>
    <link rel="stylesheet" href="static/css/style.css">
</head>
```
作業フォルダ内にstaticフォルダを作成、staticフォルダ内にcssフォルダを作成、cssフォルダ内にcssファイル(`style.css`)を作成します。

```css:style.css
p{
    color:#f00;
}
```

現時点でのディレクトリとファイルの構成
```
├── web
    ├── main.py
    ├── static
    │   └── css
    │       └── style.css
    └── templates
        └── test.html
```

## KujiraCafeの再構築

実際にKujiraCafeのデータをFlaskで再構築していきます。
URLと各ページの関係は下記の通りとします。

### KujiraCafeのデータを配置

JupyterLabの作業ディレクトリ直下に新しいディレクトリ(フォルダ)を作成します。ディレクトリ名は`kujira_cafe`とします。

`kujira_cafe`直下に`templates`と`statics`ディレクトリを作成。  
`templates`内に全ての`htmlファイル`を移動。  
`statics`ディレクトリ直下に`css`と`images`ディレクトリを移動します。

pythonファイル`app.py`を`kujira_cafe`直下に作成します。

現時点でのディレクトリとファイルの構成
```
├── kujira_cafe
│   ├── app.py
│   ├── statics
│   │   ├── css
│   │   │   └── style.css
│   │   └── images
│   │       ├── access-hero.jpg
│   │       ├── banner.jpg
│   │       ├── contact-hero.jpg
│   │       ├── gotop.svg
│   │       ├── home-hero.jpg
│   │       ├── item1.jpg
│   │       ├── item2.jpg
│   │       ├── item3.jpg
│   │       ├── item4.jpg
│   │       ├── item5.jpg
│   │       ├── item6.jpg
│   │       ├── item7.jpg
│   │       ├── item8.jpg
│   │       ├── item9.jpg
│   │       ├── logo-whale.svg
│   │       ├── logo.svg
│   │       ├── map.png
│   │       ├── menu-hero.jpg
│   │       └── stripe.png
│   └── templates
│       ├── access.html
│       ├── contact.html
│       ├── index.html
│       ├── menu.html
│       └── result.html
```
## ルーティングの設定
URLとプログラム動作の関係をルーティングと言います。
リクエストされたURLと動作するメソッドを紐つけることでWebアプリケーションを管理します。この役割を**コントローラー**といいます。

| URL | method | 関数名 | テンプレート |
| ---- | ---- |  ---- | ---- |
| / | GET | index | index.html |
| /menu | GET | menu | menu.html |
| /access | GET | access | access.html |
| /contact | GET | contact | contact.html |
| /contact | POST | send | |
| /result | GET | result | result.html |


### Flask URLコントローラーと既存コンテンツを紐づける



## Excelデータの取得とWebコンテンツの動的生成

## カテゴリー検索機能の実装(POSTとセッション)

## 課題　お知らせ機能の実装

## 課題イメージ
  
<img src="images/kujiracafe.png">