#MD 学习笔记
##简介 二级标题
中文网页需要使用 <br> 声明编码，否则会出现乱码。
中文网页需要使用 <meta charset="utf-8"> 声明编码，否则会出现乱码。
即使 <br> 目前在所有浏览器中都是有效的，但为了获得更长远的保障，w3cschool 建议使用 <br />进行换行。
这个东西 **真的** 很难用哎
是吗？*为什么*你这么觉着呢
***就是说***，我也不知道啊
那我们来试试 ***引用*** 吧
> 即使 <br> 目前在所有浏览器中都是有效的，但为了获得更长远的保障，w3cschool 建议使用 <br />进行换行。

**没有用！**
现在问题是什么？
1. 我要做html的笔记，但有些语法和md的一样
2. 如何才能让它呈现而不是解读呢
8. 骗子！不是说可以不用按顺序的吗---原来要加空格
1. a !这并不是结构化列表！---加了空格就是列表啦
4. 新问题是怎么变成二级列表
   1. 这就是二级列表
   2. 只要手动给他缩进去？
4. 然后再手动戳出来   

+ 这依然是个列表，只是没有序号
    这样就不是列表了（缩进去四个空格）
    >加个引用呢
- 试试减号，哇也可以
>> 
        <html>
          <head>
            <title>Test</title>
          </head>
***请注意，后面学习一下怎么插入图片***
如果要表示其为代码，需要加反引号,试试吧 `title`
>如果你要表示为代码的单词或短语中包含一个或多个反引号，则可以通过将单词或短语包裹在双反引号
``Use `code` in your Markdown file.``

缩进四个空格，创建代码块

    <html>
      <head>
      </head>
    </html>

要创建分隔线，请在单独一行上使用三个或多个星号 (***)、破折号 (---) 或下划线 (___) ，并且不能包含其他内容。为了兼容性，请在分隔线的前后均添加空白行。

是

***

吗？

是

___   

不是啊

---

果然是啊

这是一个链接[葵花宝典](https://baike.baidu.com/item/%E8%91%B5%E8%8A%B1%E5%AE%9D%E5%85%B8/69672 "最好的葵花宝典")

超链接Markdown语法代码：[超链接显示名](超链接地址 "超链接title")
对应的HTML代码：<a href="超链接地址" title="超链接title">超链接显示名</a>

使用尖括号可以很方便地把URL或者email地址变成可点击的链接。
<794098319@qq.com>

##带格式的链接
I love supporting the **[EFF](https://eff.org)**.
This is the *[Markdown Guide](https://www.markdownguide.org)*.
See the section on [`code`](#code).

##链接语法没看懂，用时再说吧
/# 反斜杠字符转意
我&你  我&amp你
>现在是块级元素吗
就是说>还是>啊

This is a regular paragraph.

<table>
    <tr>
        <td>Foo</td>
    </tr>
</table>

This is another regular paragraph.