---
title: 产品经理用例图简析
date: 2021-08-19 14:56:00
categories: 文档
tags: 产品经理
password: product
---

### 基础信息
* UML建模语言：Unified Modeling Language（UML)又称作统一建模语言或标准建模语言。
> * 静态模型（系统结构）
用例图、类图、对象图、构件图、部署图
> * 动态模型（系统行为）
状态图、活动图、序列图、协作图
* 用例图：由参与者（Actor)、用例（Use Case)、边界（Use Case Subject）以及他们之间的关系构成的用于描述系统功能的视图。
* 主要关系：泛化（ganeralization）、包含（include）、扩展（extend）、依赖（Dependency)、关联（ssociasion）。
* 应用场景：项目初期确认需求阶段，产品销售阶段。

### 绘制用例图
![3781629216596_.pic_hd](16293556715768.jpg)

* 所有关系之间要满足说话的要素：`谁` `做` `什么事`。
* 重点理解`条件执行`的逻辑关系。
* 包含、扩展、泛化这三点的理解
> * 条件性：泛化中的子用例和include中的被包含的用例会无条件发生，而extend中的延伸用例的发生是由条件的；
> * 直接性：泛化中的子用例和extend中的延伸用例，是可以为参与者提供直接服务的，但include就不能提供直接服务，只能提供间接服务；
> * 对扩展而言：延伸的用例并不包含基础用例的内容，基础用例也不包含延伸用例的内容；
> * 而对于泛化而言：子用例包含基础用例的所有内容及其和其他用例或者参与者之间的关系。

### 推荐软件
* Microsoft Visio （Windows OS）
* StarUML （Windows OS， MAC OS）
* <font color="red">OmniGraffle（MAC OS）</font>
* 印象笔记（Markdown）
* 语雀（Markdown）
* <font color="red">MWeb（Markdown）</font>

### 参考文档
* [UML文档](https://docs.staruml.io/)
* [MARKDOWN文档](https://guides.github.com/features/mastering-markdown/)