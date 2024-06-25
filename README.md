# webpage-JavaCcript-Code

### Introductions

主要记录有关网页开发的代码。其中多为JavaScript，Jquery（CSS在本库仅为辅助作用，若想查看其实际、详细的介绍和运用请移步本人的另一仓库——webpage-CSS-code，里面对常用的CSS属性都有着专门的针对性的练习（￣︶￣））。


### Development Environments

- VsCode

- Git

### Update

#### 2024/5/14 

按照老师的要求学习了JS的基本语法。本库内标号为1 ~ 27的内容皆为对应的实现。因其内容略多且较为基础，暂不使用链接引出，感兴趣的话欢迎直接点击code进行查看。每节主要内容都已体现在每节的标题中~

#### 2024/5/15 ~ 2024/5/16

对JS整一点小练习~
- [追加内容](/code/example01-Appends%20the%20input%20content%20to%20the%20list.html)
- [选择列表内的东西（指定数量）](/code/example02-Select%20a%20specified%20number%20of%20options.html)

#### 2024/5/17

使用JS实现了以下需求：
当 2s 后输入框没有输入时，将输入字母转为大写。(up/down 事件；定时器；定时器取消；封装)<br>
[2s后输入框无操作，输入字母转大写](/code/homework01.html)

#### 2024/5/19

使用JS实现了以下需求：
当改变课程名称下拉框值时，从对象数组中找到对应的授课教师姓名，渲染到页面。
下拉框项的值为 id 值。

[
  { "id": 1, "courseName": "Java", "teacherName": "BO" },
  { "id": 2, "courseName": "Web", "teacherName": "SUN" },
  { "id": 3, "courseName": "Python", "teacherName": "ZHANG" }
]
<br>
[改变课程名称下拉框值时，将授课教师姓名渲染到页面。](/code/homework02.html)

#### 2024/5/21

实现了导航组的手风琴效果。<br>
[导航组的手风琴效果](/code/homework03.html)


#### 2024/5/24

学习了Jquery基本语法。相应笔记如下~<br>
[Jquery笔记](/jQuery-notes.md)

#### 2024/6/10

用自己的思路实现了选课系统的避免选课时间冲突需求。<br>
[避免选课时间冲突1.0](/code/homework04-Avoid%20scheduling%20conflicts.html)

#### 2024/6/11

用自己的思路实现了将一个数转成千分数格式（该数可能小数可能负数）<br>
[普通数转千分数](/code/homework05.html)

#### 2024/6/12

用自己的思路实现了对象数组去重。<br>
[去重](/code/homework06.html)

#### 2024/6/15

按照老师建议优化了选课时间冲突需求。
优化：
从静态的表格拿数据 -> 使用数据动态地生成表格并运算。<br>
[避免选课时间冲突2.0](/code/homework04-modified2.0.html)

#### 2024/6/16

按照老师建议优化了选课时间冲突需求。
优化：
1. 使用数据动态生成表格 -> 使用数据动态生成部分表格数据（因为表头这些其实是不变的可以原本就有的，直接写在body就行）
  <br>
2. 使用html的生成语句生成html元素及添加类 -> 使用模板字符串生成html元素（极大地简化了代码，可读性大大加强）<br>
[避免选课时间冲突3.0](/code/homework04-modified3.0.html)

   改了一下数据和复选框的绑定顺序。<br>
[避免选课时间冲突3.1](/code/homework04-modified3.1.html)

#### 2024/6/18

按照老师建议优化了选课时间冲突需求。
优化：
1. 监听事件开始前就记录下所有的冲突课程 -> 运用缓存。一边监听事件一边记录缓存（若缓存内无数据则加入缓存，若有则直接调用数据）（减小空间储存）

2. 优化部分冗余代码<br>
[避免选课时间冲突4.0](/code/homework04-modified4.0.html)

#### 2024/6/20

按照老师的建议以及提供的答案优化选课时间冲突需求。
优化：
使用二维数组记录缓存 -> 使用map记录缓存。（减小储存空间）
[避免选课时间冲突5.0](/code/homework04-modified5.0.html)














