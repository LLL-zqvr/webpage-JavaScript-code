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
介绍：
通过 jQuery，您可以使用 hide() 和 show() 方法来隐藏和显示 HTML 元素。
语法：
- $(selector).hide(speed,callback);
- $(selector).show(speed,callback);
可选的 speed 参数规定隐藏/显示的**速度**（会得到动态的效果），可以取以下值："slow"、"fast" 或毫秒。
可选的 callback回调函数 参数是隐藏或显示完成后所执行的函数名称。之间还可以加上参数，是一个字符串，表示过渡使用哪种缓动函数。（jQuery自身提供"linear" 和 "swing"，其他可以使用相关的插件）<br>
具体见：[33-hide() and show() (callback)](./code/33-hide()%20and%20show()%20(callback).html)

#### 淡入淡出
- fadeIn()          jQuery fadeIn() 用于淡入已隐藏的元素。
- fadeOut()         jQuery fadeOut() 方法用于淡出可见元素。
- fadeToggle()      jQuery fadeToggle() 方法可以在 fadeIn() 与 fadeOut() 方法之间进行切换。如果元素已淡出，则 fadeToggle() 会向元素添加淡入效果;如果元素已淡入，则 fadeToggle() 会向元素添加淡出效果。
- fadeTo()          jQuery fadeTo() 方法允许渐变为给定的不透明度（值介于 0 与 1 之间）。

#### 滑动
- slideDown()       jQuery slideDown() 方法用于向下滑动元素。
- slideUp()         jQuery slideUp() 方法用于向上滑动元素。
- slideToggle()     jQuery slideToggle() 方法可以在 slideDown() 与 slideUp() 方法之间进行切换。

####  动画
介绍：
jQuery animate() 方法用于创建自定义动画。
该方法通过 CSS 样式将元素从一个状态改变为另一个状态。CSS属性值是逐渐改变的，这样就可以创建动画效果。
只有数字值可创建动画（比如 "margin:30px"）。字符串值无法创建动画（比如 "background-color:red"）。
提示：请使用 "+=" 或 "-=" 来创建相对动画。

语法：$(selector).animate({params},speed,callback);
其中：
- speed	可选。规定动画的速度。
    可能的值：
    1. 毫秒
    2. "slow"
    3. "fast"
- easing 可选。规定在动画的不同点中元素的速度。默认值是 "swing"。
    可能的值：
    1. "swing" - 在开头/结尾移动慢，在中间移动快
    2. "linear" - 匀速移动
    提示：扩展插件中提供更多可用的 easing 函数。
- callback 可选。
    1. animate 函数执行完之后，要执行的函数。

### jquery遍历
- parent() 返回每个匹配元素的直接父元素。
- parents() 返回匹配元素的所有祖先元素。
- parentsUntil() 返回找到给定选择器参数的元素之前的所有祖先元素。
- children() 返回匹配元素的所有直接子元素。
- find() 返回匹配元素的所有子孙元素。
- next() next() 方法返回被选元素的下一个同胞元素。该方法只返回一个元素。
- siblings() siblings() 方法返回被选元素的所有同胞元素。可选参数来过滤对同胞元素的搜索。

### js HTML

#### 捕获元素
- text()    设置或返回所选元素的文本内容(括号里面没值则是返回当前表单字段的值，若括号里面有值则是设置值)。
- html()    设置或返回所选元素的内容（包括 HTML 标签）(括号里面没值则是返回当前表单字段的值，若括号里面有值则是设置值)。
- val()     设置或返回表单字段的值(括号里面没值则是返回当前表单字段的值，若括号里面有值则是设置值)。
- attr()    用于获取属性值。

#### 添加元素
- append() - 在被选元素的结尾插入内容
- prepend() - 在被选元素的开头插入内容
- after() - 在被选元素之后插入内容
- before() - 在被选元素之前插入内容

#### HTML方法
- prop() 方法设置或返回被选元素的属性和值。当该方法用于返回属性值时，则返回第一个匹配元素的值。当该方法用于设置属性值时，则为匹配元素集合设置一个或多个属性/值对。