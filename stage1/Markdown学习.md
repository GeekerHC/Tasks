# Markdown学习

[TOC]

## 语法

> 要创建标题，请在单词或短语前面添加井号# 。#的数量代表了标题的级别。

注意，在拟写标题时，请用一个空格在#和标题之间进行分隔。   

## 段落语法

> 要创建段落，请使用空白行将一行或多行文本进行分隔。

## 换行语法

> 在一行的末尾添加两个或多个空格，然后按回车键,即可创建一个换行.

## 强调语法

### 斜体

> 要用斜体显示文本，请在单词或短语前后添加一个星号或下划线。要斜体突出单词的中间部分，请在字母前后各添加**一**个星号，中间不要带空格。

### 粗体

> 要加粗文本，请在单词或短语的前后各添加两个星号或下划线。如需加粗一个单词或短语的中间部分用以表示强调的话，请在要加粗部分的两侧各添加**两**个星号。

### 粗体与斜体

> 要同时用粗体和斜体突出显示文本，请在单词或短语的前后各添加三个星号或下划线。要加粗并用斜体显示单词或短语的中间部分，请在要突出显示的部分前后各添加**三**个星号，中间不要带空格。

## 引用语法

> 要创建块引用，请在段落前添加一个>符号。

### 多个段落的块引用

> 块引用可以包含多个段落。为段落之间的空白行添加一个>符号。

### 嵌套块引用

> 块引用可以嵌套。在要嵌套的段落前添加一个>>符号。

### 带有其它元素的块引用

>块引用可以包含其他 Markdown 格式的元素。并非所有元素都可以使用，你需要进行实验以查看哪些元素有效。

## 列表语法

### 有序列表

>要创建有序列表，请在每个列表项前添加数字并紧跟一个英文句点。数字不必按数学顺序排列，但是列表应当以数字 1 起始。

### 无序列表

>要创建无序列表，请在每个列表项前面添加破折号 (-)、星号 (*) 或加号 (+) 。缩进一个或多个列表项可创建嵌套列表。

### 在列表中嵌套其他元素

要在保留列表连续性的同时在列表中添加另一种元素，请将该元素缩进四个空格或一个制表符。

## 代码语法

> 要将单词或短语表示为代码，请将其包裹在引号 ( '  ' ) 中。

### 转义反引号

> 如果你要表示为代码的单词或短语中包含一个或多个反引号，则可以通过将单词或短语包裹在双反引号( "  " )中。

### 代码块

> 要创建代码块，请将代码块的每一行缩进至少四个空格或一个制表符。

## 分隔线语法

> 要创建分隔线，请在单独一行上使用三个或多个星号 (***)、破折号 (---) 或下划线 (___) ，并且不能包含其他内容。

## 链接语法

链接文本放在中括号内，链接地址放在后面的括号中，链接title可选。

超链接Markdown语法代码：`[超链接显示名](超链接地址 "超链接title")`

对应的HTML代码：`<a href="超链接地址" title="超链接title">超链接显示名</a>`

### 给链接增加 Title

> 链接title是当鼠标悬停在链接上时会出现的文字，这个title是可选的，它放在圆括号中链接地址后面，跟链接地址之间以空格分隔。

### 网址和Email地址

> 使用尖括号可以很方便地把URL或者email地址变成可点击的链接。

### 带格式化的链接

> 链接, 在链接语法前后增加星号。 要将链接表示为代码，请在方括号中添加反引号。

### 引用类型链接

>引用样式链接是一种特殊的链接，它使URL在Markdown中更易于显示和阅读。参考样式链接分为两部分：与文本保持内联的部分以及存储在文件中其他位置的部分，以使文本易于阅读。

## 图片语法

>要添加图像，请使用感叹号 (`!`), 然后在方括号增加替代文本，图片链接放在圆括号里，括号里的链接后可以增加一个可选的图片标题文本。
>
>插入图片Markdown语法代码：`![图片alt](图片链接 "图片title")`。
>
>对应的HTML代码：`<img src="图片链接" alt="图片alt" title="图片title">`

### 链接图片

> 给图片增加链接，请将图像的Markdown 括在方括号中，然后将链接添加在圆括号中。

## 转义字符语法

> 要显示原本用于格式化 Markdown 文档的字符，请在字符前面添加反斜杠字符 () 。

### 可做转义的字符

以下列出的字符都可以通过使用反斜杠字符从而达到转义目的。

| Character |                             Name                             |
| :-------: | :----------------------------------------------------------: |
|     \     |                          backslash                           |
|     `     | backtick (see also [escaping backticks in code](https://markdown.com.cn/basic-syntax/escaping-characters.html#escaping-backticks)) |
|     *     |                           asterisk                           |
|     _     |                          underscore                          |
|    { }    |                         curly braces                         |
|    [ ]    |                           brackets                           |
|    ( )    |                         parentheses                          |
|     #     |                          pound sign                          |
|     +     |                          plus sign                           |
|     -     |                     minus sign (hyphen)                      |
|     .     |                             dot                              |
|     !     |                       exclamation mark                       |
|    \|     | pipe (see also [escaping pipe in tables](https://markdown.com.cn/extended-syntax/escaping-pipe-characters-in-tables.html)) |

## 内嵌 HTML 标签

对于 Markdown 涵盖范围之外的标签，都可以直接在文件里面用 HTML 本身。如需使用 HTML，不需要额外标注这是 HTML 或是 Markdown，只需 HTML 标签添加到 Markdown 文本中即可。

### 行级內联标签

>HTML 的行级內联标签如 `<span>`、`<cite>`、`<del>` 不受限制，可以在 Markdown 的段落、列表或是标题里任意使用。依照个人习惯，甚至可以不用 Markdown 格式，而采用 HTML 标签来格式化。例如：如果比较喜欢 HTML 的 `<a>` 或 `<img>` 标签，可以直接使用这些标签，而不用 Markdown 提供的链接或是图片语法。当你需要更改元素的属性时（例如为文本指定颜色或更改图像的宽度），使用 HTML 标签更方便些。
>
>HTML 行级內联标签和区块标签不同，在內联标签的范围内， Markdown 的语法是可以解析的。

### 区块标签

>区块元素──比如 `<div>`、`<table>`、`<pre>`、`<p>` 等标签，必须在前后加上空行，以便于内容区分。而且这些元素的开始与结尾标签，不可以用 tab 或是空白来缩进。Markdown 会自动识别这区块元素，避免在区块标签前后加上没有必要的 `<p>` 标签。

请注意，Markdown 语法在 HTML 区块标签中将不会被进行处理。

