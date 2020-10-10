---
title: HTML学习（一）
date: 2020-09-28 16:31:55
tags: 
	- Web
	- HTML
categories: 
	-Web
---

# HTML介绍

## HMTL入门



>  当页面被加载后HTML中的head部分**是不会**被显示在web浏览器中的。它包含了许多信息，例如网页的标题[``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/title)，指向[CSS](https://developer.mozilla.org/zh-CN/docs/Glossary/CSS)的链接（如果你想用CSS来设计HTML内容的样式），指向自定义网站图标的链接和一些元数据（关于HTML本身的数据，例如它的作者和描述这个文档的关键字）。
>
> 

>  **注：**HTML 标签**不区分大小写**。也就是说，输入标签时既可以使用大写字母也可以使用小写字母。例如，标签 [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/title) 写作`<title>、``<TITLE>`、`<Title>`、`<TiTlE>`，等等都可以正常工作。不过，从一致性、可读性等各方面来说，最好仅使用小写字母。

### 斜体强调：<em>

```html
<em>刀枪剑戟 斧钺钩叉</em>
```



### 嵌套元素

```html
<p>我的猫咪脾气<strong>爆</strong>:)</p>
```

必须注意打开和关闭的次序



### 块级元素和内联元素

- 块级元素在页面中以块的形式展现 —— 相对于其前面的内容它会出现在新的一行，其后的内容也会被挤到下一行展现。
- 内联元素通常出现在块级元素中并环绕文档内容的一小部分，，内联元素不会导致文本换行。

```html
<em>第一</em><em>第二</em><em>第三</em> //内联

<p>第四</p><p>第五</p><p>第六</p>//块级
```



### 空元素

不是所有元素都拥有开始标签，内容，结束标签。一些元素只有一个标签，通常用来在此元素所在位置插入/嵌入一些东西。例如：元素img是用来在元素img所在位置插入图片

```html
<img src="https://roy-tian.github.io/learning-area/extras/getting-started-web/beginner-html-site/images/firefox-icon.png">
```



### 属性

元素可以拥有属性。![&amp;amp;amp;lt;p class="editor-note">æçç«åªè¾æ°ç&amp;amp;amp;lt;/p>](https://mdn.mozillademos.org/files/16476/attribute.png)

在上述例子中，这个class属性给元素赋了一个识别的名字（id），这个名字此后可以被用来识别此元素的样式信息和其他信息。

一个属性必须包含如下内容：

1. 一个空格，在属性和元素名称之间。(如果已经有一个或多个属性，就与前一个属性之间有一个空格。)
2. 属性名称，后面跟着一个等于号。
3. 一个属性值，由一对引号“ ”引起来。

### 锚元素<a>

元素[``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/a)是锚，它使被标签包裹的内容成为一个超链接。此元素也可以添加大量的属性，其中几个如下：

- `href`: 这个属性声明超链接的web地址，当这个链接被点击浏览器会跳转至href声明的web地址。例如：`href="https://www.mozilla.org/"`。
- `title`: 标题`title`属性为超链接声明额外的信息，比如你将链接至的那个页面。例如：`title="The Mozilla homepage"`。当鼠标悬停在超链接上面时，这部分信息将以工具提示的形式显示。
- `target`: 目标`target`属性用于指定链接如何呈现出来。例如，`target="_blank"`将在新标签页中显示链接。如果你希望在当前标签页显示链接，忽略这个属性即可。`target="_parent"`直接由当前页面跳转至目标页。
- 

### 布尔属性

有时你会看到没有值的属性，它是合法的。这些属性被称为布尔属性，**他们只能有跟它的属性名一样的属性值**。例如`disabled` 属性，他们可以标记表单输入使之变为不可用(变灰色)，此时用户不能向他们输入任何数据。

```html
<input type="text" disabled="disabled">
```

方便起见，我们完全可以将其写成以下形式(我们还提供了一个非禁止输入的表单元素供您参考，以作为对比)：

```html
<!-- 使用disabled属性来防止终端用户输入文本到输入框中 -->
<input type="text" disabled>

<!-- 下面这个输入框没有disabled属性，所以用户可以向其中输入 -->
<input type="text">
```



### 单引号或者双引号？

单双引号都可以用，已经用了一种引号时可以在此引号中嵌套另外一种引号：

```html
<a href="http://www.example.com" title="你觉得'好玩吗'？">示例站点链接</a>
```



### 剖析HTML文档

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>我的测试站点</title>
  </head>
  <body>
    <p>这是我的页面</p>
  </body>
</html>`<!DOCTYPE html>`: 声明文档类型. 
```

1. `<!DOCTYPE html>`: 声明文档类型. 
2. `<html></html>`: `<html>`元素。这个元素包裹了整个完整的页面，是一个根元素。
3. `<head></head>`: `<head>元素`. 这个元素是一个容器，它包含了所有你想包含在HTML页面中但不想在HTML页面中显示的内容。这些内容包括你想在搜索结果中出现的关键字和页面描述，CSS样式，字符集声明等等。
4. `<meta charset="utf-8">`: 这个元素设置文档使用utf-8字符集编码，utf-8字符集包含了人类大部分的文字。基本上他能识别你放上去的所有文本内容。
5. `<title></title>`: 设置页面标题，出现在浏览器标签上，当你标记/收藏页面时它可用来描述页面。
6. `<body></body>`: `<body>`元素。 包含了你访问页面时所有显示在页面上的内容，文本，图片，音频，游戏等等。

### HTML中的空白

```html
<p>狗 狗 很 呆 萌。</p>

<p>狗 狗        很
         呆 萌。</p>
```

上面两个代码段等价。

无论你在HTML元素的内容中使用多少空格(包括空白字符，包括换行)，当渲染这些代码的时候，HTML解释器会将连续出现的空白字符**减少为一个单独的空格符**。



### 实体引用： 在HTML中包含特殊字符

在HTML中，字符 `<`, `>`,`"`,`'` 和 `&` 是特殊字符. 它们是HTML语法自身的一部分, 那么你如何将这些字符包含进你的文本中呢, 比如说如果你真的想要在文本中使用符号&或者小于号, 而不想让它们被浏览器视为代码并被解释?

我们必须使用字符引用 —— 表示字符的特殊编码, 它们可以在那些情况下使用. 每个字符引用以符号&开始, 以**分号(;)**结束.

| 原义字符 | 等价字符引用 |
| :------- | :----------- |
| <        | &lt          |
| >        | &gt          |
| "        | &quot        |
| '        | &apos        |
| &        | &amp         |

```html
<p>HTML 中用 &lt;p&gt; 来定义段落元素</p>
<p>HTML 中用 <p> 来定义段落元素。</p>
```



### HTML注释

```html
<p>我在注释外！</p>

<!-- <p>我在注释内！</p> -->
```



