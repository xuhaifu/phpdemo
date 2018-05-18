Makedown语法
---

Markdown 的目标是实现「易读易写」。

###### 1.兼容 HTML
不在 Markdown 涵盖范围之内的标签，都可以直接在文档里面用 HTML 撰写。不需要额外标注这是 HTML 或是 Markdown；只要直接加标签就可以了。

要制约的只有一些 HTML 区块元素比如``<div>``、``<table>``、``<pre>``、``<p>``等标签，必须在前后加上空行与其它内容区隔开，还要求它们的开始标签与结尾标签不能用制表符或空格来缩进。Markdown 的生成器有足够智能，不会在 HTML 区块标签外加上不必要的``<p>``标签。

HTML的区段（行内）标签如``<span>``、``<cite>``、``<del>``可以在Markdown的段落、列表或是标题里随意使用。依照个人习惯，甚至可以不用Markdown格式，而直接采用HTML标签来格式化。举例说明：如果比较喜欢HTML的<a>或<img>标签，可以直接使用这些标签，而不用Markdown提供的链接或是图像标签语法。

和处在 HTML 区块标签间不同，Markdown 语法在 HTML 区段标签间是有效的。
###### 2.MarkDown基本语法
1）标题

标题是每篇文章都需要也是最常用的格式，在 Markdown 中，如果一段文字被定义为标题，只要在这段文字前加 # 号即可。
```
# 一级标题     //对应html标签<h1>
## 二级标题   //对应html标签<h2>
### 三级标题 //对应html标签<h3>
```
以此类推，总共六级标题，建议在井号后加一个空格，这是最标准的 Markdown 语法。

这里要注意的是#和后面的内容之间要有空格隔开。

2）粗体和斜体

Markdown 使用星号（*）和底线（_）作为标记强调字词的符号，被 * 或 _ 包围的字词会被转成用 <em> 标签包围，用两个 * 或 _ 包起来的话，则会被转成 ```<strong>```

```
*single asterisks* 斜体

_single underscores_ 斜体

**double asterisks** 粗体

__double underscores__ 粗体
```

3）分割线
分割线也比较简单，markdown语法为：

`---`
或者
`***`

4）列表

这里的列表指的就是我们html中常用的有序列表和无序列表，及``<ul>``和``<ol>``.这里不再给出截图，大家可以自己动手实践。

其语法如下：

无序列表：

```
* 1  或者 - 1  或者 + 1 

* 2  或者 - 2  或者 + 2 

* 3  或者 - 3  或者 + 3 
```

这里要注意的是有使用*就都是用*号，使用 '-' 就都用 '-' 号，混合使用会出错的。还有就是* 和内容之间要加一个空格。

有序列表比较简单，写法如下：
```
1. Item1

2. Item2

3. Item3
```
 当然，这里前面的序号可以随便写，总之后面会得到与之相同的输出。

5）引用

如果你需要引用一小段别处的句子，那么就要用引用的格式。引用的语法就是在文字前面加 > ,如：
```
> 这里是引用
```

当然，不同的markdown编辑器输出的显示略有不同.

6）超链接

超链接的写法比较特殊，但是也很好记忆，如我们加一个百度的超链接，markdown语法如下：
```
[百度](http://www.baidu.com)
```
当我们导出到html中时，就会得到一个<a>标签的输出。

链接内容定义的形式为：

    方括号（前面可以选择性地加上至多三个空格来缩进），里面输入链接文字
    接着一个冒号
    接着一个以上的空格或制表符
    接着链接的网址
    选择性地接着 title 内容，可以用单引号、双引号或是括弧包着

7）表格

markdown的表格我感觉写起来并不是那么简便，我们先来看一下表格的写法：

```
| Tables        | Are           | Cool  |
| ------------- |:-------------:| -----:|
| col 3 is      | right-aligned | $1600 |
| col 2 is      | centered      |   $12 |
| zebra stripes | are neat      |    $1 |
```
这里值得注意的是第二行，|:------------:|,这里两边加冒号就是居中，如果只有一边加冒号就是哪边对齐，如Cool那一列就是右对齐。默认左对齐。

 8）代码框

 程序员写东西，难免会插入一些代码，在 Markdown下实现也非常简单，只需要用两个 `把中间的代码包裹起来，代码的语法如下：
 
` -- 代码内容 -- `

 注意这里的`不是单引号，而是键盘左边那个~上的。
 
9）图片

Markdown 使用一种和链接很相似的语法来标记图片，同样也允许两种样式： 行内式和参考式。

行内式的图片语法看起来像是：

```
![Alt text](/path/to/img.jpg)
![Alt text](/path/to/img.jpg "Optional title")
```
详细叙述如下：

    一个惊叹号 !
    接着一个方括号，里面放上图片的替代文字
    接着一个普通括号，里面放上图片的网址，最后还可以用引号包住并加上 选择性的 'title' 文字。

参考式的图片语法则长得像这样：

    ![Alt text][id]
    
「id」是图片参考的名称，图片参考的定义方式则和连结参考一样：

    [id]: url/to/image  "Optional title attribute"
到目前为止， Markdown 还没有办法指定图片的宽高，如果你需要的话，你可以使用普通的 `<img>` 标签。







