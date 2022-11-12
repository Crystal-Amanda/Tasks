# 1️⃣HTML是什么？

HTML 是用来描述网页的一种语言
+ HTML 指的是***超文本标记语言: HyperText Markup Language***
+ HTML 不是一种编程语言，而是一种标记语言
+  标记语言是一套标记标签 (markup tag)
+ HTML 使用标记标签来描述网页
+ HTML 文档包含了HTML 标签及文本内容
+ HTML文档也叫做 web 页面
# 2️⃣HTML标签/元素
"HTML 标签" 和 "HTML 元素" 通常都是描述同样的意思.
但是严格来讲, 一个 HTML 元素包含了开始标签与结束标签



- 标签格式<sth>

  开始标签<sth> 结束标签</sth>

- div标签

  - div 标签定义 HTML 文档中的一个分隔区块或者一个区域部分。

  ​      div标签常用于组合块级元素，以便通过 CSS 来对这些元素         进行格式化。

  - 例（div可以嵌套，在div里的命令到div截至）

  - <div style="color:#0000FF">
      <h3>这是一个在 div 元素中的标题。</h3>
      <p>这是一个在 div 元素中的文本。</p>
    </div>

- table标签

  - table声明<table border="1">

  - 行 用了几个tr就几行

  - 列 tr里面的数字按列排放，标签为td

  - 例子

  - <table border="1">
    <tr>
      <td>100</td>
      <td>200</td>
      <td>300</td>
    </tr>
    <tr>
      <td>400</td>
      <td>500</td>
      <td>600</td>
    </tr>
    </table>

    

- 列表
  - 有序列表用ul
  - 无序列表用ol
  - 里面元素用li

+ **<button>标签**

  - 作用：按钮

  - <button type="button" onclick="alert('你好，世界!')>点我！</button>

  - onclick>出现嵌入式页面

    ------

    ***标签***

  - 标题<h1>XXXXXX</h1>(h1->h6)

  - 段落<p>XXXXX</p>

  - 链接<a  属性（href/target）="链接">+文字解释 </a>

    - target在新窗口打开：href="url" **target="-blank"**

  - 图像

    - 格式：<img src="url" alt="Pulpit rock" width="304" height="228">
    - src(源属性) url(图像位置)
    - Alt属性用来为图像定义一串预备的可替换的文本；替换文本属性的值是用户定义的
    - 设置高度与宽度

    

补充：br换行 b/strong粗体 i/em斜体 big/small放大缩小 sup上标 sub下标

# 3️⃣区块元素和内联元素

- 块级元素 以新行开始 h1,p,ul,ol,table
  - div 如果与 CSS 一同使用，<div> 元素可用于对***大的内容***块设置样式属性。
- 内联元素 不以新行开始 b,i,td,a,img
  - span 当与 CSS 一同使用时，<span> 元素可用于为***部分文本***设置样式属性。
- div和span应用：style="color:#0000FF;font-weight：bold"
- 各类标签的块级内联
  - ul，ol--->li
  - table--->tr,td

# 4️⃣HTML元素

元素的内容是开始标签与结束标签之间的内容

- head元素包含了所有的头部标签元素。 可以添加在头部区域的元素标签为: <title>, <style>, <meta>, <link>, <script>, <noscript> 和 <base>。    

- title定义不同文档的标题

- base标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接

- link标签标签定义了文档与外部资源之间的关系。

  <link> 标签通常用于链接到样式表:

  - <link rel="stylesheet" type="text/css" href="mystyle.css">

- <body> 元素定义了 HTML 文档的主体

- <html> 元素定义了整个 HTML 文档

- style标签定义了HTML文档的样式文件引用地址.

  在<style> 元素中你也可以直接添加样式来渲染 HTML 文档:

- meta标签描述了一些基本的元数据。

  <meta> 标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。
  META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。

- <script>标签用于加载脚本文件，如： JavaScript。

# 6️⃣HTML文本格式

起始行-------><!DOCTYPE html>

开始标签-----><html>

结束标签------></html>

