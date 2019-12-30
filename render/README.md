# 页面渲染过程

当渲染进程 `提交文档` 给浏览器之后，浏览器便开始渲染页面和加载资源。

页面渲染的过程(按照时间顺序)大致分为以下几点：<br>
* 构建dom树
* 构建cssom（计算css样式）
* dom树和cssom合并形成渲染树（render tree）
* 根据渲染树呈现布局


#### 构建dom树

什么是 `dom树` ？<Br>
`dom树` 指的是将一个 `html` 文件解析成浏览器可以识别的结构，最终输出树状结构的 `dom`；


我们打开浏览器的 `控制台` - `console` ，输入 `document` 后回车。<br>
我们可以看到控制台输出一个完整的 `dom` 结构。

我们可以看到输出的 `dom` 结构与我们 `html` 的内容是一模一样的。<br>
但是不同的是，`dom` 是保存在内存中的树状图结构，可以用 `JS` 来查询或者修改 `dom` 的内容。

比如你要获取 `html` 的内容，我们可以在 `控制台` - `console` 输入：

(以 https://www.baidu.com/ 为例)

```copy
document.documentElement
```

输出结构为：

```copy
<html>
    <header>...</header>
    <body link="#0000cc" style>...</body>
</html>
```


#### 构建cssom

`构建cssom` ，其实就是计算 `css` ;<br>
<Br>

<b>一般我们 `css` 的来源有三个途径：</b>
* 通过 `<link>` 标签引入的 `css文件` ；
* 在 `<style>` 标记内的 `css` ；
* 在元素中的 `style` 属性中的 `css` ；

<br>

就跟 `html` 一样，浏览器无法直接理解这些文件， `css` 需要转换成浏览器能够识别的结构。
这个就是 `styleSheet` 。<br><br>

我们可以通过 `控制台` - `console` 来查看 `cssom` 的结构：

(以 https://www.baidu.com/ 为例)

```copy
document.styleSheets
```

输出结构为：

```copy
StyleSheetList {0: CSSStyleSheet, 1: CSSStyleSheet, 2: CSSStyleSheet, 3: CSSStyleSheet, 4: CSSStyleSheet, 5: CSSStyleSheet, 6: CSSStyleSheet, 7: CSSStyleSheet, length: 8}
```

<br>

这个 `styleSheets` 会把我们刚才说的三种 `css` 途径来源一起输出出来。<br>
同样，这个 `styleSheets` 也具备来查询和修改的功能。

接下来，渲染进程还会进一步处理这个 `styleSheets` 。在 `css` 中有一些相对的单位和一些语意化的属性值（比如说 `rem` ，`em` ， `red` ，`bold` 等等）并不能很好的让渲染引擎理解，所以需要将这些转换成渲染引擎容易理解的值。

```copy
color:red;            -->       color:rgb(255,0,0);
font-size:1rem;       -->       font-size:100px;
font-weight:bold;     -->       font-weight:700;
```

从

<Br>
<Br>

<!-- https://coolshell.cn/articles/11564.html -->
<!-- https://coolshell.cn/articles/9666.html -->
