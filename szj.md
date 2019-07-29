# 1.jQuery基础

## 第01章-属性和样式操作

1. .attr 设置元素属性

2. :ep左右

##  第02章-事件绑定

1.  
    ```js

    $("selector").click(function(){
        //事件触发执行的代码
    })鼠标点击事件

    ```

2. this代表$里的元素

3. 
    ```js

    $("#").mouseenter(function(){
			$(this).find("#").slideDown(500); 注释：鼠标滑到效果
    }).mouseleave(function(){
			$(this).find("#").slideUp(500); 注释：鼠标离开效果
    })
    
    ```

## 第03章-动画效果

1. 

    ```
    show 显示

    hide 隐藏

    slideUp 上下隐藏

    slideDown 上下显示

    fadeOut 逐渐透明

    fadeIn 逐渐出来

    addClass添加class

    removeClass删除class

    ```

#  2.JavaScript基础

## 第02章：变量与数据类型

|类型名称 |值|说明|
|---------|------|----------------|
|数值     |100;3.14  |不管是整数还是小数，都是数值型。|
|字符串   |"hello";"100"  |双引号或单引号中的值是字符串。|
|布尔     |true;false  |布尔值只有两个值，代表真和假。|
|空       |null|空值只有null，后续讲解。|
|未定义   |undefined  |未定义值只有undefined，后续讲解|
|对象     |{}  |后续讲解|

## 第03章：表达式与运算符

|运算符|操作|类型|
|------|----|--------|
|>|大于|num,num=>bool|
|>=|大于等于|num,num=>bool|
|<|小于|num,num=>bool|
|<=|小于等于|num,num=>bool|
|==|判断相等|any,any=>bool|
|!=|判断不等|any,any=>bool|
|===|判断恒等|any,any=>bool|
|!==|判断非恒等|any,any=>bool|

|运算符|操作|类型|
|------|----|--------|
|=|赋值|any,any=>any|
|+=|加并赋值|any,any=>any|
|-=|减并赋值|any,any=>any|
|*=|乘并赋值|any,any=>any|
|/=|除并赋值|any,any=>any|

## 第5章：循环语句

###  一、for语句
for语句的语法如下：
``` js
for(初始值;布尔值;计数器){
    //语句块
}
```
在for语句中，如果布尔值是true,就会一直执行语句块中的内容，为了防止死循环，需要有一个计数器，当数值达到指定值，布尔值就会变成false，循环便停止了，下面的示例代码使用for循环输出0~9九个数字（demo01.html）

``` js
for(var i = 0;i<10;i++){  
    // i的初始值是0
    // 判断i是否小于10，如果小于10则执行花括号中的代码
    // 每次执行完花括号中的代码后，i的值加1
    console.log(i);
}
```

上面的代码通过判断，实现当i的值为6的时候，跳过本次循环，直接接入下一次循环。下面我们使用continue来实现计算100以内所有不能被7整除的正整数加和（demo06.html）
``` js
var sum = 0;
for(var i = 0;i<=100;i++){
    if(i%7===0){
        continue;
    }
    sum += i;
}
console.log(sum);
```

for语句 continue跳过 break出现设定数值是结束循环
while语句

## 第6章.函数基础

###  一、函数的基本概念

``` js
function fun(){   //定义函数,函数名为fun
    //函数体
}
fun();            //调用函数
```

```js
        function a(num1,sign,num2){
            var eas = 0;
            switch(sign){
                case "+":eas =  num1 + num2;break;
                case "-":eas =  num1 - num2;break;
                case "*":eas =  num1 * num2;break;
                case "/":eas =  num1 / num2;break;
                default:console.log("请输入正确的操作符")
            }
            return eas;
        }
        console.log(a(10,"-",20));

```

##  第08章：数组

#### 一、数组的基本概念

 length它可以获取数组元素的个数

 我们可以使用push方法想数组中追加元素

``` js

var friends = ["小明","小亮"];
friends.push("小红");
console.log(friends);   //输出["小明","小亮","小红"];

```

## 第09章：实践课

### 一、弹出框方法

* alert是最简单的弹出框，我们在之前的课程中使用过，它可以向用户显示一条消息，并等待用户关闭对话框（demo01.html）。
``` js
alert("hello world");
```

* confirm也会向用户显示一条消息，但是用户可以通过点击“确定”或“取消”按钮，并返回一个布尔值。
``` js
var result = confirm("点确定返回true,点取消返回false");
console.log(result);   //点击不同按钮，控制台输出结果不同
```

* prompt也可以像用户显示一条消息，等待用户输入字符串后，返回这个字符串，如果用户点击取消，则返回null。
``` js

var result = prompt("请输入你的名字：")
console.log(result); 

```

 Number只能输入数值