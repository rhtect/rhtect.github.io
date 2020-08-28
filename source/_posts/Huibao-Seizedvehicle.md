---
title: 矿井车辆使用时长报告
date: 2020-07-24 14:16:59
categories: 汇报
tags: 辅助运输
---
x
{% echarts 400 '100%' %}
{
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["2小时", "4小时", "8小时", "超时"]
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
                type: ["line", "bar", "stack", "tiled"]
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
            data: ["3吨料车", "3吨料车(小)", "5吨加长平板", "5吨平板", "5吨翻斗"]
        }
    ],
    yAxis: [
        {
            type: "value"
        }
    ],
    series: [
        {
            type: "line",
            itemStyle: {
                normal: {
                    areaStyle: {
                        type: "default"
                    }
                }
            },
            name: "2小时",
            data: [2330, 129, 96, 1268, 380]
        },
        {
            type: "line",
            itemStyle: {
                normal: {
                    areaStyle: {
                        type: "default"
                    }
                }
            },
            name: "4小时",
            data: [952, 54, 6, 219, 39]
        },
        {
            type: "line",
            itemStyle: {
                normal: {
                    areaStyle: {
                        type: "default"
                    }
                }
            },
            name: "8小时",
            data: [3868, 237, 12, 315, 76]
        },
        {
            type: "line",
            itemStyle: {
                normal: {
                    areaStyle: {
                        type: "default"
                    }
                }
            },
            name: "超时",
            data: [550, 34, 4, 31, 13]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2020年1月-2020年6月
* 对比车型：`3吨料车` `3吨料车(小)` `5吨加长平板` `5吨平板` `5吨翻斗`
* 对比时长段：`0-2小时` `2-4小时` `4-8小时` `超过8小时`
* 数据结论
> 各种车型大部分一次出入井时长可以控制在8小时内
> 各种车型均存在一次出入井时长超过8小时的情况

### 车辆出入井时长月度对比
![车辆出入井时长月度对比](15955836646320.jpg)
* `3吨料车`：`8小时`与`超过8小时`任务占比相对稳定，曲线变化幅度不大。
* `3吨料车(小)`：`8小时` `超过8小时`与`4小时`任务占比相对稳定，曲线变化幅度不大。
* `5吨翻斗`：`8小时`与`超过8小时`任务占比相对稳定，曲线变化幅度不大。
* `5吨平板`：`8小时`与`超过8小时`任务占比相对稳定，曲线变化幅度不大。

### 各种车型出入井时长占比

![出入井时长对比](15955799703118.jpg)
* `3吨料车`：超过4小时占比超过`50%`, 超过8小时占比达到`4.81%`。
* `3吨料车(小)`：超过4小时占比超过`54%`, 超过8小时占比达到`5.46%`。
* `5吨加长平板`：超过4小时占比超过`17%`, 超过8小时占比达到`5.88%`。
* `5吨平板`：超过4小时占比超过`19%`, 超过8小时占比达到`1.17%`。
* `5吨翻斗`：超过4小时占比超过`21%`, 超过8小时占比达到`2.75%`。

### 项目部申请车型占比
![项目部占比](15955798280001.jpg)

* `3吨料车`：前5名的用车单位9月-12月占比超过82%。
* `3吨料车(小)`：掘进八区机掘18队占比为63.65%，前5名的用车单位9月-12月占比超过90%。
* `5吨翻斗`：综采预备队占比为36.19%；前5名的用车单位9月-12月占比超过96%；9月-12月一共只有9个项目部申请5顿翻斗。
* `5吨平板`：5吨平板执行的任务类型不确定；项目部使用5吨平板次数比较随机。

### 车型分类详情
#### 3吨料车
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
    legend: {
        orient: "vertical",
        x: "left",
        data: ["2小时", "4小时", "8小时", "超时"]
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
            name: "3吨料车",
            type: "pie",
            radius: "55%",
            center: ["50%", "60%"],
            itemStyle: {
                normal: {
                    label: {
                        show: true,
                        formatter: "{b}: {c} ({d}%)"
                    }
                }
            },
            data: [
                {
                    value: 503,
                    name: "2小时"
                },
                {
                    value: 143,
                    name: "4小时"
                },
                {
                    value: 502,
                    name: "8小时"
                },
                {
                    value: 58,
                    name: "超时"
                }
            ]
        }
    ]
}
{% endecharts %}


#### 3吨料车(小)

{% echarts 400 '100%' %}
{
    title: {
        text: "3吨料车(小)",
        subtext: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "left",
        data: ["2小时", "4小时", "8小时", "超时"]
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
            name: "3吨料车(小)",
            type: "pie",
            radius: "55%",
            center: ["50%", "60%"],
            itemStyle: {
                normal: {
                    label: {
                        show: true,
                        formatter: "{b}: {c} ({d}%)"
                    }
                }
            },
            data: [
                {
                    value: 16,
                    name: "2小时"
                },
                {
                    value: 9,
                    name: "4小时"
                },
                {
                    value: 27,
                    name: "8小时"
                },
                {
                    value: 3,
                    name: "超时"
                }
            ]
        }
    ]
}
{% endecharts %}


#### 5吨加长平板

{% echarts 400 '100%' %}
{
    title: {
        text: "5吨加长平板",
        subtext: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "left",
        data: ["2小时", "4小时", "8小时", "超时"]
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
            name: "5吨加长平板",
            type: "pie",
            radius: "55%",
            center: ["50%", "60%"],
            itemStyle: {
                normal: {
                    label: {
                        show: true,
                        formatter: "{b}: {c} ({d}%)"
                    }
                }
            },
            data: [
                {
                    value: 13,
                    name: "2小时"
                },
                {
                    value: 1,
                    name: "4小时"
                },
                {
                    value: 2,
                    name: "8小时"
                },
                {
                    value: 1,
                    name: "超时"
                }
            ]
        }
    ]
}

{% endecharts %}

#### 5吨平板

{% echarts 400 '100%' %}
{
    title: {
        text: "5吨平板",
        subtext: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "left",
        data: ["2小时", "4小时", "8小时", "超时"]
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
            name: "5吨平板",
            type: "pie",
            radius: "55%",
            center: ["50%", "60%"],
            itemStyle: {
                normal: {
                    label: {
                        show: true,
                        formatter: "{b}: {c} ({d}%)"
                    }
                }
            },
            data: [
                {
                    value: 298,
                    name: "2小时"
                },
                {
                    value: 47,
                    name: "4小时"
                },
                {
                    value: 78,
                    name: "8小时"
                },
                {
                    value: 5,
                    name: "超时"
                }
            ]
        }
    ]
}

{% endecharts %}

#### 5吨翻斗

{% echarts 400 '100%' %}
{
    title: {
        text: "5吨翻斗",
        subtext: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "left",
        data: ["2小时", "4小时", "8小时", "超时"]
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
            name: "5吨翻斗",
            type: "pie",
            radius: "55%",
            center: ["50%", "60%"],
            itemStyle: {
                normal: {
                    label: {
                        show: true,
                        formatter: "{b}: {c} ({d}%)"
                    }
                }
            },
            data: [
                {
                    value: 76,
                    name: "2小时"
                },
                {
                    value: 10,
                    name: "4小时"
                },
                {
                    value: 20,
                    name: "8小时"
                },
                {
                    value: 3,
                    name: "超时"
                }
            ]
        }
    ]
}

{% endecharts %}

### 车辆出入井时长月度详情

#### 3吨料车
{% echarts 350 '80%' %}
{
    title: {
        text: "",
        subtext: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["2小时", "4小时", "8小时", "超时"]
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
            data: ["一月", "二月", "三月", "四月", "五月", "六月"]
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "°C"
        }
    ],
    series: [
        {
            type: "line",
            name: "2小时",
            data: [388, 305, 348, 382, 403, 503]
        },
        {
            type: "line",
            name: "4小时",
            data: [166, 144, 175, 162, 155, 143]
        },
        {
            type: "line",
            name: "8小时",
            data: [629, 625, 757, 693, 617, 502]
        },
        {
            type: "line",
            name: "超时",
            data: [95, 115, 124, 93, 57, 58]
        }
    ]
}
{% endecharts %}
#### 3吨料车（小）
{% echarts 350 '80%' %}
{
    title: {
        text: "",
        subtext: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["2小时", "4小时", "8小时", "超时"]
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
            data: ["一月", "二月", "三月", "四月", "五月", "六月"]
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "°C"
        }
    ],
    series: [
        {
            type: "line",
            name: "2小时",
            data: [27, 14, 27, 22, 23, 16]
        },
        {
            type: "line",
            name: "4小时",
            data: [7, 10, 5, 13, 9, 9]
        },
        {
            type: "line",
            name: "8小时",
            data: [42, 48, 44, 41, 34, 27]
        },
        {
            type: "line",
            name: "超时",
            data: [11, 4, 7, 7, 2, 3]
        }
    ]
}
{% endecharts %}
#### 5吨平板
{% echarts 350 '80%' %}
{
    title: {
        text: "",
        subtext: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["2小时", "4小时", "8小时", "超时"]
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
            data: ["一月", "二月", "三月", "四月", "五月", "六月"]
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "°C"
        }
    ],
    series: [
        {
            type: "line",
            name: "2小时",
            data: [149, 152, 204, 212, 252, 298]
        },
        {
            type: "line",
            name: "4小时",
            data: [32, 29, 51, 30, 30, 47]
        },
        {
            type: "line",
            name: "8小时",
            data: [47, 39, 69, 39, 43, 78]
        },
        {
            type: "line",
            name: "超时",
            data: [2, 4, 5, 11, 3, 5]
        }
    ]
}
{% endecharts %}

#### 5吨翻斗
{% echarts 350 '80%' %}
{
    title: {
        text: "",
        subtext: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["2小时", "4小时", "8小时", "超时"]
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
            data: ["一月", "二月", "三月", "四月", "五月", "六月"]
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "°C"
        }
    ],
    series: [
        {
            type: "line",
            name: "2小时",
            data: [58, 43, 57, 73, 73, 76]
        },
        {
            type: "line",
            name: "4小时",
            data: [3, 2, 10, 8, 6, 10]
        },
        {
            type: "line",
            name: "8小时",
            data: [9, 9, 16, 8, 14, 20]
        },
        {
            type: "line",
            name: "超时",
            data: [3, 2, 0, 3, 2, 3]
        }
    ]
}
{% endecharts %}

