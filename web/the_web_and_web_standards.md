## WebおよびWeb標準

> Webに関する有用な背景、どのように生まれたのか、Web標準テクノロジーとはなにか、どのように連携するのか、などを説明する
>
> Ref: https://developer.mozilla.org/en-US/docs/Learn/Getting_started_with_the_web/The_web_and_web_standards

### Webの簡単な歴史

- 1960年代後半に米軍が[ARPANET](https://developer.mozilla.org/en-US/docs/Glossary/Arpanet)と呼ばれる通信ネットワークを開発した。これは「パケット交換」や「TCP/IP」の最初の実装を特徴としていたため、Webの先駆者とみなすことだできる。この２つは、**インターネットが構築されているインフラストラクチャの基盤**を形成している
- 1980年、Tim Berners-Leeが、異なるノード間のリンクの概念を特徴するENQUIREと呼ばれるノートプログラムを作成する
- 1990年後半には、TimBLは「HTTP」「HTML」「WorldWideWeb」を作成する

### Web標準

- Webサイトを構築するために使用するテクノロジーのこと
- 標準化団体
  - [WHATWG](https://whatwg.org/)
  - [ECMA](https://www.ecma-international.org/)
  - [Khronos](https://www.khronos.org/)

### オープンスタンダード

- Web標準の重要な側面の１つは、特許やライセンスに邪魔されることなく自由に貢献することができ、誰でも無料でWebサイトを構築するためのコードを記述することができる

### Webを壊さないでください

- それはつまり、導入される新しいWebテクノロジーは、以前のものと下位互換性がある必要があること

### Web開発者であることは良いことです

- 唯一の定数は変化です。

### 最新のWebテクノロジーの概要

- ブラウザ
  - Webブラウザは、人々がWebを利用するために使用するソフトウェアプログラム
- HTTP(Hyper Text Transfer Protocol)
  - WebブラウザがWebサーバー（Webサイトが保存されている場所）と通信できるようにするメッセージプロトコル。実際の構文は、人間が読める形式ではないが、こんな感じ

```text
"Hello web server. Can you give me the files I need to render bbc.co.uk"?

"Sure thing web browser — here you go"

[Downloads files and renders web page]
```

#### HTML, CSS, JavaScript

- **HTML（Hyper Text Markup Language）**は、コンテンツをラップ（マークアップ）して意味（セマンティクス）と構造を与えることのでき、さまざまな要素で構成されるマークアップ言語

```html
<h1>This is a top-level heading</h1>

<p>This is a paragraph of text.</p>

<img src="cat.jpg" alt="A picture of my cat">
```

- **CSS（Cascade Style Sheet）**は、テキストや背景色の設定、境界線の追加、アニメーション、特定の方法でのページのレイアウトなど、HTMLにスタイルを適用するためにルールベースの言語

```css
p {
  color: red;
}
```

- **JavaScript**は、動的なスタイルの切り替えから、サーバーからフェッチ、複雑な3Dグラフィックまで、Webサイトに双方向性を追加するために使用するプログラミング言語

```javascript
let pElem = document.querySelector('p');
pElem.textContent = 'We changed the text!';
```

### ツール

- ブラウザの開発者ツール
- テストツール
- リンター
- ミニファイア

### サーバー側の言語とフレームワーク

- HTML, CSS, JavaScriptはフロントエンド（クライアント側）で動作する言語。
- ASP.NET, Python, PHP, Rubyはバックエンド（サーバー側）で動作する言語。結果がブラウザに送信されて表示される前に、サーバー上で実行される。
- 一般的なサーバー処理の順番
  1. データベースからデータを取得する。
  1. データを含むHTMLを生成する。
  1. HTMLをブラウザに送信してユーザに表示する。

### Webのベストプラクティス

- Web開発を行う場合、不確実性の主な原因は、各ユーザーがWebサイトを表示するテクノロジーの組み合わせがわからない事実です
  - ユーザー1は、小さくて狭い画面のiPhoneでそれを見ている可能性があります。
  - ユーザー2は、ワイドスクリーンモニターが接続されたWindowsラップトップでそれを見ている可能性があります。
  - ユーザー3は目が見えず、スクリーンリーダーを使用してWebページを読み上げている可能性があります。
  - ユーザー4は、最新のブラウザーを実行できない非常に古いデスクトップマシンを使用している可能性があります。
- このため、防御的に設計する必要がある。つまりWebサイトをできるだけ柔軟にして、上記の全てのユーザが同じようにならない場合でも、Webサイトを利用できるようにする

- **ブラウザ間の互換性**
  - Webページができるだけ多くのデバイスで機能することを確認すること。

- **レスポンシブウェブデザイン**
  - 機能とレイアウトを柔軟にして様々なブラウザに自動的に適用できるようにすること
- **パフォーマンス**
  - Webサイトをできるだけ早くロードするだけでなく、ユーザーがイライラして別の場所に移動しないように、Webサイトを直感的で使いやすいものにすること
- **アクセシビリティ**
  - できるだけ多くの異なる種類の人々がWebサイトを使用できるようにすること。それは、視覚障害、聴覚障害、認知障害。また、若者や老人、異文化の人々、モバイルデバイスを使用している人々、ネットワーク接続の信頼性の低いか遅い人々など
- **国際化**
  - さまざまな言語を自分の言語で話すさまざまな文化の人々がWebサイトを使用できるようにすること。
- **プライバシーとセキュリティ**
  - プライバシーは、人々が個人的にビジネスを行うことを許可し、彼らをスパイしたり、絶対に必要以上のデータを収集したりしないこと。セキュリティは、悪意のあるユーザーがWebサイトに含まれる情報をあなたやあなたのユーザーから盗むことがないように、Webサイトを構築すること
