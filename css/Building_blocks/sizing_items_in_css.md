# CSSによるサイズ設定

このページでは、要素のサイズを設定する方法をまとめ、サイジングに役立ついくつかの用語について見ていきます。

## 要素固有のサイズ

HTML要素には自然なサイズがあり、それはCSSの影響を受ける前に設定されます。

画像はページに埋め込む画像ファイルで定義された幅と高さがあります。このサイズは固有サイズと呼ばれ、画像自体に由来します。

空の`div`要素には独自のサイズはなく、コンテンツのないHTMLにボーダーを設定しても線みたいなものが出力されるだけです。ボーダーとして機能させるには、`width, height`を指定するか、入れ子にテキストなどを入れる必要があります。

### サイズの指定

要素にサイズが指定されている場合、外部サイズと呼びます。外部サイズを定義する注意点として、オーバーフローしやすくなります。

```css
.box {
  width: 250px;
  height: 250px;
}
```

### 比率指定

パーセンテージで長さなどの単位を指定することです。

パーセンテージを使用する場合、何に対しての比率であるか確認する必要があります。コンテナ内のボックスの場合、子ボックスの幅にパーセンテージを与えると、親コンテナの幅のパーセンテージになります。

```css
.container {
  width: 100px;
}

.container > .box {
  width: 50%; /* 50px */
}
```

### マージンとパディングの比率

マージンとパディングにパーセンテージを使用すると、値はインラインサイズから計算されます。つまりマージンとパディングは親要素の大きさに比例して大きくなったり小さくなったりすることです。

### 最小サイズ、最大サイズ

常に特定の高さ以上にしたい場合は`min-height`プロパティを、常に特定の高さ以下にしたい場合は`max-height`プロパティを使う。

これらは、オーバーフローを回避しながら、可変長のコンテンツを処理するのに非常に役立ちます。

あと画像をレスポンシブにするときに便利です。大きすぎる画像の場合、最大サイズを指定することで、適切に縮小されます。

## ビューポートに関する単位

ビューポート（ブラウザのページ表示領域）にも`vw, vh`のようなサイズがあります。これらの単位を使用すると、ユーザのビューポートを基準にしてサイズを変更できます。

1vhはビューポートの高さ1%で、vwも幅1%です。

ビューポートに応じてサイズを調節すると、デザインで役立ちます。現ページのヒーローセクションを他のコンテンツの前に表示させたい場合、ページのその部分を100vhの高さにすると、残りのコンテンツはビューポートの下に押しやられてしまい、ドキュメントがスクロールされたときにのみ表示されてしまいます。

## まとめ

CSSレイアウトで、レイアウトメソッドを習得する際にサイズ設定が非常に重要になるため、このページで説明した概念を理解しておくとよいと思います。
