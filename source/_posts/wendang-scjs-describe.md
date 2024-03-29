---
title: 生产技术管理系统功能梳理
date: 2021-08-31 09:28:47
categories: 文档
tags: 生产技术管理
# password: management
---

### 协同设计模块架构

<!--more-->
![生产管理系统功能结构2](16303365546879.jpg)


### 信息描述
| 功能模块  |  技术难点 | N模块复用 | 地测知识 | 可外包程度 |
|:---:|:---|:---:|:---:|:---:|
|  系统图  | 1.WEB端管理后台; 2.有C端功能; 3.业务要求高; 4.涉及核心算法。 | 低 | 不需要 | 低 |
|  解算报告  | 1.WEB端解算功能; 2.生成WORD报告; 3.业务要求极高; 4.涉及核心算法。 | 低 | 不需要 | 底 |
|  设备布置图  | 1.WEB端管理功能; 2.有C端功能; 3.业务要求高; 4.涉及核心算法。 | 中（出图逻辑一致） | 需要采掘工程平面图基础 | 中 |
|  台账管理  | 1.WEB端增删改查操作（N个模块高复用）; 2. 无C端功能; 3.不涉及核心数据; 4.不涉及核心算法。 | 高  | 不需要 | 高 |

### 系统架构效果图
![首页-新](%E9%A6%96%E9%A1%B5-%E6%96%B0.png)
![首页-新1](%E9%A6%96%E9%A1%B5-%E6%96%B01.png)
![首页-新2](%E9%A6%96%E9%A1%B5-%E6%96%B02.png)
![地质测量](%E5%9C%B0%E8%B4%A8%E6%B5%8B%E9%87%8F.png)

![生产管理](%E7%94%9F%E4%BA%A7%E7%AE%A1%E7%90%86.png)
![大数据](%E5%A4%A7%E6%95%B0%E6%8D%AE.png)

### 资源分配图
![](16357376935371.jpg)

### 功能模块结构拓扑图
![](16357391224726.jpg)


### 系统里程碑

| 名称  |  时间 | 说明 |
|:---:|:---|:---:|
|  供电协同设计  | 2021年12月23日 | 完成供电协同设计全部产品设计 |
|  通风协同设计  | 2022年1月28日 | 完成通风协同设计全部产品设计 |
|  供排水协同设计  | 2022年1月28日 | 完成供排水协同设计全部产品设计 |
|  采掘协同设计  | 2021年1月24日 | 完成采掘协同设计全部产品设计 |

#### 通风协同设计

| 通风协同设计  |  时间 | 说明 |
|:---:|:---|:---:|
|  通风台帐管理  | 2021年11月17日 | 设备台账、运行台账 |
|  通风设备布置图  | 2021年12月2日 | 后台管理，前端显示 |
|  通风系统图  | 2022年1月18日 | 后台管理，前端显示 |
|  通风解算报告  | 2021年1月28日 | 导出通风解算报告 |

#### 供电协同设计

| 供电协调设计  |  时间 | 说明 |
|:---:|:---|:---:|
|  供电设备布置图  | 2021年11月23日 | 后台管理，前端显示 |
|  供电系统图  | 2021年12月8日 | 后台管理，前端显示 |
|  供电台帐管理  | 2021年12月23日 | 设备台账、运行台账|
|  供电整定计算报告  | 2021年12月23日 | 导出供电整定计算报告 |

#### 供排水协同设计

| 供排水协同设计  |  时间 | 说明 |
|:---:|:---|:---:|
|  供排水台帐管理  | 2022年1月10日 | 设备台账、运行台账|
|  供排水解算报告  | 2022年1月18日 | 导出供排水解算报告 |
|  供排水系统图  | 2022年1月28日 | 后台管理，前端显示 |

#### 采掘协同设计
| 采掘协同设计  |  时间 | 说明 |
|:---:|:---|:---:|
|  采掘系统图  | 2022年1月20日 | 后台管理，前端显示|
|  采掘台帐管理  | 2022年1月24日 | 设备台账、运行台账|