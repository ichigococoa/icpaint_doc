---
hide:
  - toc
---

<!-- ---
# markdown_extensions: meta の例
title: タイトル名を上書き
summary: 概要を上書き
date: 2021-02-26
# hide:
# - navigation # これを使えば左側の一覧を非表示にできる
# - toc # これを使えば右側の一覧を非表示にできる
--- -->

mkdocs フォルダでコマンドプロンプトを開き、 mkdocs serve を実行して、
ブラウザで http://127.0.0.1:8000/ を開いて確認する

# h1 Heading
## h2 Heading
### h3 Heading
#### h4 Heading
##### h5 Heading
###### h6 Heading

水平線(3種類の書き方(___, ---, ***))
___
---
***

### 文字の装飾

**太字 abcdef 1**

__太字 abcdef 2__

*斜体文字 abcdef 1*

_斜体文字 abcdef 2_

***斜体文字の太字 abcdef 1***

___斜体文字の太字 abcdef 2___

<u>下線 abcdef</u>

<del>取り消し線</del>

markdown_extensions: pymdownx.mark を有効にすると ==黄色のマーカー== が使える。

> Blockquotes
>
> ～ 文章 ～
>
>> 2重にする場合

### リスト

* リスト
    * リスト
    * リスト
* リスト

リストは * でも ＋ でも - でも同じリストになる。リストは上に1行空けておく必要がある

+ リスト
    + リスト
    + リスト
+ リスト

### 順序付きリスト

1. first
1. second
1. third

### テーブル

| Option | Description |
| ------ | ----------- |
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |

------:にすると右寄せになる

| Option | Description |
| ------:| -----------:|
| data   | path to data files to supply the data that will be passed into templates. |
| engine | engine to be used for processing templates. Handlebars is the default. |

First Header | Second Header | Third Header
:----------- |:-------------:| -----------:
Left         | Center        | Right
Left         | Center        | Right

### 注釈の例

markdown_extensions: footnotes を有効にする。

注釈をつけたい単語[^1]はこれ
[^1]: この行だけページの最下部に自動的に表示される。注釈機能

### リンクの例

[MkDocsのmarkdownの書き方](https://www.mkdocs.org/user-guide/writing-your-docs/#writing-with-markdown)

リンクを書く時の第2引数の文字列はマウスオーバー時に表示される

[マウスオーバーあり](https://www.mkdocs.org/user-guide/writing-your-docs/#writing-with-markdown "マウスオーバー時に表示される文字列")

.htmlのidへのリンクの例

+ [順序付きリスト](#_1)
+ [テーブル](#_2)
+ [注釈の例](#_3)

### タスクリストの例

markdown_extensions: pymdownx.tasklist を有効にする。

+ [X] item 1
    + [X] item A
    + [ ] item B
        more text
        + [x] item a
        + [ ] item b
    + [X] item C
+ [ ] item 2

### 吹き出しのようなものの例

markdown_extensions: admonition を有効にする。

!!! Note "" のように ""をつけると Noteの部分を非表示にできる

!!! Note ""
	ノートです。
	``` python
    def bubble_sort(items):
        for i in range(len(items)):
            for j in range(len(items) - 1 - i):
                if items[j] > items[j + 1]:
                    items[j], items[j + 1] = items[j + 1], items[j]
    ```
	埋め込みコードの例
!!! Note
	ノートです。
!!! Info
    Infoです。
!!! Tip
	ヒントです。
!!! Warning
	警告です
!!! Danger
	危険です。
!!! Success
	成功です。
!!! Failure
	失敗です。
!!! Bug
	バグです。
!!! summary
	概要です。
!!! help
	ヘルプです。
!!! example
	例です。
!!! quote
	引用です。
!!! Note ""
	タイトルを省略した書き方
!!! Note "カスタムタイトル"
    カスタムタイトル
??? info "開閉式(markdown_extensions: pymdownx.details を有効にする)"
	開いたら表示される。

	改行含めて自由に文章を書ける。
	??? note "Open styled details"
		??? danger "Nested details!"
			And more content again.
	??? success
		Content.
	??? warning
		Content.

### コードブロックの例

markdown_extensions: pymdownx.highlight を有効にする。
コードブロック内の色はcssで指定する。

```python
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

コードブロックに linenums="1" を入れると行数付きになる。 hl_lines="2 4" で指定する行数をハイライトにする。

```python linenums="1" hl_lines="2 4"
def bubble_sort(items):
    for i in range(len(items)):
        for j in range(len(items) - 1 - i):
            if items[j] > items[j + 1]:
                items[j], items[j + 1] = items[j + 1], items[j]
```

コードのインライン表示は `gem install hoge` のように ` を使う。
