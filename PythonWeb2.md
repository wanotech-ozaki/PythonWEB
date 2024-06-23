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

## Flask URLコントローラーと既存コンテンツを紐づける

###　KujiraCafeのデータを配置

## Excelデータの取得とWebコンテンツの動的生成

## カテゴリー検索機能の実装(POSTとセッション)

## 課題　お知らせ機能の実装

## 課題イメージ
  
<img src="images/kujiracafe.png">