---
hide:
  - toc
---

### カスタム CSS の例

markdown_extensions: attr_list を有効にする。

```css
.image_center_block {
    display: block;
    margin: 0 auto; /* center */
}
```

css で指定しておくと {: .image_center_block } のように .md 内で書くと画像を中央に表示できる。

![Placeholder](https://dummyimage.com/200x100/eee/aaa){: .image_center_block }

```html
![Placeholder](https://dummyimage.com/200x100/eee/aaa){: .image_center_block }
```

画像リンクから画像を表示するには先頭に ! をつけ、 [ 名前 ] のようにする。

### 埋め込みの例

```html
<blockquote class="twitter-tweet">
	<a href="https://twitter.com/xxxxx/status/1299556784210735104"></a>
</blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
```

これを .md に直接書くと Twitter のツイートが埋め込まれる。

---

```html
<div class="video-wrapper">
  <iframe width="1280" height="720" src="https://www.youtube.com/embed/UoklxctRrsk" frameborder="0" allowfullscreen></iframe>
</div>
```

これを .md に直接書くと YouTube の動画が埋め込まれる。

<div class="video-wrapper">
  <iframe width="1280" height="720" src="https://www.youtube.com/embed/UoklxctRrsk" frameborder="0" allowfullscreen></iframe>
</div>

---

[https://jsfiddle.net](https://jsfiddle.net/) にシェーダーを保存して埋め込み機能を使う。

```html
<script async src="//jsfiddle.net/xxxxx/3e6fncud/1/embed/result/dark/"></script>
```

これを.mdに直接書くと canvas が埋め込まれる。

```html
<script async src="//jsfiddle.net/xxxxx/3e6fncud/1/embed/result,js,html/dark/"></script>
```

このように書くと Result と Javascript と Html のタブができるが
切り替えると高さが変わって小さくなって戻らないのでやめる。

---

```html
<script src="https://gist.github.com/ocornut/2aae72968154ccb7800cd40dc9be7f31.js"></script>
```

これを .md に直接書くとGistが埋め込まれる。丸ごと埋め込まれるのでとても長い Gist の場合注意。
