---
title: 勘探线图业务梳理
date: 2020-08-03 11:04:35
categories: 文档
tags: 三维地测系统
mathjax: ture
# password: password
---

### 准备工作
* 确认勘探线钻孔是否正确，根据实际情况增减
![](15954861594451.jpg)

* 设置孔斜计算方法
![](15954865397352.jpg) 
 
*  提取勘探线
![](15954891120479.jpg)


>  1.数据选择流程
![勘探线剖面图1](%E5%8B%98%E6%8E%A2%E7%BA%BF%E5%89%96%E9%9D%A2%E5%9B%BE1.jpg)

> 2.数据来源
> 3.钻孔排序方式
> 4.图形参数
>> 网格`最大值` `最小值`可以输入也可以读取钻孔实际数据

* 设置`小柱状`参数，可以选择是否进行绘制
![](15954896503435.jpg)

* 剖面设置
![](15954897637198.jpg)
> 1.孔口坐标
> 2.地形图坐标,需要导入地形图数据文件
> <details>
> <summary>剖面信息注意事项</summary>
> ```
钻孔在勘探线上的投影设置需要确认用途
现有数据库生成剖面图出错，未弹出下一级窗口
```
> </details>

* 图签设置
![](15954884275257.jpg)

* 准备工作绘制内容及效果图
> <details>
> <summary>准备工作涉及信息</summary>
> ```
钻孔
网格
断层资料
小柱状
```
> </details>

![](15954902630890.jpg)

### 绘制地层
![](15954907036104.jpg)
![](15954938680134.jpg)



* 交互式绘制坡面地层
> * 绘制方式
    通常选择逐层绘制，方便编辑地层
> * 交互式选择
> * 地层间距
    `参考地层`与`待绘制地层`之间的距离
> *  地层厚度

* 编辑剖面地层
> 需要显示修改状态
> <details>
> <summary>编辑详细设置</summary>
> ```
加点
删除点
移点
修改厚度
统改厚度
截断
设置左侧关联
设置右侧关联
取消左侧关联
取消右侧关联
```
> </details>

![](15954947569777.jpg)
