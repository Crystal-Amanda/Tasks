# 1️⃣CSS的作用

- CSS 指层叠样式表 (Cascading Style Sheets)

- 样式表定义如何显示 HTML 元素，就像 HTML 中的字体标签和颜色属性所起的作用那样。样式通常保存在外部的 .css 文件中。我们只需要编辑一个简单的 CSS 文档就可以改变所有页面的布局和外观。

# 2️⃣CSS选择器

**id选择器**

- 格式：

- <style>
  #para1
  {
  	text-align:center;
  	color:red;
  } 
  </style>

- <p id="para1">Hello World!</p>

  /* 定义和应用于文本*/

**class选择器**

- 格式

- <style>
  .center {
  	text-align:center;
  }
  .color {
  	color:#ff0000;
  }
  </style>

<h1 class="center">标题居中</h1>
<p class="center color">段落居中，颜色为红色。</p>

***都先在style里定义***

# 3️⃣CSS语法

1.**格式：**p {属性：值；属性：值；}

2.**CSS颜色**

- 十六进制颜色：#000000

- RGB颜色:rgb(0,0,0)

- RGBA颜色:rgba(0,0,0,0)（***0.0<a<1.0***）

- HSL色彩：hsl（0-360，0%，0%）

  - 色相是在色轮上的程度（从0到360）-0（或360）是红色的，120是绿色的，240是蓝色的。饱和度是一个百分比值;0％意味着灰色和100％的阴影，是全彩。亮度也是一个百分点;0％是黑色的，100％是白色的。

- HSLA颜色:hsla(120,65%,75%,0.3)

  - HSLA（色调，饱和度，亮度，α），α是Alpha参数定义的不透明度。 ***Alpha参数是一个介于0.0（完全透明）和1.0（完全不透明）之间的参数。***

- 预定义/跨浏览器的颜色名称

- 使用格式：p

  ​                    {

  ​                           color:rag(225,0,0)

  ​                     }

  ​                 ***应用于文本段落***

3.**字体**

- 字型：serif sans-serif monospase

- 大小：font-size：40px/em

  ​      px/16=em

4.**文本**

- **文本对齐方式**
  - 格式：{text-align：center（**居中**）/right/justify（每一行被展开         为宽度相等，左，右外边距是对齐（如杂志和报纸））；}

- **文本修饰**
  - h1 {text-decoration:overline;}上划线
    h2 {text-decoration:line-through;}划线
    h3 {text-decoration:underline;}下划线

5.**列表**

- 无序
  - ul.a {list-style-type:circle;}
    ul.b {list-style-type:square;}

- 有序
  - ol.c {list-style-type:upper-roman;}
    ol.d {list-style-type:lower-alpha;}

# 4️⃣CSS盒模型

- 不同部分的说明
  - Margin(外边距) - 清除边框外的区域，外边距是透明的。
  - Border(边框) - 围绕在内边距和内容外的边框。
  - Padding(内边距) - 清除内容周围的区域，内边距是透明的。
  - Content(内容) - 盒子的内容，显示文本和图像。

- 在style里加div声明背景颜色，宽度，外边距，边框，内边距
- body里直接使用div

# 5️⃣CSS Postion

- **static定位**：HTML 元素的默认值，即没有定位，遵循正常的文档流对象。

- **fixed定位**：元素的位置相对于浏览器窗口是固定位置。

  即使窗口是滚动的它也不会移动：

  - 注意： Fixed 定位在 IE7 和 IE8 下需要描述 !DOCTYPE 才能支持。

    Fixed定位使元素的位置与文档流无关，因此不占据空间。

    Fixed定位的元素和其他元素重叠。

  - 例子

  - p.pos_fixed
    {
    	position:fixed;
    	top:30px;
    	right:5px;
    }

  - <p class="pos_fixed">Some more text</p>

- **relative 定位**
  - h2.pos_left
    {
        position:relative;
        **left:-20px;**
    }
  - left 负值向左移动   正值向右移动
  - top 负值向上移动 正值向下移动

​          

- **absolute定位**
  - 用绝对定位,一个元素可以放在页面上的任何位置。
  - position:absolute;
    	left:100px;
    	top:150px;

- **sticky定位**

  - sticky 英文字面意思是粘，粘贴，所以可以把它称之为粘性定位。

    **position: sticky;** 基于用户的滚动位置来定位。

    粘性定位的元素是依赖于用户的滚动，在 **position:relative** 与 **position:fixed** 定位之间切换。

    它的行为就像 **position:relative;** 而当页面滚动超出目标区域时，它的表现就像 **position:fixed;**，它会固定在目标位置。

    元素定位表现为在跨越特定阈值前为相对定位，之后为固定定位。

    这个特定阈值指的是 top, right, bottom 或 left 之一，换言之，指定 top, right, bottom 或 left 四个阈值其中之一，才可使粘性定位生效。否则其行为与相对定位相同。

- **定位的选择器都是class**

# 6️⃣CSS网页布局

- **头部区域head**

  - body {
      margin: 0;
    }

    /* 头部样式 */
    .header {
      background-color: #f1f1f1;
      padding: 20px;
      text-align: center;
    }、

  - div标签+class选择器

- 菜单导航区域

  - 导航条

     . topnav {

    overflow: hidden;

    background-color:#333;

    ​         }

  - 导航链接

    .topnav a {
      float: left;
      display: block;
      color: #f2f2f2;
      text-align: center;
      padding: 14px 16px;
      text-decoration: none;
    }

  - 链接-修改颜色

    .topnav a:hover {
      background-color: #ddd;
      color: black;
    }

  - body标签

    <div class="topnav">
      <a href="#">链接</a>
      <a href="#">链接</a>
      <a href="#">链接</a>
    </div>
  
- 内容区域

  - 创建相等列

    。

    .column{

    float:left;

    width:33.33%;

    }

  - 列后清除浮动

    .row:after {
      content: "";
      display: table;
      clear: both;
    }

  - 响应式布局 - 小于 600 px 时改为上下布局

    @media screen and (max-width: 600px) {
      .column {
        width: 100%;
      }
    }

  - 显示

    <div class="row">
      <div class="column">
        <h2>第一列</h2>
        <p>菜鸟教程 - 学的不仅是技术，更是梦想！菜鸟教程 - 学的不仅是技术，更是梦想！菜鸟教程 - 学的不仅是技术，更是梦想！菜鸟教程 - 学的不仅是技术，更是梦想！</p>
        </div>

  - row声明一次就行

  - column有几列声明几列

  - **不相等的列**

    .column {
      float: left;
      padding: 10px;
    }

    /* 左右两侧宽度 */
    .column.side {
      width: 25%;
    }

    /* 中间区域宽度 */
    .column.middle {
      width: 50%;
    }

- **响应式页面布局**

  - 文章卡片效果

    - .card {
        background-color: white;
        padding: 20px;
        margin-top: 20px;
      }

  - 图像部分

    - .fakeimg {
        background-color: #aaa;
        width: 100%;
        padding: 20px;
      }

  - 应用显示

    - <div class="row">
        <div class="leftcolumn">
          <div class="card">
            <h2>文章标题</h2>
            <h5>2019 年 4 月 17日</h5>
            <div class="fakeimg" style="height:200px;">图片</div>
            <p>一些文本...</p>
            <p>菜鸟教程 - 学的不仅是技术，更是梦想！菜鸟教程 - 学的不仅是技术，更是梦想！菜鸟教程 - 学的不仅是技术，更是梦想！菜鸟教程 - 学的不仅是技术，更是梦想！</p>
          </div>

- **底部区域**

  - .footer {
      background-color: #f1f1f1;
      padding: 10px;
      text-align: center;
    }

  

# 7️⃣CSS伪类

- anchor伪类

  - a:link {color:#000000;}      /* 未访问链接*/*
  - a:visited {color:#00FF00;}  /* 已访问链接 */*
  - *a:hover {color:#FF00FF;}  /* 鼠标移动到链接上 */
  - a:active {color:#0000FF;}  /* 鼠标点击时 */

- first-child

  - p:first-child
    {
    	color:blue;
    }**一段蓝色渲染**
  - p > i:first-child
    {
    	color:blue;
    }**一个蓝色渲染+斜体

- lang伪类

  - q:lang(no)
    {
    	quotes: "~" "~";
    }

  - <p>Some text <q lang="no">A quote in a paragraph</q> Some text.</p>

  - 在这个例子中,:lang定义了q元素的值为lang =“no”
