# 結合子

> 参考：https://developer.mozilla.org/ja/docs/Learn/CSS/Building_blocks/Selectors/Combinators

このページでは、他のセレクタと組み合わせて、互いの関係や文書内のコンテンツの位置を明確にするコンビネーターについて紹介します。

## 子孫コンビネータ

これは、最初のセレクタと一致する要素と、その子である2番目のセレクタと一致する要素が選択されるセレクタです。

```css
article p {}
.box p {}
```

## 子コンビネータ

これは、最初のセレクタと一致する要素と、直接の子である２番目のセレクタと一致する要素が選択されるセレクタです。

```css
article > h1 {}
p > span {}
```

## 隣接する兄弟コンビネータ

最初のセレクタと一致する要素と、同じ階層の隣接している2番目のセレクタと一致する要素が選択されるセレクタです。

```css
p + img {}
```

## 一般的な兄弟コンビネータ

最初のセレクタと一致する要素と、同じ階層にいる2番目のセレクタと一致する要素が選択されるセレクタです。

```css
p ~ img {}
```

## コンビネータの使用

これまでに学んできたセレクタと組み合わせて、より細かなCSSセレクタを選択することができます。

```css
ul > li[class="a"] {}
```
