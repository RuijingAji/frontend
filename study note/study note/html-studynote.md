#HTML
##html 简介
## URL与path
### URL
**url** 统一资源定位符，定义网络位置的文本字符串
>此目录结构的根目录称为 creating-hyperlinks。建设网页时会有一个包含整个网站的目录。根目录有一个 index.html（网站主页或登录页面） 和一个 contacts.html 文件。</br>
根目录还有两个目录——pdfs 和 projects，它们分别包含一个 PDF（project-brief.pdf）文件和一个 index.html 文件。可以有两个 index.html 文件，前提是他们在不同的目录下。第二个 index.html 或许是项目相关信息的主登录界面。</br>
**指向当前目录**：如果 index.html（目录顶层的 index.html）想要包含一个超链接指向 contacts.html，你只需要指定想要链接的文件名，因为它与当前文件是在同一个目录的。所以你应该使用的 URL 是 contacts.html</br>
**指向子目录**：如果 index.html （目录顶层 index.html）想要包含一个超链接指向 projects/index.html，你需要先进入 projects 项目目录，然后指明要链接到的文件 index.html。 通过指定目录的名称+正斜杠+文件的名称。因此你要使用的 URL 是 projects/index.html</br>
**指向上级目录**：如果你想在 projects/index.html 中包含一个指向 pdfs/project-brief.pdf 的超链接，你必须先返回上级目录，然后再回到 pdf 目录。“返回上一个目录级”使用两个英文点号表示（..），所以你应该使用的 URL 是 ../pdfs/project-brief.pdf

--文档片段
超链接除了可以链接到文档外，也可以链接到 HTML 文档的特定部分（被称为文档片段）
```
<h2 id="Mailing_address">邮寄地址</h2>

<p>要提供意见和建议，请将信件邮寄至<a href="contacts.html#Mailing_address">我们的地址</a>。</p>