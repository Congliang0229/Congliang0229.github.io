---
title: Web入门（二）
date: 2020-09-23 19:20:47
tags:
	- Web
	- HTML
	- CSS
categories: 
	- Web
---

# Web入门（二）

## JavaScript

JavaScript 是一门编程语言，可为网站添加交互功能（例如：游戏、动态样式、动画以及在按下按钮或收到表单数据时做出的响应等）。

<!--more-->

### 变量（Variable）

[变量](https://developer.mozilla.org/en-US/docs/Glossary/Variable) 是存储值的容器。要声明一个变量，先输入关键字 `let` 或 `var`，然后输入合适的名称：

```js
let myVariable;
var myVariable2;
```

*注：单行语句可以不加分号*

String的值必须用引号括起来，单双均可。

```js
let myVariable = '李雷';
```



数组：用于在单一引用中存储多个值的结构。

```js
let myVariable = [1, '李雷', '韩梅梅', 10];
let a = myVariable[0],b = myVariable[1];//元素引用方法
```



***对象：JavaScript 里一切皆对象，一切皆可储存在变量里。这一点要牢记于心。***

---



### 运算符

等于用===：

```js
let myVariable = 3;
myVariable === 4; // false
```

不等于用!==:

```js
let myVariable = 3;
myVariable !== 3; // false
```

---



### 函数

```js
function multiply(num1, num2) {
  let result = num1 * num2;
  return result;
}
```

---



### 事件

事件能为网页添加真实的交互能力。它可以捕捉浏览器操作并运行一些代码做为响应。最简单的事件是 [点击事件](https://developer.mozilla.org/zh-CN/docs/Web/Events/click)，鼠标的点击操作会触发该事件。 可尝试将下面的代码输入到控制台，然后点击页面的任意位置：

```js
document.querySelector('html').onclick = function() {
    alert('别戳我，我怕疼。');//document.querySelector获取html元素
}
```

将事件与元素绑定有许多方法。在这里选用了 [``](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element/html) 元素，把一个匿名函数（就是没有命名的函数，这里的匿名函数包含单击鼠标时要运行的代码）赋值给了 `html` 的 `onclick` 属性。

请注意：

```js
document.querySelector('html').onclick = function() {};
```

等价于

```js
let myHTML = document.querySelector('html');
myHTML.onclick = function() {};
```

只是前者更简洁。

---

***idea 行尾加分号/光标切换到下一行 快捷键***

***Ctrl+Shift+Enter***

---

document.querySelector可以得到html里的一个元素，getAttribute可以得到元素的一个属性值，setAttribute可以设置元素的属性值：

```js
let myImage = document.querySelector('img');

myImage.onclick = function() {
    let mySrc = myImage.getAttribute('src');
    if(mySrc === 'images/firefox-icon.png') {
      myImage.setAttribute('src', 'images/firefox2.png');
    } else {
      myImage.setAttribute('src', 'images/firefox-icon.png');
    }
}
```

 [`prompt()`](https://developer.mozilla.org/zh-CN/docs/Web/API/Window.prompt) 函数， 与 `alert()` 类似会弹出一个对话框。但是这里需要用户输入数据，并在确定后将数据存储在 变量里。

