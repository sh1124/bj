# 1.jQuery基础

## 第01章-属性和样式操作

1. .attr 设置元素属性

2. :ep左右

##  第02章-事件绑定

1.  $("selector").click(function(){
        //事件触发执行的代码
    })鼠标点击事件
    
2. this代表$里的元素

3. 
    ```html

    $("#").mouseenter(function(){
			$(this).find("#").slideDown(500); 注释：鼠标滑到效果
    }).mouseleave(function(){
			$(this).find("#").slideUp(500); 注释：鼠标离开效果
    })
    
    ```

# 第03章-动画效果

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