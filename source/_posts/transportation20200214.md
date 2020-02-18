---
title: 辅助运输20200216
date: 2020-02-16 18:04:20
updated: 2020-02-16 18:04:20
categories: 计划任务
tags: 辅助运输
# password: ruihua123
---

### 服务端
**母玉峰**
* 测试用车申请推送服务
* 电话中心服务增加多账户支持

### 车载终端APP
**花雷 左俊**
* 电话中心服务增加多账户支持
* 测试行车记录功能

#### 用车申请APP
**左俊**
* 用车申请APP首页图片从服务端获取

### 报表统计 （孙虎）
* 用车申请APP首页图片从服务端获取
* 测试APP软件更新
> * 更新文字
> * 更新路径
* 车辆出入井时长统计
> 可选所有种类的车辆： 默认`三吨料车`
> 可选时间范围：默认范围过去4个自然周
> 对比精度：`月` `周` 默认精度`周`
> 最小范围4周
> 饼壮图显示全部比例情况
> 交互操作如下图示例
> 测试数据至少2个月以上
> 颜色可以随机显示
> 可以下载保存图片

{% echarts 400 '100%' %}
{
    title: {
        text: "3吨料车",
        subtext: "",
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
                show: false
            },
            dataView: {
                show: false,
                readOnly: true
            },
            restore: {
                show: false
            },
            saveAsImage: {
                show: true
            }
        }
    },
    calculable: true,
    series: [
        {
            name: "",
            type: "pie",
            radius: "55%",
            center: ["50%", "60%"],
            data: [
                {
                    value: 248,
                    name: "少于30分钟"
                },
                {
                    value: 672,
                    name: "大于30分钟小于一小时"
                },
                {
                    value: 1723,
                    name: "大于1小时小于1.5小时"
                },
                {
                    value: 1861,
                    name: "大于1.5小时小于2小时"
                },
                {
                    value: 1440,
                    name: "大于2小时小于2.5小时"
                },
                {
                    value: 996,
                    name: "大于2.5小时小于3小时"
                },
                {
                    value: 736,
                    name: "大于3小时小于3.5小时"
                },
                {
                    value: 567,
                    name: "大于3.5小时小于4小时"
                },
                {
                    value: 2111,
                    name: "大于4小时小于8小时"
                },
                {
                    value: 305,
                    name: "大于8小时"
                }
            ]
        }
    ]
}
{% endecharts %}



{% echarts 400 '100%' %}
{
    title: {
        text: "三吨料车",

    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["9月", "10月", "11月", "12月"]
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: false
            },
            dataView: {
                show: false,
                readOnly: true
            },
            magicType: {
                show: false,
                type: ["line", "bar"]
            },
            restore: {
                show: false
            },
            saveAsImage: {
                show: true
            }
        }
    },
    calculable: true,
    xAxis: [
        {
            type: "category",
            boundaryGap: false,
            data: ["少于30分钟", "大于30分钟小于一小时", "大于1小时小于1.5小时", "大于1.5小时小于2小时", "大于2小时小于2.5小时", "大于2.5小时小于3小时", "大于3小时小于3.5小时", "大于3.5小时小于4小时", "大于4小时小于8小时", "大于8小时"]
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "次"
        }
    ],
    series: [
        {
            name: "9月",
            type: "line",
            data: [61, 191, 437, 377, 337, 277, 206, 170, 680, 108]
        },
        {
            name: "10月",
            type: "line",
            data: [66, 234, 644, 882, 568, 326, 193, 140, 370, 26]
        },
        {
            type: "line",
            name: "11月",
            data: [84, 135, 393, 351, 339, 246, 205, 164, 688, 109]
        },
        {
            type: "line",
            name: "12月",
            data: [37, 112, 249, 251, 196, 147, 132, 93, 373, 62]
        }
    ]
}
{% endecharts %}
