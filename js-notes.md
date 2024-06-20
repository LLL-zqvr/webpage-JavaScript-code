### 如何定位指定元素
getElementById：根据ID，获取的是一个元素

getElementsByClassName：根据class属性查找元素，返回的是数组

getElementsByTagName：根据标签名查找元素，返回的是数组

getElementsByName：根据name属性查找元素，返回的是数组

### 如何自建HTML元素属性并用jquery取得属性值
自建：data-*="属性"；
如：<input type="checkbox" data-courseid="course.id">;
jquery取得该值：
如：const courseId = $(this).data("courseid");
