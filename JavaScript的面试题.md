##### JavaScript的面试题

###### 1.JavaScript中的强制转型是什么？

答：强制转型在JavaScript 中分为显式和隐式。

比如将字符串类型转换为number类型，那么将一个字符串赋值给变量a之后，采用Number(a)赋值给b进行转换，输出b为number类型而不是字符串类型，这种方式为显式；如果将a变量乘以一个数字1之后赋值给变量b，那么输出b为number类型，此方式为隐式。

###### 2.JavaScript中的作用域(scope)是指什么？

答：在js中每个函数都有自己的作用域 ，作用域是变量以及通过名称访问这些变量的规则的集合，同一个作用域中的变量名必须是唯一的，一个作用域可以嵌套在另一个作用域内，如果一个作用域嵌套在另一个作用域内最内部作用域的代码可以访问另一个作用域的变量。

###### 3.解释JavaScript中的相等性。

答：有严格比较和抽象比较。

严格比较(===)在不允许强制类型转型的情况下检查两个值是否相等

抽象比较(==)在允许强制转型的情况下检查两个值是否相等

###### 4.解释什么是回调函数，并提供一个简单的例子。

答：回调函数是一个可以做为参数传递给另一个函数的函数，并在某些操作完成后执行。下面是一个简单的回调函数的例子。

```
	function modifyArray(arr,callback){
        // 对arr做一些操作
        arr.push(100);
        // 执行传进来的callback函数
        callback()
    }
    var arr = [1,2,3,4,5];
    modifyArray(arr,function(){
        console.log("array has been modifyed",arr)
    })
```

###### 5."use strict"的作用是什么？

答：use strict 一般写在函数的顶部或代码的顶部，可以帮助我们写出更安全的js代码。例如，如果我们错误的创建了全局变量，它会通过抛出错误的方式来警告我们

```
	// 错误的示范
    function doSomething(val){
        "use strict";
        x = val + 10
    }
    //因为x没有被定义，并且使用了全局作用域中的某个字对其进行赋值，use strict 不允许这样做，所以会抛出一个错误。
```

```
	// 正确的示范
    function doSomething(val){
        "use strict";
        var x = val + 10
    }
```

######  6.解释JavaScript中的null和undefined。

答：

###### 7.什么是JavaScript？

答：JavaScript是客户端和服务器端的脚本语言(node)，同时也是面向对象的编程语言。它可以插入到HTML页面中，是目前较热门的web开发语言。

###### 8.列举Java和JavaScript之间的区别？

答：Java是一门十分完整，成熟的编程语言。相比之下，JavaScript是一个可以被引入HTML页面的编程语言。这两种语言并不完全依赖，而是针对不同的意图而设计的。Java是一种面向对象的结构化编程语言，而JavaScript是客户端脚本语言，被称为非结构化编程语言。

###### 9.JavaScript和ASP脚本相比，哪个更快？

答：JavaScript更快，JavaScript是一种客户端语言，因此它不需要web服务器的协助来执行。而ASP是服务器端语言，因此总是比JavaScript慢。值得注意的是，JavaScript现在也可用于服务器端语言(node.js)

###### 10.什么是负无穷大？

答：负无穷大是JavaScript中的一个数字，可以通过将负数除以0来得到。

###### 11.如何将JavaScript代码分解成几行？ (new)

答：在字符串语句中可以在第一行末尾处使用反斜杠"\"来完成

例：document.write("This is \a program");

如果不是在字符串语句中更改为新行，那么js会忽略行中的断点。

###### 12.什么是未声明和未定义变量？(important)

答：***未声明的变量是程序中不存在且未声明的变量***，如果程序尝试读取未声明变量的值，则会遇到运行时错误。

***未定义的变量是在程序中声明但尚未给出任何值的变量***，如果程序尝试读取未定义变量的值，则返回未定义的值。

###### 13.如何编写可*动态添加新元素*的代码？

答：

```
<html>
    <head>
        <meta charset="UTF-8">
        <title>动态添加新元素</title>
        <script type="text/javascript">
            function addNode(){
                var newP = document.createElement("p");
                var textNode = document.createTextNode("this is a new text node");
                newP.appendChild(textNode);
                document.getElementById("firstP").appendChild(newP)
            }
        </script>
    </head>
    <body>
        <p id="firstP">firstP</p>
    </body>
</html>
```

###### 14.什么是全局变量？这些变量如何声明？使用全局变量有哪些问题？

答：全局变量是整个代码长度都可用的变量，这些变量没有任何的作用域。使用全局变量所面临的问题是本地和局部变量名称的冲突。此外，很难调试和测试依赖于全局变量的代码。

###### 15.解释js中的定时器是怎么工作的？

答：定时器用于在设定的时间执行一段代码，或者在给定的时间间隔内重复执行一段代码。例如**setTimeOut**,**setInterval**,**clearInterval**

###### 16.如何使用js提交表单？

document.form[0].submit();

###### 17.元素的样式和类如何改变？

document.getElementById("#id").style.font-size="20";

document.getElementById("#id").className="anyclass"

###### 18.delete操作符的功能是什么？

答：用于删除程序中的所有变量或对象，但不能删除使用**var**关键字声明的变量。

###### 19.  3+2+“7”的结果是什么？

答：3和2 是整数，可以直接相加，由于7是字符串，它将会被直接连接

###### 20.原生js给一个元素绑定click事件(三种实现方法)

![image-20210919134435472](C:\Users\lzm\AppData\Roaming\Typora\typora-user-images\image-20210919134435472.png)

![image-20210919134456106](C:\Users\lzm\AppData\Roaming\Typora\typora-user-images\image-20210919134456106.png)

![image-20210919134514222](C:\Users\lzm\AppData\Roaming\Typora\typora-user-images\image-20210919134514222.png)

###### 21.void函数

void函数是js中的一个函数，它会接收一个参数，返回值永远是undefined。也就是说，使用void目的就是为了得到js中的undefined。

###### 22. void(0)怎么用？

答：用于防止页面刷新，并在调用时传递参数"0"

###### 23.在js中Cookie是什么？

答：Cookie是用来存储计算机中的小型测试文件，当用户访问网站以存储他们需要的信息是，它将被创建。

###### 24.shift，pop，unshift，push

![image-20210919174704035](C:\Users\lzm\AppData\Roaming\Typora\typora-user-images\image-20210919174704035.png)















