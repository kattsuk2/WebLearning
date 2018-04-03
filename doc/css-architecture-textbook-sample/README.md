# Web制作者のためのCSS設計の教科書サンプルデータ

本データは『Web制作者のためのCSS設計の教科書』で解説しているコードの一部をサンプルデータとして用意したものです。

## データについて

本書はCSS設計における考え方とその実装例についてフォーカスし、コードを一部省略した記述をしています。そのため、書籍に記述されているコードをそのまま記述するだけでは、キャプチャ画像の通りの見た目にならないこともあります。

本サンプルデータでは、キャプチャを再現するための装飾スタイルを加えています。

## 掲載コードの一部訂正

### 初版（2014年7月21日 訂正）

#### P.115 アイコンフォントの実装例

```
/* 不要 */
@import url(http://weloveiconfonts.com/api/?family=fontawesome);
```

上記の一行はサンプルを実行する上では不要となります。（後述されている`@font-face`で各フォントデータを読み込むようにしているため）

#### P.137 グリッドの実装例

```
/* 記述の誤り */
.grid__item {
  float: left;
  box-sizing: border-box; /* border-widthとpaddingをwidthに含める */
  width: 16.667%;
  > div {
    background-color: rgba(#489);
  }
}

/* 正しい記述 */
.grid__item {
  float: left;
  box-sizing: border-box; /* border-widthとpaddingをwidthに含める */
  width: 16.667%;
}
.grid__item > div {
  background-color: rgba(#489);
}
```

上記はCSSのコードですが、本書上では一部がSass（SCSS)の記述となっていましたので、訂正します。
