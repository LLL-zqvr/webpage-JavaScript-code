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
        <script src="https://ajax.aspnetcdn.com/ajax/jquery/jquery-1.9.0.min.js">
        </script>
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
- 试图隐藏一个不存在的元素.
- 获得未完全加载的图像的大小.
  
### jQuery 选择器
介绍:
- jQuery 选择器允许您对 HTML 元素组或单个元素进行操作。
- jQuery 选择器基于元素的 id、类、类型、属性、属性值等"查找"（或选择）HTML 元素。 它基于已经存在的 CSS 选择器，除此之外，它还有一些自定义的选择器。
- jQuery 中所有选择器都以**美元符号**开头：**$()**。
  
#### 元素选择器
介绍:
- jQuery 元素选择器基于元素名选取元素。
- 在页面中选取所有 <p> 元素语法如下:`$("p")`。
  
#### id 选择器
介绍：
- jQuery #id 选择器通过 HTML 元素的 id 属性选取指定的元素。
- 页面中元素的 id 应该是唯一的，所以您要在页面中选取唯一的元素需要通过 #id 选择器。
- 通过 id 选取元素语法如下：`$("#test")`。

#### .class 选择器
介绍：
- jQuery 类选择器可以通过指定的 class 查找元素。
- 语法如下：`$(".test")`。

#### 更多用法
- `$("*")`	选取所有元素	
- `$(this)`	选取当前 HTML 元素	
- `$("p.intro")`	选取 class 为 intro 的`<p>`元素	
- `$("p:first")`选取第一个`<p>`元素	
- `$("ul li:first")`	选取第一个 `<ul>` 元素的第一个 `<li>` 元素	
- `$("ul li:first-child")`	选取每个 `<ul>` 元素的第一个 `<li>` 元素	
- `$("[href]")`	选取带有 `href` 属性的元素	
- `$("a[target='_blank']")`	选取所有 target 属性值等于 "_blank" 的 `<a>` 元素	
- `$("a[target!='_blank']")`	选取所有 target 属性值不等于 "_blank" 的 `<a>` 元素
- `$(":button")`     选取所有 type="button" 的 `<input>` 元素 和 `<button>` 元素
- `$("tr:even")`	 选取偶数位置的 `<tr>` 元素	
- `$("tr:odd")`	 选取奇数位置的 `<tr>` 元素

### jQuery 事件
介绍：
- 页面对不同访问者的响应叫做事件。
- 事件处理程序指的是当 HTML 中发生某些事件时所调用的方法。
- 实例：
    1. 在元素上移动鼠标。
    2. 选取单选按钮。
    3. 点击元素
    4. 在事件中经常使用术语"触发"（或"激发"）例如： "当您按下按键时触发 keypress 事件"。
- 常见的事件：
#### 鼠标事件
1. **click**            单击元素时触发
2. **dblclick**         双击元素时触发
3. **mouseenter**       当鼠标指针穿过（进入）被选元素时触发(与 mouseover 事件不同，mouseenter 事件只有在鼠标指针进入被选元素时被触发，mouseover 事件在鼠标指针进入任意子元素时也会被触发。)
4. **mouseleave**       当鼠标指针离开被选元素时触发
5. **hover**            hover() 方法规定当鼠标指针悬停在被选元素上时要运行的两个函数。方法触发 `mouseenter` 和 `mouseleave` 事件。<br>
                        如:
                            `$("p").hover(function(){
                                $("p").css("background-color","yellow");
                                },function(){
                                $("p").css("background-color","pink");
                            });`
        另: 如果只指定一个函数，则 `mouseenter` 和 `mouseleave` 都执行它。
6. **mousedown()**              当鼠标指针移动到元素上方，并按下鼠标按键时，会发生 mousedown 事件。
7. **mouseup()**        当在元素上松开鼠标按钮时，会发生 mouseup 事件。
#### 键盘事件
1. **keypress**         键被按下触发      
2. **keydown**          键按下的过程触发
3.  **keyup**            键被松开触发
#### 表单事件
1.  **submit**           提交表单触发（另：只适用于<form>）
2.  **change**           当元素的值改变时发生 change 事件（仅适用于表单字段）。当用于 select 元素时，change 事件会在选择某个选项时发生。当用于 text field 或 text area 时，change 事件会在元素失去焦点时发生。
3.  **focus**            当元素获得焦点时（当通过鼠标点击选中元素或通过 tab 键定位到元素时），发生 focus 事件。另：该方法通常与 blur() 方法一起使用。
4.  **blur**             当元素失去焦点时发生 blur 事件。
#### 文档/窗口事件
1.  **load**             当指定的元素已加载时，会发生 load 事件。（另：**load() 方法在 jQuery 版本 1.8 中已废弃！**）
2.  **resize**           当调整浏览器窗口大小时，发生 resize 事件。
3.  **scroll**           当用户滚动指定的元素时，会发生 scroll 事件。
4.  **unload**	        当用户离开页面时，会发生 unload 事件。另：**unload() 方法在 jQuery 版本 1.8 中被废弃，在 3.0 版本被移除。Firefox 与 Chrome 会阻止弹窗，所以没办法看到效果。**

### jQuery 效果

#### 隐藏和显示
介绍：通过 jQuery，您可以使用 hide() 和 show() 方法来隐藏和显示 HTML 元素。
语法：
- $(selector).hide(speed,callback);
- $(selector).show(speed,callback);
可选的 speed 参数规定隐藏/显示的**速度**（会得到动态的效果），可以取以下值："slow"、"fast" 或毫秒。
可选的 callback回调函数 参数是隐藏或显示完成后所执行的函数名称。之间还可以加上参数，是一个字符串，表示过渡使用哪种缓动函数。（jQuery自身提供"linear" 和 "swing"，其他可以使用相关的插件）<br>
具体见：[33-hide() and show() (callback)](./code/33-hide()%20and%20show()%20(callback).html)