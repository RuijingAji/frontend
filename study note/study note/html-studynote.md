# HTML
## html 简介
## URL
**url** 统一资源定位符，定义网络位置的文本字符串
>此目录结构的根目录称为 creating-hyperlinks。建设网页时会有一个包含整个网站的目录。根目录有一个 index.html（网站主页或登录页面） 和一个 contacts.html 文件。</br>
根目录还有两个目录——pdfs 和 projects，它们分别包含一个 PDF（project-brief.pdf）文件和一个 index.html 文件。可以有两个 index.html 文件，前提是他们在不同的目录下。第二个 index.html 或许是项目相关信息的主登录界面。</br>
**指向当前目录**：如果 index.html（目录顶层的 index.html）想要包含一个超链接指向 contacts.html，你只需要指定想要链接的文件名，因为它与当前文件是在同一个目录的。所以你应该使用的 URL 是 contacts.html</br>
**指向子目录**：如果 index.html （目录顶层 index.html）想要包含一个超链接指向 projects/index.html，你需要先进入 projects 项目目录，然后指明要链接到的文件 index.html。 通过指定目录的名称+正斜杠+文件的名称。因此你要使用的 URL 是 projects/index.html</br>
**指向上级目录**：如果你想在 projects/index.html 中包含一个指向 pdfs/project-brief.pdf 的超链接，你必须先返回上级目录，然后再回到 pdf 目录。“返回上一个目录级”使用两个英文点号表示（..），所以你应该使用的 URL 是 ../pdfs/project-brief.pdf

---**文档片段**---
超链接除了可以链接到文档外，也可以链接到 HTML 文档的特定部分（被称为文档片段）
```
<h2 id="Mailing_address">邮寄地址</h2>

<p>要提供意见和建议，请将信件邮寄至<a href="contacts.html#Mailing_address">我们的地址</a>。</p>
```
---**电子邮件**---
链接到电子邮件： `<a>` 元素+ mailto:URL
```
<a href="mailto:nowhere@mozilla.org">向 nowhere 发邮件</a>
向 nowhere 发邮件
```
邮件中添加指定详细信息
cc-抄送；subject-主题；body-邮件主体，例：
```
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
><p>我们使用 <abbr title="超文本标记语言（Hyper text Markup Language）">HTML</abbr> 来组织网页文档。</p>