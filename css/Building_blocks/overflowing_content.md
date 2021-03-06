# 要素のはみ出し

> 参考：https://developer.mozilla.org/ja/docs/Learn/CSS/Building_blocks/Overflowing_content

このページでは、コンテンツのオーバーフローについて紹介します。

## オーバーフローとは

CSSの全てがボックスであり`width, height, inline-size, block-size`の値を与えることでボックスのサイズを制御してきました。

オーバーフローは、コンテンツがボックス内に収まりきらないという場合に発生します。

### CSSのデータ損失の回避

**よくあるオーバーフローの発生する場面**

- heightで高さを設定しており、コンテンツの量がその設定した高さより領域を使ってしまいボックスからはみ出し、下の段落にかぶさってしまう。
- inlineを設定しており、コンテンツの大きさがそのボックスより大きい場合に、ボックスからはみ出てしまう。

CSSでは可能な限りコンテンツを隠しません。データの損失が発生してしまうからです。これは開発者がデータが損していることに気がつかない場合があるからです。

ボックスをwidth, heightで制御している場合はオーバーフローに注意しなければいけない。

## overflowプロパティ

`overflow`プロパティは、要素のオーバーフローを制御します。デフォルトの値は`visible`です。

**overflowの値**

- `visible`、コンテンツを隠しません。
- `hidden`、コンテンツを隠します。
- `scroll`、隠しますが、はみ出たコンテンツはスクロールで見ることができます。
- `auto`、コンテンツがボックスに収まらない場合にのみ、スクロールします。

他にも、`overflow-y, overlofw-x`プロパティもあります。

overflow-xは文字が見切れてしまうことの回避策としては推奨されていません。、`word-break, overflow-wrap`を使う方が推奨されています。

## オーバーフローとブロック整形コンテキスト

CSSにはブロック整形コンテキスト（Block Formatting Context）の概念があります。	`scroll,auto`などのオーバーフローの設定でBFCは作成されます。詳しくは[ブロック整形コンテキスト](https://developer.mozilla.org/ja/docs/Web/Guide/CSS/Block_formatting_context)で見ることができます。

## オーバーフローの望ましくないウェブデザイン

モダンなレイアウト手法では、オーバーフローを管理します。

過去には固定された高さを使用して、実際にはお互いに関係のないボックスの底を揃えようとしました。それは脆く、レガシーなアプリケーションでは、コンテンツが他のコンテンツに重なってしまうのを見かけることがあります。理想はボックスサイズの固定に依存しないようなレイアウト調整を実現することです。

サイトを開発するときは常にオーバーフローの問題に注意する必要があります。大量のコンテンツと少量のコンテンツを含むデザインをテストし、テキストのフォントサイズを大きくし、CSSが堅牢に対処できているか確認する必要があります。オーバーフローの値を変更してコンテンツを非表示にしたり、スクロールバーを追加したりするのは特別な場合にのみ使用するべきです。
