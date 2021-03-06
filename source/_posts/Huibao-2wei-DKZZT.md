---
title: 二维出图项目阶段性成果汇报_2020年07月30日
date: 2020-07-30 09:36:41
categories: 汇报
tags: 三维地测系统
mathjax: ture
password: password2
---

### 汇报内容
* 阶段性工作总结与后期规划
* 单孔柱状图自动成图演示
* 单孔柱状图前后台联动演示

### 单孔柱状图完成功能
* 绘制单孔柱状图表头图框
* 绘制单孔柱状图属性图框
> 钻孔基本信息
> 钻孔地层信息
> 综合采用成果信息
> 测井成果信息
> 钻探成果信息

* 通过数据接口动态选择钻孔数据
> 用户权限认证
> 矿井信息选择
> 钻孔信息选择

* 前后胎联动生成单孔柱状图
* 通过设置比例尺参数绘制单孔柱状图
* 绘制简单单孔柱状图模版

### 单孔柱状图未完成功能
* 完善菜单操作
* 完善参数设置功能
* 单孔柱状图表尾信息绘制
* 单孔柱状图图签功能绘制
* 钻孔结构封孔情况信息绘制
* 简易水文绘制
* 测井曲线信息绘制
* 接口数据优化
* 人机操作流程优化

### 单孔柱状图自动成图演示
* 命令行输入命令：`NETLOAD`
* 加载动态链接库文件：`ZuanKongZhuZhuangTu.dll`
> ![](15960714644587.jpg)


* 信任开发者
> ![](15960733387336.jpg)
* 输入绘制命令：`DKZZT`
* 设置绘制选项
> ![](15960733612942.jpg)
![](15960733096140.jpg)


* 单孔柱状图效果图
> ![](15960722455737.jpg)

### 单孔柱状图前后台联动演示
* 数据库后台地址：[http://192.168.1.234:8080/](http://192.168.1.234:8080/)

> 用户名：Admin
> 密码：123456

* 选择编辑钻孔
> ![](15960726121414.jpg)

* 重新生成新的`单孔柱状图`