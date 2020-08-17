# JavaScript

[TOC]

*笔记参考https://www.bilibili.com/video/BV1JJ41177di*

## 简介

### 简述

- 脚本语言



## 快速入门

### 引入js

1. 内部标签

```java
<script>
    alert("Hello World!")
</script>
```

2. 外部引入

```javascript
<script src="js/js.js"></script>
```

完整样例：

```javascript
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Title</title>

        <!-- 内部标签使用-->
    <!--    <script>-->
    <!--        alert("Hello World!")-->
    <!--    </script>-->

        <!-- 外部引入 -->
        <!-- 注意：尽量不要使用半闭合标签 -->
        <script src="js/js.js"></script>

        <!-- 不用显示定义type，也默认是javascript -->
        <script type="text/javascript">
            // ......注释
        </script>
    </head>
    <body>

    </body>
</html>
```

### 基本语法入门

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8">
        <title>Title</title>

    	<!-- JavaScript严格区分大小写 -->
        <script>
            // 定义变量 var
            var score = 1;
            // 条件控制
            if (score > 60 && score < 70){
                alert("及格")
            }else if (score > 90) {
                alert("优秀")
            }

            // console.log()在浏览器的控制台打印

        </script>

    </head>
    <body>

    </body>
</html>
```

### 数据类型

1. **number** --JS不区分浮点数和整数

```javas
123 // 整数123
123.1 // 浮点数
1.123e# // 科学计数法
-99 // 复数
NaN // not a number
Infinity // 无限大
```

2. **字符串**

‘abc'  "abc"

2. **布尔值**

true  false

3. **逻辑运算**

```javascript
&&
||
|     // 真即假，假即真
```

4. **比较运算**

```javascript
=
==  // 等于，类型不一样，值一样。结果为true
=== // 绝对等于，类型一样，值一样，结果为true
```

5. **null和undefined**

   - null：空
   - undefined：未定义

6. **数组**

   - JS中的数组中不必是相同类型的元素

   ```javascript
   var arr = [1, 2, 3, 4, 5, 'hello', null, true]
   new Array(1,2,3,4,5,'hello')
   ```

   ​	去数组下标，越界时为undefined。

7. **对象**

   - 数组是[]，对象是{}

   ```javascript
   var person = {
       name: "zhangsan",
       age: 18,
       tags: ['js', 'java']
   }
   ```

   去对象的值

   ```javascript
   person.name
   ```

8. 须知

   - NaN===NaN。这个与所有的数值都不相等，包括自己。
   - 只能通过isNaN()方法来确认这个数是否为NaN
   - 尽量避免使用浮点数进行运算，存在精度问题。



###  严格检查模式

```javascript
<script>
    // 严格检查模式，预防JavaScript的随意性导致产生的一些问题。必须写在第一行。
    'use strict'
	// 建议用let声明局部变量，用var也可
	let i = 1
</script>
```



## 数据类型

### 字符串

