# HTML
## html 简介
1.不是编程语言
2.是超文本标记语言，告知浏览器如何组织页面
3.页面由一系列**元素**（elements）组成，元素包围不同内容，使其按照某种方式呈现。元素需要正确的打开和关闭，即关注正确的嵌套关系。
***注意:***  虽浏览器不区分大小写，但为了可读性，应使用小写字母。
4.为了使网页代码便于他人理解，可采用`<!--说明说明说明-->`形式为关键部分添加说明
5.为了可读性，要坚持自己的网页编写风格，风格体现在代码的缩进等方面。

## html 元素
`<em></em>` 斜体 补充：`<i>`元素
`<strong></strong>`加粗强调 补充：` <b> `元素 
`<img src="">` 插入图片 （部分元素没有关闭的标签，通常用来在此元素所在位置插入/嵌入一些东西。）称为空元素 （Empty elements/ void elements）
`<a></a> `超链接
`<imput>`输入 
**元素的属性**
属性可以为元素添加额外信息，其构成：
元素名称和属性间加一个空格+属性=+“属性值”（双引号不要省略），以`<a>`为例
href="" 链接地址
title="" 链接的名称
target="_blank" 表明在当前页面不显示超链接地址
```
<a href="" title="" target="">滴滴</a>
```
<a href="" title="什么是滴滴" target="_blank">滴滴</a>

<!-- 学名 -->
<p>
  红喉北蜂鸟（学名：<i>Archilocus colubris</i>）是北美东部最常见的蜂鸟品种。
</p>

<!-- 舶来词 -->
<p>
  菜单上有好多舶来词汇，比如 <i lang="uk-latn">vatrushka</i>（东欧乳酪面包）,
  <i lang="id">nasi goreng</i>（印尼炒饭）以及<i lang="fr">soupe à l'oignon</i>（法式洋葱汤）。
</p>

<!-- 已知的错误书写 -->
<p>
  总有一天我会改掉写<u style="text-decoration-line: underline; text-decoration-style: wavy;">措字</u>的毛病。
</p>

<!-- 在一组指令中突出显示关键字 -->
<ol>
  <li>
    <b>切</b>下两片面包，
  </li>
  <li>
    在两片面包中间<b>夹入</b>一片西红柿和一片生菜叶。
  </li>
</ol>

再例`<imput>` disabled 属性-布尔属性，可以使输入标签不可用
```
<input type="text">
<input type="text" disabled>
```
<input type="text">
<input type="text" disabled>

## html 结构
1.页面声明：`<!DOCTYPE html>`
2.文档主语言：`<html lang="zh-CN">`，设置主语言有利于网页被搜索引擎有效索引。
>补充：可以将文档的分段设置为不同的语言
```
<p>Japanese example: <span lang="ja">ご飯が熱い。</span></p>
```
2.页面根元素：`<html></html>`,包裹完整页面
3.需包含但不想显示在页面上的内容：`<head></head>`
4.网页主体内容：`<body></body>`
### 结构1-head
作用：保存页面的元数据
1.`<title>` 网页标题，元数据，该网页在收藏栏里显示的名字
2.`<meta charset="utf-8">` 字符编码
3.`<meta name="author(页面作者)" content="TY">`
`<meta name="description（页面的简要描述）" content="">` 可用于搜索引擎优化
4.网页自定义图标favicon，在浏览器的收藏夹或书签列表）中显示
将该图片保存在网页文件夹里，格式：（1）.ico（最通用格式）（2）.png (3).jpg
```
<link rel="icon" href="favicon.ico" type="image/x-icon">
```

## 在 HTML 中应用 CSS 和 JavaScript
css `<link>`
```
<link rel="stylesheet" href="my-css-file.css">
```
javascript `<script>`,没必要非要放在文档的` <head>` 中,最好加上 defer 以告诉浏览器在解析完成 HTML 后再加载 JavaScript
```
<script src="my-js-file.js" defer></script>
```


## html 特殊字符转义 
用的时候再搜吧，现在完全记不住

## URL
**url** 统一资源定位符，定义网络位置的文本字符串
>此目录结构的根目录称为 creating-hyperlinks。建设网页时会有一个包含整个网站的目录。根目录有一个 index.html（网站主页或登录页面） 和一个 contacts.html 文件。</br>
根目录还有两个目录——pdfs 和 projects，它们分别包含一个 PDF（project-brief.pdf）文件和一个 index.html 文件。可以有两个 index.html 文件，前提是他们在不同的目录下。第二个 index.html 或许是项目相关信息的主登录界面。</br>
**指向当前目录**：如果 index.html（目录顶层的 index.html）想要包含一个超链接指向 contacts.html，你只需要指定想要链接的文件名，因为它与当前文件是在同一个目录的。所以你应该使用的 URL 是 contacts.html</br>
**指向子目录**：如果 index.html （目录顶层 index.html）想要包含一个超链接指向 projects/index.html，你需要先进入 projects 项目目录，然后指明要链接到的文件 index.html。 通过指定目录的名称+正斜杠+文件的名称。因此你要使用的 URL 是 projects/index.html</br>
**指向上级目录**：如果你想在 projects/index.html 中包含一个指向 pdfs/project-brief.pdf 的超链接，你必须先返回上级目录，然后再回到 pdf 目录。“返回上一个目录级”使用两个英文点号表示（..），所以你应该使用的 URL 是 ../pdfs/project-brief.pdf

---**文档片段**---
超链接除了可以链接到文档外，也可以链接到 HTML 文档的特定部分（被称为文档片段）
```html
<h2 id="Mailing_address">邮寄地址</h2>

<p>要提供意见和建议，请将信件邮寄至<a href="contacts.html#Mailing_address">我们的地址</a>。</p>
```
---**电子邮件**---
1)链接到电子邮件： `<a>` 元素+ mailto:URL
```html
<a href="mailto:nowhere@mozilla.org">向 nowhere 发邮件</a>
向 nowhere 发邮件
```
2)邮件中添加指定详细信息
cc-抄送；subject-主题；body-邮件主体，例：
```html
<a href="mailto:nowhere@mozilla.org?
cc=name2@rapidtables.com&
bcc=name3@rapidtables.com&subject=The%20subject%20of%20the%20email&body=The%20body%20of%20the%20email">
  Send mail with cc, bcc, subject and body
</a>
```
**备注:**  每个字段的值必须是使用 URL 编码的，即使用百分号转义的非打印字符（不可见字符比如制表符、换行符、分页符）和空格。同时注意使用问号（?）来分隔主 URL 与参数值，以及使用 & 符来分隔 mailto: URL 中的各个参数。 这是标准的 URL 查询标记方法。阅读 GET 方法以了解哪种 URL 查询标记方法是更常用的。

## 高阶文字排版
**描述列表 description list`<dl></dl>`**
被描述的术语 ` <dt></dt>`
用来描述的语言 `<dd></dd>` 会缩进哈
><dl>
<dt>培根</dt>
<dd>整个世界的粘合剂。</dd>
<dt>鸡蛋</dt>
<dd>一块蛋糕的粘合剂。</dd>
<dt>咖啡</dt>
<dd>一种浅棕色的饮料。</dd>
<dd>可以在清晨带来活力。</dd>`
</dl>


**引用 完全没有看懂**
相应学习内容：https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting

**缩略语**
元素`<abbr>` 用来包裹一个缩略语或缩写，并用title提供缩写的解释，例：
```html
><p>我们使用 <abbr title="超文本标记语言（Hyper text Markup Language）">HTML</abbr> 来组织网页文档。</p>
```
**标记联系方式**
元素`<address>`用来标记联系方式，但通常只用来标记该网页编写者的联系方式
```html
<address>
  <p>Page written by <a href="../authors/chris-mills/">Chris Mills</a>.</p>
</address>
```
**上标和下标**
日期、化学方程式、数学方程式上下标
`<sub>`下标，化学配平
`<sup>` 上标，平方
```html
<p>C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub></p>
<p>如果X<sup>2</sup>的值是9，那么x的值必为-3或3</p>
```
<p>C<sub>8</sub>H<sub>10</sub>N<sub>4</sub>O<sub>2</sub></p>
<p>如果X<sup>2</sup>的值是9，那么x的值必为-3或3</p>

**展示计算机代码 记不住**
相应学习内容：https://developer.mozilla.org/zh-CN/docs/Learn/HTML/Introduction_to_HTML/Advanced_text_formatting

**标记时间和日期 记不住**
元素 `<time datetime="2016-01-20">2016年1月20日</time>`
```
<!-- 标准简单日期 -->
<time datetime="2016-01-20">20 January 2016</time>
<!-- 只包含年份和月份-->
<time datetime="2016-01">January 2016</time>
<!-- 只包含月份和日期 -->
<time datetime="01-20">20 January</time>
<!-- 只包含时间，小时和分钟数 -->
<time datetime="19:30">19:30</time>
<!-- 还可包含秒和毫秒 -->
<time datetime="19:30:01.856">19:30:01.856</time>
<!-- 日期和时间 -->
<time datetime="2016-01-20T19:30">7.30pm, 20 January 2016</time>
<!-- 含有时区偏移值的日期时间 -->
<time datetime="2016-01-20T19:30+01:00">7.30pm, 20 January 2016 is 8.30pm in France</time>
<!-- 调用特定的周 -->
<time datetime="2016-W04">The fourth week of 2016</time>
```
## 网页基本结构（文档与网站架构）
**页面的基本组成部分**
1.页眉 `<header>`
2.导航栏 `<nav>`
3.主内容 `<main>`,其中可以有各种子内容区段，可用`<article>、<section>、<div> `等元素表示。
4.侧边栏`<aside>`：常嵌套在 `<main>` 中
5.页脚`<footer>`
**页面布局细节**
1.`<main> `存放每个页面独有的内容。每个页面上只能用一次 `<main>`，且直接位于 `<body>` 中，不要把它嵌套进其它元素。
2.`<article>` 包围的内容即一篇文章，与页面其它部分无关。`<section> `与` <article> `类似，但 `<section> `更适用于组织页面使其按功能分块。
3.`<aside>` 包含一些间接信息（术语条目、作者简介、相关链接等等）。
4.`<header>` 是简介形式的内容。如果它是 `<body> `的子元素，表示网站的全局页眉。如果它是` <article>` 或`<section>` 的子元素，表示这些部分特有的页眉。
5.`<nav> `包含页面主导航功能,不应包含二级链接内容。
6.`<footer>` 包含页面的页脚部分。

