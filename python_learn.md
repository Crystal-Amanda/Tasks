# python学习
## python——“内置电池”
Python就为我们提供了非常完善的基础代码库，覆盖了网络、文件、GUI、数据库、文本等大量内容，被形象地称作“内置电池（batteries included）”。用Python开发，许多功能不必从零编写，直接使用现成的即可。

除了内置的库外，Python还有大量的第三方库，也就是别人开发的，供你直接使用的东西。当然，如果你开发的代码通过很好的封装，也可以作为第三方库给别人使用。
## Frist python
### vscode如何运行python代码
> 只有重新将新建文件保存为以 .py 为后缀名的文件，VS Code 才能够识别出来是 Python 文件，后期在此文件中编写 Python 代码时，才能高亮显示。

在vscode中运行前需要下载python的应用，不止要有python的扩展，这样就可以正常运行啦！

参考 [vscode如何运行python代码](http://c.biancheng.net/view/5827.html)
### VSCode Python DEBUG 调试
根据上述步骤，输出结果除了运行结果，还有代码执行过程中产生的信息。
第一步 创建launch.json
> 点击左侧栏的小甲虫+三角形图标（运行和调试）

![](https://raw.githubusercontent.com/Crystal-Amanda/Tasks/main/debug1.png)
这个launch只有在py文件里点击下面这个才有（我也不确定 但我纯文本的时候没有出现新建launch.json）
![](https://raw.githubusercontent.com/Crystal-Amanda/Tasks/main/debug2.png)
> 新建json后就是选定打开py文件，是python current flie，然后我打开我的py，就可以了

![](https://raw.githubusercontent.com/Crystal-Amanda/Tasks/main/debug3.png)
参考 [VSCode Python DEBUG 调试](https://blog.csdn.net/pandoraliu/article/details/124620656#:~:text=VSCode%20Debug%201%20Single%20file%20debug%20-%3E%20%E9%80%89%E6%8B%A9,Python%20%E6%96%87%E4%BB%B6%E2%80%9D%20%E5%B0%B1%E4%BC%9A%E7%94%9F%E6%88%90%E4%B8%80%E4%B8%AA%20Launch.json%20%E7%9A%84%E6%96%87%E4%BB%B6%20%E5%9C%A8%20.vscode%20%E7%9A%84%E6%96%87%E4%BB%B6%E5%A4%B9%E4%B8%8B)
这个教程里有断点Breakpoint，没搞懂
参考 [vscode：代码断点调试](https://blog.csdn.net/weixin_43972437/article/details/123280471)
### format Debug
> 命令面板搜索format Debug ，会显示未安装，安装就好。为了使用方便，在setting设置里搜索formatOnSave 打开权限后，写代码时点击保存键就可以直接格式化。
# 🛒python基本语法
## 1️⃣python 字符串
> 对于**单个字符**的编码，Python提供了ord()函数获取字符的整数表示，chr()函数把编码转换为对应的字符

![](https://raw.githubusercontent.com/Crystal-Amanda/Tasks/main/py2.png)
> 以Unicode表示的str通过encode()方法可以编码为指定的bytes

> 要把bytes变为str，就需要用decode()方法

#### len()函数

![](https://raw.githubusercontent.com/Crystal-Amanda/Tasks/main/py3.png)
### 格式化
| 占位符 | 替换内容   |
| ------ | ---------- |
| %d     | 整数       |
| %f     | 浮点数     |
| %s     | 字符串     |
| %x     | 十六进制数 |
> 如果你不太确定应该用什么，%s永远起作用，它会把任何数据类型转换为字符串

>字符串里面的%是一个普通字符怎么办？这个时候就需要转义，用%%来表示一个%

> 另一种格式化字符串的方法是使用字符串的format()方法，它会用传入的参数依次替换字符串内的占位符{0}、{1}……，不过这种方式写起来比%要麻烦得多

![](https://raw.githubusercontent.com/Crystal-Amanda/Tasks/main/5.png)
> 最后一种格式化字符串的方法是使用以f开头的字符串，称之为f-string，它和普通字符串不同之处在于，字符串如果包含{xxx}，就会以对应的变量替换

![](https://raw.githubusercontent.com/Crystal-Amanda/Tasks/main/py6.png)
## 2️⃣数据类型和变量
### 整数
### 浮点数
### 字符串
> 用'或"括起来 ，但是当打印I'm fine.时出现'如何处理，用**转义字符** \'就可以
> **转义字符\可以转义很多字符**，比如\n表示换行，\t表示制表符，字符\本身也要转义，所以\\表示的字符就是\，可以在Python的交互式命令行用print()打印字符串;Python还允许用**r''表示''内部的字符串默认不转义**
> 如果字符串内部有很多换行，用\n写在一行里不好阅读，为了简化，***Python允许用'''...'''的格式表示多行内容***(在交互式行输入，.py文件不用...)

![](https://raw.githubusercontent.com/Crystal-Amanda/Tasks/main/py7.png)
> 多行字符串'''...'''还可以在前面加上r使用
### 布尔值
我的理解也就是判断表达式的对错，对是Ture，错就是False
还可以用and、or、not运算
### 空值none
### 除法
/计算结果浮点数
//计算结果整数 10//3=3
%取余数
### 常量
> 在Python中，通常用全部大写的变量名表示常量
## 3️⃣list
list相当于数组，但是它里面的元素类型可以是多种数据类型，元素也可以是另一个list(此时就像是个二维数组)。
格式：**classmates = ['Michael', 'Bob', 'Tracy']**
list的元素个数可以用len()计算得到。
> 000.insert(数字，元素)是指把元素插入到指定位置
000.pop()是指删除list末尾元素；000.pop(数字)删除指定位置
000.append()在末尾加入元素
## 4️⃣tuple
tuple 也是Python的有序集合只是定义了就不能改变。
格式：**a = ()
    b = (1,)
    c = (4,5,6)
    t = (1, 'a', ["A", "B"])**
第四个例子中其中一个元素是list，意味着可以改变list里的元素
## 5️⃣条件判断
if 000:
elif 000:
else：
## 6️⃣循环
### for in
L = ['Bart', 'Lisa', 'Adam']
for l in L:
    print(**f**'Hello,**{l}**!')
### while
while 条件：
000
> **break**提前结束循环
> **continue**跳过这次循环进行下一次循环
# 🛒函数
## 1️⃣调用函数
abs() 绝对值函数
max() 求最大值
数据类型转换 int()
## 2️⃣定义函数
> 格式: def my_date(x):
>      00000000000

## 3️⃣函数参数
### 可变参数
如果在定义函数时我们的参数并不确定，我们可以定义一个list或tuple来实现
> def clac(numbers):
> 00000
> clac([1,2,3,4])

这种方法在我们已经有了一个list时写起来就比较麻烦
> nums = [1,2,3]
> clac([nums[0], nums[1], nums[2]])

这时候我们就可以用我们的**可变函数**
定义可变参数和定义一个list或tuple参数相比，仅仅在参数前面加了一个*号。在函数内部，参数numbers接收到的是一个tuple，因此，函数代码完全不变。但是，调用该函数时，可以传入任意个参数，包括0个参数
> def clac(*numbers):
00000
clac(1,2,3,4)
nums = [1,2,3]
clac(*nums)

为什么nums可以直接把元素传进去呢？
Python允许你在list或tuple前面加一个*号，把list或tuple的元素变成可变参数传进去
# 🛒面向对象编程
面向对象的程序设计把计算机程序视为一组对象的集合，而每个对象都可以接收其他对象发过来的消息，并处理这些消息，计算机程序的执行就是一系列消息在各个对象之间传递。
假设我们要处理学生的成绩表，为了表示一个学生的成绩，面向过程的程序可以用一个dict表示：
> std1 = {'name':'Tom','score':98}

如果打印出来可以定义一个函数
> def print_std():
> print("%s:%s" %(std['name'],std['score']))

如果采用面向对象的程序设计思想，我们首选思考的不是程序的执行流程，而是Student这种数据类型应该被视为一个对象，这个对象拥有name和score这两个属性（Property）。如果要打印一个学生的成绩，首先必须创建出这个学生对应的对象，然后，给对象发一个print_score消息，让对象自己把自己的数据打印出来。
> class Student(object):

    def __init__(self, name, score):
        self.name = name
        self.score = score

    def print_score(self):
        print('%s: %s' % (self.name, self.score))

> bart = Student('Bart Simpson', 59)
lisa = Student('Lisa Simpson', 87)
bart.print_score()
lisa.print_score()
## 1️⃣类和实例
类是抽象的模板，比如Student类，而实例是根据类创建出来的一个个具体的“对象”，每个对象都拥有相同的方法，但各自的数据可能不同。
**类**创建的时候需要class关键字，类首字母大写后面还跟着(object)，一般都是object。
**实例**就是类的主要承载的，bart = Student()
我们可以在创建类的时候，通过_init_这个方法把实例必须绑定的属性强制绑定，当然我们也可以自由绑定
**数据封装**是类具有数据，无需从外面的函数访问，在创建类时就定义函数。
get_grade()
> class Student(object):
    ...

    def get_grade(self):
        if self.score >= 90:
            return 'A'
        elif self.score >= 60:
            return 'B'
        else:
            return 'C'
可以直接在实例里使用
# 🛒爬虫
 爬虫能做些什么
> 抓取互联网上的数据，为我所用。

 什么是爬虫
 > 通过编写程序，模拟浏览器上网，然后让其去互联网上抓取数据的过程

爬虫在使用场景的分类
> 通用爬虫：抓取系统的重要组成部分，抓取的是一整张页面的数。
> 聚焦爬虫：是建立在通用爬虫的基础上，抓取的是页面中特定的局部内容。
> 增量式爬虫：检测网站中数据更新的情况，只会抓取网站中最新更新出来的数据。

## request模块
[Requests: 让 HTTP 服务人类](https://cn.python-requests.org/zh_CN/latest/)
> request的作用：发送HTTP请求，获得响应数据

