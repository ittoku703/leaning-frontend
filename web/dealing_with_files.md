## ファイルの扱い

> 参考：https://developer.mozilla.org/ja/docs/Learn/Getting_started_with_the_web/Dealing_with_files
>
> ここでは、Webサイトに合理的なファイル構造を設定できるように、注意すべきいくつかの問題について説明します。

### コンピュータ上でWebサイトがあるべき場所

自分のコンピュータ上のWebサイトでローカルで作業をしている時、関連するすべてのファイルを、サーバー上に公開されたWebサイトのファイルと同じにする必要がある。

自分のコンピュータのWebサイトのフォルダは、デスクトップ、ホームフォルダの中、またはハードディスクのルートなどに置くと良い。

1. まずはWebサイトのプロジェクトを保存する場所を選択。ファイル名を`web-projects`などの名前で新しいフォルダを作成する。このフォルダはWebサイトのプロジェクト全てを保持するところである。
2. 上記のフォルダの中に、最初のWebサイトを格納する別のフォルダを作成する。ファイル名は`test-site`などの適当な名前にする。

### 大文字と空白の除外

**フォルダやファイルに空白のない全て小文字で名前をつける理由**

1. 多くのコンピュータ、特にWebサーバーでは大文字と小文字が区別される。
   例えば、`test-site/MyImage.png`と`test-site/myimage.png`は別のファイルとなる。
2. ブラウザ、Webサーバー、プログラミング言語は、空白の扱いが一貫していない。
   **ファイル名に空白を使用するとおきること**
   1. システムによっては、2つのファイル名として扱う場合がある。
   2. サーバーによっては、ファイル名の空白を%20（URIの空白の文字コード）に置き換えるので、リンクが壊れてしまう。

ファイル名で空白を使いたい場合はハイフンを代わりに使う。

理由は、Googleの検索エンジンはハイフンを単語の区切りとして扱うが、アンダースコアは違うから。

### Webサイトはどのような構成にするべきか

1. `index.html`
> このファイルは、あなたのホームページの内容、最初にあなたのサイトへ訪れた時に見るテキストと画像が含まれる。
2. `images/`
> このフォルダは、サイトで使用されるすべての画像を格納する。

3. `styles/`

> このフォルダには、コンテンツのスタイルを設定するためのCSSコードを入れる。

4. `scripts/`

> このフォルダには、サイトにインタラクティブ機能を追加するために使用されるJavaScriptコードを入れる。

### ファイルパス

**ファイルパスの一般的なルール**

- HTMLファイルと画像ファイルが同じディレクトリにある場合は`my-image.jpg`と指定する。
- HTMLファイルと画像ファイルがサブディレクトリにある場合は`subdhirectory/my-image.jpg`と指定する。
- HTMLファイルと画像ファイルが上階層にある場合は`../my-image.jpg`と指定する。
- `../subdirectory/another-subdirectory/my-image.jpg`など好きなだけ組み合わせることもできる

> Windowsのファイルシステムでは、スラッシュではなくバックスラッシュ、または￥記号を使用する。これはHTMLでは使用できない。

