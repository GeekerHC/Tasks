# HTML学习——构建Web

[TOC]

## 基本内容

### 简介

HTML（Hyper Text Markup Language）,即超文本标记语言，时Web最基本的构建块。它定义了Web的内容含义和结构。  

不同于编程语言，HTML时一种用于定义内容结构的**标记语言**。HTML由一系列的元素组成，这些元素用来包裹不同部分的内容，使其以某种方式呈现或者工作。

其文档格式为“.html”或“.htm”

### 标签

#### 总览

在正式学习HTML前，我们先了解标签这个概念，类似C语言中的关键字，标签是具有特定意义的一类文字形式，它承担了一些实际上的功能。这样的描述是不严谨的，但是对于刚接触HTML的人而言却是最易理解的。

！[标签](https://img-blog.csdnimg.cn/20201230171712536.png?x-oss-process=image/watermark,type_ZmFuZ3poZW5naGVpdGk,shadow_10,text_aHR0cHM6Ly9ibG9nLmNzZG4ubmV0L3dlaXhpbl80NDY4NDI3Mg==,size_16,color_FFFFFF,t_70)

#### 按结构分

- **围堵标签**：有开始标签和结束标签，如< html > < /html >。
- **自闭合标签**：开始和结束标签在一起，如 < br/>。

#### 按功能分

1. **文件标签**

- html:*HTML文档的根标签。该元素包含整个页面的内容，也称作根元素。*
- head:*头标签。该元素的内容对用户不可见，其中包含例如面向搜索引擎的搜索关键字、页面描述、CSS 样式表和字符编码声明等。*
- title：*标题标签，显示在浏览器标签页上。*
- body：*体标，包含期望让用户在访问页面时看到的内容，包括文本、图像、视频、游戏、可播放的音轨或其他内容。*

2. **文本标签**

- < !-- 注释内容 -->:*注释*
- < h1> to < h6>:*标题标签*（区别title）
- < p>：*段落标签*
- < br>：*换行标签*
- < hr>：*展示一条水平线*


### 元素

由简介可知，元素是构成HTML最基本的单位。一个元素的主要部分有：

- **开始标签**：包含元素名，该标签表示元素从这里开始或者起作用。
- **结束标签**：在开始标签的元素名前包含一个*斜杠*，该标签表示元素的结尾。
- **内容**：元素的内容。

这三个部分组合起来，就是一个完整的元素，而Web正需要一个个元素拼接起来而形成的。

### 元素的分类

1. **块级元素**

- 在页面以块的形式展现

- 出现在新的一行

- 占全部宽度

  eg：

  > \<div>、\<h1>-\<h6>、\<p>

2. **内联元素**

- 通常在块级元素内

- 不会导致文本换行

- 只占必要的部分宽度

  eg:\<strong>、\<em>

### 标签和元素的区别

当初学标签和元素时，因其相似的外形和CSDN上模棱两可的介绍，我们很难区别标签和元素的区别。但从定义上看，我们不难发现，元素就是一个**整体**，包括标签

、文本内容等，而标签仅仅只是一些类似关键字的东西。

eg：

> <p>Lorem ipsum dolor sit amet</p>

在这个元素中，'<p>'是开始标签（opening tag），‘</p>’是结束标签，被包围的则是文本内容。

### 元素的属性

我们以一个例子来引入属性的概念。  

eg：

> \<p href="https://google.com">Lorem ipsum dolor sit amet</p>

在这个例子中，"href='https://google.com'就是属性。*href*属性可以在Web中插入超链接。

属性包含了关于元素的一些额外信息，这些信息本身不应显现在内容中，他一般包含：

1. 在属性与元素名称（或上一个属性，如果有超过一个属性的话）之间的**空格符**。
2. 属性的名称，并接上一个**等号**。
3. 由**引号**所包围的属性值。

### 文档基本格式

		<html>
			
				<head>
					<title>title</title>
				</head>
				
				<body>
	                <h1>This is a heading</h1>
					<br/>
					<p>This is a paragraph</p>
					<font color='green'>Hello World</font>
				
				</body>
		
			</html>

## 结语

完成一个网页，需要的东西基本都有了，展示一些基本的文字已经不是问题了，改变字体和颜色等简单功能也可以通过嵌套元素来实现，而对应的标签都可以查询到。但是例如嵌入多媒体、表格、表单等需要其他方法实现，在此则不过多深入了解。我在此留下一个链接[HTML初学者教程](https://developer.mozilla.org/zh-CN/docs/Web/HTML)以便后期进一步学习。

