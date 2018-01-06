---
layout: archive
title:  "Response Web design book notes"
date:   2017-12-22 23:45:15 +0800
categories: posts  rwd
Tages: rwd
header:
 teaser: /assets//images/dala.jpg
---
#响应式Web设计读书笔记


##1 HTML5、CSS3及响应式设计

1.1. 响应式网页设计的定义
> 响应式网页设计这个术语是将三种已有的开发技巧（弹性网格布局、弹性图片、媒体和媒体查询）整合起来并命名为响应式网页设计，这个术语还有一堆其他相同意思的叫法，如流式设计、弹性布局、塑料布局、流体设计、自适应布局、跨设备设计以及弹性设计。真正的响应式设计方法 不仅仅只是根据视口大小改变网页布局，相反，它是要从整体上颠覆当前设计网页的方法，以往我们先是针对桌面电脑进行固定宽度设计，然后将其缩小并针对小屏幕进行内容重排；现在我们应该首先针对小屏幕进行设计，然后逐步增强针对大屏幕的设计和内容。

1.2 视口和屏幕尺寸

> 视口和屏幕尺寸不是同一个概念。视口是指浏览器窗口内的内容区域，不包含工具栏、标签栏等，也就是网页实际显示的区域。屏幕尺寸指的是设备的物理显示区域。需要注意的是有些浏览器调整工具显示的尺寸包含浏览器的其他元素，诸如地址栏、标签栏和搜索栏，而有些工具则不是这样。 

##2. 媒体查询：支持不同的视口 

2.1 媒体查询的语法：

```body{
    background-color:grey;
}
@media screen and (max-width:960px){
    body{
        background-color:red;
    }
}
@media screen and (max-width:768px){
    body{
        background-color:orange;
    }
}
@media screen and (max-width:550px){
    body{
        background-color:yellow;
    }
}
@media screen and (max-width:320px){
    body{
        background-color:green;
    }
}
```
##3. 流式布局

3.1 将固定像素宽度转换为对应的百分比宽度依照如下公式：

> 目标元素宽度/上下文元素宽度=百分比宽度

将固定像素宽度元素转换为百分比之后还需要将文字的固定像素大小转换为等量的相对尺寸，用em代替px。em的实际大小是相对于其上下文的字体大小而言的，所以上述公式同样适用文字固定像素宽度的转换，值得注意的是，现代浏览器的默认文字大小都是16像素。
##4. CSS3中创建阴影

4.1 文字阴影

CSS中添加如下代码后：
> text-shadow:.039em .039em 0em #dad7d7;

4.2 盒阴影

盒阴影的语法与文字阴影完全一样：水平偏移距离、垂直偏移距离、模糊半径，以及阴影颜色。但是，盒阴影的跨浏览器支持并不好，所以明智的做法是使用浏览器私有前缀，例如：
> webkit-box-shadow:0px 3px 5px #444;
-moz-box-shadow:0px 3px 5px #444;
-o-box-shadow:0px 3px 5px #444;
-ms-box-shadow:0px 3px 5px #444;
-khtml-box-shadow:0px 3px 5px #444;
box-shadow:0px 3px 5px #444;


4.3 背景渐变

给网站的侧边栏制作一个背景渐变效果，只需要添加如下代码：

> background: linear-gradient(90deg,#fff 0,#e4e4e4 50%,#fff 100%);


4.4 径向背景渐变

CSS3背景渐变不只局限于线性渐变，制作径向渐变同样简单。径向渐变是从一个中心点开始，依据椭圆形或者圆形进行扩张渐变。

径向背景渐变语法如下：

> background: -webkit-radial-gradient(center,ellipse cover,#fff 72%,#ddd 100%);