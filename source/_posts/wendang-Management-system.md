---
title: 生产技术信息管理系统分析
date: 2021-07-08 19:17:05
categories: 文档
tags: 三维地测系统
password: password2
---


### 各子系统权重分析

| 功能模块 | 权重占比(%) |
|:-----------:|:----:|
| 全空间地测协同系统 | 35 |
| 供电协同系统    | 10 |
| 通风协同系统    | 10 |
| 采掘协同系统    | 10 |
| 供排水协同系统   | 5  |
| 辅助运输协同系统  | 5  |
| 主运输协同系统   | 5  |
| 应急救援协同系统  | 5  |
| 人员定位协同系统  | 5  |
| 通讯联络协同系统  | 5  |
| 机电管理协同系统  | 5  |


### 各子系统权重分析

{% echarts 400 '100%' %}

{
    title: {
        text: "生产技术信息管理系统",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: true
            },
            dataView: {
                show: true,
                readOnly: true
            },
            restore: {
                show: true
            },
            saveAsImage: {
                show: true
            }
        }
    },
    calculable: true,
    series: [
        {
            name: "权重",
            type: "pie",
            radius: [30, 90],
            center: ["50%", "50%"],
            roseType: "area",
            data: [
                {
                    value: 35,
                    name: "全空间地测协同系统"
                },
                {
                    value: 10,
                    name: "供电协同系统"
                },
                {
                    value: 10,
                    name: "通风协同系统"
                },
                {
                    value: 10,
                    name: "采掘协同系统"
                },
                {
                    value: 5,
                    name: "供排水协同系统"
                },
                {
                    value: 5,
                    name: "辅助运输协同系统"
                },
                {
                    value: 5,
                    name: "主运输协同系统"
                },
                {
                    value: 5,
                    name: "应急救援协同系统"
                },
                {
                    value: 5,
                    name: "人员定位协同系统"
                },
                {
                    value: 5,
                    name: "通讯联络协同系统"
                },
                {
                    value: 5,
                    name: "机电管理协同系统"
                }
            ]
        }
    ]
}
{% endecharts %}
