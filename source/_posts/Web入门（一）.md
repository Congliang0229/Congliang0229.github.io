---
title: Web入门（一）
date: 2020-09-20 17:46:03
tags:
	- Web
	- HTML
	- CSS
categories: 
	- Web
---

# Web入门（一）

## 网站应该使用什么结构？

> 最基本、最常见的网页结构是：一个主页、一个图片文件夹、一个样式表文件夹和一个脚本文件夹：

<!--more-->

1. `**index.html**` ：这个文件一般包含主页内容，即用户第一次访问站点时看到的文本和图像。使用文本编辑器在 `test-site` 文件夹中新建 `index.html`。

2. **`images` 文件夹** ：这个文件夹包含站点中的所有图像。在 `test-site` 文件夹中新建 `images` 文件夹。

3. **`styles` 文件夹** ：这个文件夹包含站点所需样式表（比如，设置文本颜色和背景颜色）。在 `test-site` 文件夹中新建一个 `styles` 文件夹。

4. **`scripts` 文件夹** ：这个文件夹包含提供站点交互功能的 JavaScript 代码（比如读取数据的按钮）。在 `test-site` 文件夹中新建一个 `scripts` 文件夹。

## HTML简介



> 超文本标记语言 (英语：**H**yper**t**ext **M**arkup **L**anguage，简称：HTML ) 是一种用来结构化 Web 网页及其内容的标记语言。网页内容可以是：一组段落、一个重点信息列表、也可以含有图片和数据表。

文件路径的一些通用规则：

- 若引用的目标文件与 HTML 文件同级，只需直接使用文件名，比如 `my-image.jpg` 。

- 要引用子文件夹中的文件，要在路径前写下目录名并加一个斜杠，比如 `subdirectory/my-image.jpg` 。

- 若引用的目标文件位于 HTML 文件的**上级**，需要加上两个点。比如，如果 `index.html` 在 `test-site` 下面的一个子目录而 `my-image.png` 在 `test-site` 目录，你可以在 `index.html` 里使用 `../my-image.png` 引用 `my-image.png` 。

- 以上方法可以随意组合，比如 `../subdirectory/another-subdirectory/my-image.png`。

  

![](https://mdn.mozillademos.org/files/16475/element.png)

属性应该包含：

1. 在属性与元素名称（或上一个属性，如果有超过一个属性的话）之间的空格符。

2. 属性的名称，并接上一个等号。

3. 由引号所包围的属性值。

   ![](https://mdn.mozillademos.org/files/16476/attribute.png)

### 嵌套元素

也可以将一个元素置于其他元素之中 —— 称作**嵌套**。要表明猫咪非常暴躁，可以将 “爆” 用 [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/strong) 元素包围，爆字将突出显示：

```html
<p>我的猫咪脾气<strong>爆</strong>:)</p>
```

###  

### 空元素

不包含任何内容的元素称为空元素。比如 [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/img) 元素：

```html
<img src="images/firefox-icon.png" alt="测试图片">
```

### HTML 文档详解

以上介绍了一些基本的 HTML 元素，但孤木不成林。现在来看看单个元素如何彼此协同构成一个完整的 HTML 页面。示例：

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">
    <title>测试页面</title>
  </head>
  <body>
    <img src="images/firefox-icon.png" alt="测试图片">
  </body>
</html>
```

这里有：

- `<!DOCTYPE html>` — 文档类型。混沌初分，HTML 尚在襁褓（大约是 1991/92 年）之时，`DOCTYPE` 用来链接一些 HTML 编写守则，比如自动查错之类。`DOCTYPE` 在当今作用有限，仅用于保证文档正常读取。现在知道这些就足够了。
- `<html></html>` — [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/html) 元素。该元素包含整个页面的内容，也称作根元素。
- `<head></head>` — [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/head) 元素。该元素的内容对用户不可见，其中包含例如面向搜索引擎的搜索关键字（[keywords](https://developer.mozilla.org/zh-CN/docs/Glossary/Keyword)）、页面描述、CSS 样式表和字符编码声明等。
- `<meta charset="utf-8">` — 该元素指定文档使用 UTF-8 字符编码 ，UTF-8 包括绝大多数人类已知语言的字符。基本上 UTF-8 可以处理任何文本内容，还可以避免以后出现某些问题，没有理由再选用其他编码。
- `<title></title>` — [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/title) 元素。该元素设置页面的标题，显示在浏览器标签页上，也作为收藏网页的描述文字。
- `<body></body>` — [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/body) 元素。该元素包含期望让用户在访问页面时看到的内容，包括文本、图像、视频、游戏、可播放的音轨或其他内容。

---

## HTML标记文本

### 标题（Heading）

标题元素可用于指定内容的标题和子标题。就像一本书的书名、每章的大标题、小标题，等。HTML 文档也是一样。HTML 包括六个级别的标题， [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h1)–[``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/h6) ，一般最多用到 3-4 级标题。

```html  
<h1>主标题</h1>
<h2>顶层标题</h2>
<h3>子标题</h3>
<h4>次子标题</h4>
```



### 段落（Paragraph）

如上文所讲，[``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/p) 元素是用来指定段落的。通常用于指定常规的文本内容：

```html
<p>这是一个段落</p>
```

   

### 列表（List）

Web 上的许多内容都是列表，HTML 有一些特别的列表元素。标记列表通常包括至少两个元素。最常用的列表类型为：

1. **无序列表（Unordered List）**中项目的顺序并不重要，就像购物列表。用一个 [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ul) 元素包围。
2. **有序列表（Ordered List）**中项目的顺序很重要，就像烹调指南。用一个 [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/ol) 元素包围。

列表的每个项目用一个列表项目（List Item）元素 [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/li) 包围。

比如，要将下面的段落片段改成一个列表：

```html
<p>Mozilla 是一个全球社区，这里聚集着来自五湖四海的技术人员、思考者和建造者，我们致力于……</p>
```

可以这样更改标记：

```html
<p>Mozilla 是一个全球社区，这里聚集着来自五湖四海的</p>
    
<ul> 
  <li>技术人员</li>
  <li>思考者</li>
  <li>建造者</li>
</ul>

<p>我们致力于……</p>
```

### 链接    

很重要！示例：

```html
<a href="https://www.mozilla.org/zh-CN/about/manifesto/">Mozilla 宣言</a>
```

---

## CSS基础

> 层叠样式表（**C**ascading **S**tyle **S**heet，简称：CSS）是为网页添加样式的代码。和 HTML 类似，CSS 也不是真正的编程语言，甚至不是标记语言。它是一门样式表语言，这也就是说人们可以用它来选择性地为 HTML 元素添加样式。

语法样例：

```css
p {
  color: red;
}
```

之后需要将CSS文件连接至HTML文档，打开需要连接的HTML，然后在head标签上添加。例如：  

```html
<link href="styles/style.css" rel="stylesheet">
```



### 不同类型的选择器

选择器有许多不同的类型。上面只介绍了**元素选择器**，用来选择 HTML 文档中给定的元素。但是选择操作可以更加具体。下面是一些常用的选择器类型：

| 选择器名称                           | 选择的内容                                                   | 示例                                                         |
| :----------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- |
| 元素选择器（也称作标签或类型选择器） | 所有指定(该)类型的 HTML 元素                                 | `p` 选择 `<p>`                                               |
| ID 选择器                            | 具有特定 ID 的元素（单一 HTML 页面中，每个 ID 只对应一个元素，一个元素只对应一个 ID） | `#my-id` 选择 `<p id="my-id">` 或 `<a id="my-id">`           |
| 类选择器                             | 具有特定类的元素（单一页面中，一个类可以有多个实例）         | `.my-class` 选择 `<p class="my-class">` 和 `<a class="my-class">` |
| 属性选择器                           | 拥有特定属性的元素                                           | `img[src]` 选择 `<img src="myimage.png">`而不是 `<img>`      |
| 伪（Pseudo）类选择器                 | 特定状态下的特定元素（比如鼠标指针悬停）                     | `a:hover` 仅在鼠标指针悬停在链接上时选择 `<a>`。             |

---



### 一切皆盒子

编写 CSS 时你会发现，你的工作好像是围绕着一个一个盒子展开的——设置尺寸、颜色、位置，等等。页面里大部分 HTML 元素都可以被看作若干层叠的盒子。

![a big stack of boxes or crates sat on top of one another](https://mdn.mozillademos.org/files/9441/boxes.jpg)

并不意外，CSS 布局主要就是基于盒模型的。每个占据页面空间的块都有这样的属性：

- `padding`：即内边距，围绕着内容（比如段落）的空间。
- `border`：即边框，紧接着内边距的线。
- `margin`：即外边距，围绕元素外部的空间。

![three boxes sat inside one another. From outside to in they are labelled margin, border and padding](https://mdn.mozillademos.org/files/9443/box-model.png)

```css
body {
  width: 600px;
  margin: 0 auto;
  background-color: #FF9500;
  padding: 0 20px 20px 20px;
  border: 5px solid black;
}
```

margin 就是该块距离外面的块的上右下左距离。padding是块内文字距离块边界的上右下左距离。