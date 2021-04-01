---
title: 清华瑞华辅助设计平台授权系统
date: 2021-03-03 10:59:35
categories: 文档
tags: 清华瑞华CAD
password: trcad
---

## 数据结构
### 字段说明
* `Short Serial No.`：映射激活码，命名规则TRCAD-20210303-xxxxxx
* `Service Term`：授权时间`0.代表终身授权`
* `License Type`：授权方式`1.正式版` `2.试用版`
* `Sales Status`：销售方式`1.已销售` `0.未销售`
* `Activation Status`：激活状态`1.已激活` `0.未激活`
* `Enterprise`：使用企业
* `Platform`：平台版本`1.标准版` `2.平台版`
* `Apply  IP`：申请激活码使用的IP地址
* `Apply  MAC`：申请激活码使用的MAC地址

# 清华瑞华辅助设计平台授权系统
## 数据结构
### 字段说明
* `Short Serial No.`：映射激活码，命名规则TRCAD-20210303-xxxxxx
* `Service Term`：授权时间`0.代表终身授权`
* `License Type`：授权方式`1.正式版` `2.试用版`
* `Sales Status`：销售方式`1.已销售` `0.未销售`
* `Activation Status`：激活状态`1.已激活` `0.未激活`
* `Enterprise`：使用企业
* `Platform`：平台版本`1.标准版` `2.平台版`
* `Apply  IP`：申请激活码使用的IP地址
* `Apply  MAC`：申请激活码使用的MAC地址

## 产品功能
* 登录
> 标题使用`华瑞华辅助设计平台授权系统`
![2611614758320_.pic_hd](2611614758320_.pic_hd.jpg)

* 导入激活码
* 分类查询已使用激活码
> 授权时间
> 授权方式
> 使用企业
> 平台版本

* 分类查询未使用激活码
> 授权时间
> 平台版本

* 根据匹配码（hort Serial No.）查询激活码
* 根据激活码查询使用情况
> 生成时间
> 激活时间
> 激活状态
> 授权时间
> 平台版本
> 使用企业
> 记录的IP地址
> 记录的mac地址

* 激活码状态管理：`未使用` `已领用` `已激活`
> `领用操作` <--> `归还操作`
> `激活操作` <--> `注销操作`
![SN1](SN1.jpg)