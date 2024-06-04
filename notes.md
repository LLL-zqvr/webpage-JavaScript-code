### 什么是 jQuery ？
答：<br>
- jQuery 是一个 JavaScript 函数库。
- jQuery 是一个轻量级的"写的少，做的多"的 JavaScript 库。
- jQuery 库包含以下功能：
  1. HTML 元素选取
  2. HTML 元素操作
  3. CSS 操作
  4. HTML 事件函数
  5. JavaScript 特效和动画
  6. HTML DOM 遍历和修改
  7. AJAX
  8. Utilities
   
### 通过CDN（内容分发网络）引用jQuery
- 百度 CDN:
    <head>
        <script src="https://apps.bdimg.com/libs/jquery/2.1.4/jquery.min.js">
        </script>
    </head>
- Microsoft CDN:
    <head>
        <script src="https://ajax.aspnetcdn.com/ajax/jquery/jquery-1.9.0.min.js"></script>
    </head>
- Staticfile CDN:
    <head>
        <script src="https://cdn.staticfile.net/jquery/1.10.2/jquery.min.js">
        </script>
    </head>

### jQuery 使用版本
- 我们可以在浏览器的 Console 窗口中使用 `$.fn.jquery `命令查看当前 jQuery 使用的版本.

### jQuery 语法 
jQuery 语法是通过选取 HTML 元素，并对选取的元素执行某些操作.

**基础语法： $(selector).action()**
- 美元符号定义 jQuery
- 选择符（selector）"查询"和"查找" HTML 元素
- jQuery 的 action() 执行对元素的操作
如：
1. **$(this).hide()** - 隐藏当前元素
2. **$("p").hide()** - 隐藏所有 `<p>` 元素
3. **$("p.test").hide()** - 隐藏所有 class="test" 的`<p>` 元素
4. **$("#test").hide()** - 隐藏 `id="test"` 的元素

**Tips:**
实例中的所有 jQuery 函数位于一个 document ready 函数中,这是为了防止文档在完全加载（就绪）之前运行 jQuery 代码，即在 DOM 加载完成后才可以对 DOM 进行操作。<br>
如果在文档没有完全加载之前就运行函数，操作可能失败。下面是两个具体的例子：
- 试图隐藏一个不存在的元素
- 获得未完全加载的图像的大小
  
### jQuery 选择器
介绍:
- jQuery 选择器允许您对 HTML 元素组或单个元素进行操作。
- jQuery 选择器基于元素的 id、类、类型、属性、属性值等"查找"（或选择）HTML 元素。 它基于已经存在的 CSS 选择器，除此之外，它还有一些自定义的选择器。
- jQuery 中所有选择器都以**美元符号**开头：**$()**。