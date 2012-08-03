## inputcount

## これは何？

入力フォームで何文字入力できるのかいつも聞かれるので作ってみました。
よく、Twitterアプリなんかででてくるあの表示です。

このスクリプトは JQuery 1.7 以上を必要とします。
一応、IE6/7/8/9, Safari5/6, Chrome20/21 で試しています。

## デモページ

以下に用意しました。

http://cafelounge.net/dev/?jquery-inputcount

## 使い方

前提として、以下を組み込みます。

```html
<link type="text/css" rel="stylesheet" href="jquery.inputcount.css" />
<script type="text/javascript" src="jquery-1.7.2.min.js"></script>
<script type="text/javascript" src="jquery.inputcount.js"></script>
```

input タグに maxlength 属性を追加します。

```html
<input type="text" name="username" maxlength="30" />
<input type="password" name="password" maxlength="30" />
<textarea name="commenct" maxlength="400" rows="8" />
```

あとは、どこかのタイミングで入力タグに対して以下を呼び出してください。

```js
$(function(){
	if ($.fn.textcount) {
		$('textarea, input[type="text"], input[type="password"]').textcount();
	}
});
```

これだけです。

## インストール

```
$ cd path/to/css
$ wget https://raw.github.com/miko2u/jquery-inputcount/master/jquery.inputcount.css
$ cd path/to/js
$ wget https://raw.github.com/miko2u/jquery-inputcount/master/jquery.inputcount.js
```

`path/to/js` および `path/to/css` は、あなたが配置したいディレクトリにおいてください。
