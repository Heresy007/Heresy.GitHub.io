---
layout: archive


title:  "_posts上传中出现index of问题解决方法汇总"


date:   2017-12-29 23:45:15 +0800
header:
 teaser: /assets//images/kezaisheng.jpg

categories: posts  rwd

tags: jekyll
---

#在上传本地md文件时候，可能会出现如下情况

![问题](https://github.com/Heresy007/Heresy007.github.io/blob/master/images/index.png?raw=true)

> 解决方法1（粗暴、不优雅）

进入本地的navigation.yml目录下.原目录如下：![如下](https://github.com/Heresy007/Heresy007.github.io/blob/master/images/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20180101222610.png?raw=true)

修改后：![如下](https://github.com/Heresy007/Heresy007.github.io/blob/master/images/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20180101222552.png?raw=true)
> 解决方法2（优雅、官方解决方法）

使用archive方法，把navigation.yml目录下 layout的default更改为 ![archive](https://github.com/Heresy007/Heresy007.github.io/blob/master/images/%E5%BE%AE%E4%BF%A1%E6%88%AA%E5%9B%BE_20180101225343.png?raw=true)
![archive](https://github.com/Heresy007/Heresy007.github.io/blob/master/images/Y6X0R3U@VVNWUV~PD108%7D88.png?raw=true)

即指定增加一个目录名称，给网页一个详细的指引
> 解决方法3

若在文章posts问题中，遇到乱码问题可参考林树斌同学的中文乱码解决![方法](https://treeice.github.io/posts/jekyll/JekyllChineseName/)

但是依然会存在文章乱码情况，增加tags标签、Categories（类别）可解决情况。


![图片](https://github.com/Heresy007/Heresy007.github.io/blob/master/images/tags.png?raw=true)

tags：是一种更为灵活、有趣的文章或图片等信息的分类方式。用户可以为每篇文章、每张图片或每条信息添加一个或多个标签（tags），从而根据这些标签把这些文章、图片或信息进行分类。

Categories（类别）：每一个HTML元素都必须遵循定义了它可以包含哪一类内容的规则。 这些规则被归类为几个常见的元素内容模型（content model）


关于这篇心得有一些话想说:
文章引用了：（https://zhidao.baidu.com/question/12681503.html）的部分内容。本文章主要针对出现index of（文章不出现内容只出现类似列表的情况）提出了三种解决方法，但是经实测，采用老师的方法二和方法三稳妥。
