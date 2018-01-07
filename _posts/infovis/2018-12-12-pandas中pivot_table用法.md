---

layout: archive
title:  "pandas中pivot_table用法(一文看懂透视表pivot_table 首先读取数据，作为一个老火密，本文将火箭队当家吉祥物詹姆斯·哈登本赛季比赛数据作为数据集进行讲解)"
date:   2017-12-30 23:45:15 +0800
header:
 teaser: /assets//images/data.jpg
categories: posts infovis
tags: infovis

---
# Pandas | 一文看懂透视表pivot_table
## 首先读取数据，作为一个老火密，本文将火箭队当家吉祥物詹姆斯·哈登本赛季比赛数据作为数据集进行讲解

 
``` 
import pandas as pd
import numpy as np
df = pd.read_csv('h:/James_Harden.csv',encoding='utf8')
df.tail()
```


## ![最后五场数据](https://pic1.zhimg.com/50/v2-817850ef525ad668fc829d0d0d88de4b_hd.jpg)

pivot_table有四个最重要的参数index、values、columns、aggfunc，本文以这四个参数为中心讲解pivot操作是如何进行。

## Index

每个pivot_table必须拥有一个index，如果想查看哈登对阵每个队伍的得分，首先我们将对手设置为index：
```
pd.pivot_table(df,index=[u'对手'])
```

![](https://pic2.zhimg.com/50/v2-a277a701440852c5be4adb3c7345fc3a_hd.jpg)

对手成为了第一层索引，还想看看对阵同一对手在不同主客场下的数据，试着将对手与胜负与主客场都设置为index
```
pd.pivot_table(df,index=[u'对手',u'主客场'])
```
试着交换下它们的顺序，数据结果一样：
```
pd.pivot_table(df,index=[u'主客场',u'对手'])
```
![](https://pic1.zhimg.com/50/v2-6a02ed68a0b3fc6a7a25c3602ae0dba0_hd.jpg)

看完上面几个操作，Index就是层次字段，要通过透视表获取什么信息就按照相应的顺序设置字段，所以在进行pivot之前你也需要足够了解你的数据。
## Values
通过上面的操作，我们获取了james harden在对阵对手时的所有数据，而Values可以对需要的计算数据进行筛选，如果我们只需要james harden在主客场和不同胜负情况下的得分、篮板与助攻三项数据：
```
pd.pivot_table(df,index=[u'主客场',u'胜负'],values=[u'得分',u'助攻',u'篮板'])
```
![](https://pic2.zhimg.com/50/v2-6cfdd067b4c7c88920ae24a12425c003_hd.jpg)


## Aggfunc
aggfunc参数可以设置我们对数据聚合时进行的函数操作。

当我们未设置aggfunc时，它默认aggfunc='mean'计算均值。我们还想要获得james harden在主客场和不同胜负情况下的总得分、总篮板、总助攻时：
```
pd.pivot_table(df,index=[u'主客场',u'胜负'],values=[u'得分',u'助攻',u'篮板'],aggfunc=[np.sum,np.mean])
```
![](https://pic4.zhimg.com/50/v2-07bac1cb5c39073dab544aeec454be13_hd.jpg)

## Columns
Columns类似Index可以设置列层次字段，它不是一个必要参数，作为一种分割数据的可选方式。
```
#fill_value填充空值,margins=True进行汇总
pd.pivot_table(df,index=[u'主客场'],columns=[u'对手'],values=[u'得分'],aggfunc=[np.sum],fill_value=0,margins=1)
```
![](https://pic3.zhimg.com/50/v2-0fc4ac949c58fd3fef7b228dd9e08dbf_hd.jpg)

```
table=pd.pivot_table(df,index=[u'对手',u'胜负'],columns=[u'主客场'],values=[u'得分',u'助攻',u'篮板'],aggfunc=[np.mean],fill_value=0)
```
![](https://pic4.zhimg.com/50/v2-c114dd7e0184dd0cf6e5e2216cfeb49a_hd.jpg)

## pivot_table vs. groupby
目前还在学习用法，有待补充.....未完待续。
