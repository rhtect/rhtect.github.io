---
title: 低代码开发工具探索
date: 2022-10-09 19:02:27
categories: 汇报
tags: 生产技术管理
mathjax: ture
password: password2
---


### 低代码实现维度
* 数据
* 功能
* 表单
* 权限
* 组织

### 低代码工具介绍
| 序号 | 名称 | 网站 |
|:----:|:----:|:----:|
| 1    |    thingjs-x  |  https://x.thingjs.com/txo/products/apiDocument    |
| 2    |    简道云 |   https://www.jiandaoyun.com/?utm_src=bdpz   |
| 3    |    ivx  |   https://www.ivx.cn/   |
| 4    |   DWF |   http://i-g6slw29a.cloud.nelbds.org.cn:8180/dwf/modeler-web    |
| 5   |   form-create-designer  |   https://github.com/xaboy/form-create-designer   |

### 低代码工具优缺点

#### 产品优势
对代码水平没有要求

* **框架类：**
· 3D开发工具和3D模型库
· 基于WebGL技术
· 提供Javascript的3D Library
· 支持在线和离线开发
· 支持PC和移动设备
* **技术类：**
· 可动态设置模型（修改模型属性，可设置自定义ID、名称、尺寸、位置等）
· 支持的文件格式包括 .fbx, .obj, .3ds, .stl, .dae, .3d, .3mf 
· 自动吸附功能（放置摄像机时，可点击自动吸附来开启此功能）
* **业务类：**
· 在3D可视化应用中， 对接物联网或业务数据 ，实时驱动3D场景动态变化或图表数据更新
* **部署类：**
开发完成的项目，可选择 在线部署 在云服务器，或 离线部署 到自己的服务器上

#### 产品缺点

*  支持业务相对简单，对复杂业务不友好。
*  出现问题解决难度较大。
*  目前看来没有提供一些基础建模软件的插件，比如3dsmax的模型导出插件，虽然说提供一些读3ds格式，fbx格式的场景。要配合更多扩展库完成，可能会需要联网通信功能的封装、声音普通控制甚至高级频谱控制、输入设备信息的处理等诸多渲染以外的功能，加载速度慢、缺少碰撞检测等功能。


### 目前自己的设计思路
![](16653132411486.jpg)
