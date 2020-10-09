---
title: 山西省智能化矿山现场会-辅助运输分析动态图
date: 2020-10-03 11:07:36
categories: 汇报
tags: 辅助运输
password: password
---

###  用车申请分析统计

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["申请数次", "实际次数"],
        x: "center",
        y: "bottom"
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: false
            },
            dataView: {
                show: false,
                readOnly: false
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
            axisLine: {
                onZero: false
            },
            data: ["2019年9月", "2019年10月", "2019年11月", "2019年12月", "2020年1月", "2020年2月", "2020年3月", "2020年4月", "2020年5月", "2020年6月", "2020年7月", "2020年8月", "2020年9月"]
        }
    ],
    grid: {
        y: 70
    },
    yAxis: [
        {
            type: "value",
            name: "次",
            axisLine: {
                show: true
            }
        }
    ],
    series: [
        {
            type: "bar",
            name: "申请数次",
            data: [2567, 2609, 2777, 3155, 2477, 2493, 2920, 2311, 2557, 2657, 2864, 2950, 2902],
            yAxisIndex: 0,
            barWidth: 20
        },
        {
            type: "line",
            name: "实际次数",
            data: [1738, 2257, 2268, 2985, 2727, 2533, 3366, 3437, 3709, 4290, 3907, 4248, 4573],
            yAxisIndex: 0
        }
    ]
}
{% endecharts %}

###  物料运输车有效工作分布情况



#### 全年分布情况

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis",
        showDelay: 0,
        axisPointer: {
            type: "cross",
            lineStyle: {
                type: "dashed",
                width: 1
            }
        }
    },
    legend: {
        data: ["3吨料车", "5吨加长平板", "5吨平板", "5吨翻斗"],
        x: "center",
        y: "bottom"
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: false
            },
            dataZoom: {
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
    xAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "次",
            nameLocation: "end"
        }
    ],
    yAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "公里"
        }
    ],
    series: [
        {
            type: "scatter",
            name: "3吨料车",
            data: [[564, 18102.71], [55, 777.85], [497, 16177.23], [337, 8418.51], [895, 21076.15], [74, 2638.82], [73, 1056.04], [192, 2779.09], [14, 1023.56], [478, 12251.95], [741, 13706.56], [476, 12629.71], [80, 3583.16], [850, 14995.75], [291, 4336.29], [184, 3165.74], [252, 4892.68], [191, 2196.42], [473, 8592.12], [847, 16642.83], [596, 14563.54], [725, 14099.72], [463, 14205.27], [234, 10608.45], [71, 2082.59], [387, 9774.15], [94, 3999.96], [875, 22521.98], [645, 17274.87], [251, 13328.21], [117, 2079.29], [823, 12281.92], [1294, 19070.41], [89, 2027.05], [732, 12953.85], [844, 14087.98], [67, 1426.06], [715, 9783.3], [858, 13067.92], [758, 11428.08], [913, 14572.55], [433, 15757.55], [546, 12053.25], [753, 21954.78], [413, 14714.56], [630, 19903.46], [383, 11516.68], [417, 12311.93], [747, 17828.32], [787, 16824.65], [444, 16450.27], [742, 12762.71], [115, 1259.56], [512, 15978.28], [663, 17900.71], [50, 807.29], [114, 3976.31], [589, 18333.95], [317, 12705.79], [531, 11551.95], [486, 9157.9], [778, 12512.93]]
        },
        {
            type: "scatter",
            name: "5吨加长平板",
            data: [[324, 5569.89], [11, 288.8]]
        },
        {
            type: "scatter",
            name: "5吨平板",
            data: [[909, 13125.67], [850, 13527.23], [368, 5960.17], [115, 2120.4], [622, 9878.54], [235, 3961.15], [575, 8725.73], [624, 9486.02], [100, 3063.21], [369, 6659.52], [158, 3399.2], [330, 5543.01], [297, 4615.9], [320, 6836.22], [259, 4170.4], [252, 4328.45], [446, 8685.71], [540, 7317.81], [114, 2175.99], [386, 6146.91], [439, 7110.26]]
        },
        {
            type: "scatter",
            name: "5吨翻斗",
            data: [[171, 3377.29], [367, 6277.99], [660, 9492.39], [438, 6347.8], [607, 9060.99], [203, 3635.1], [554, 8487.94]],
            itemStyle: {
                normal: {
                    color: "#1DBB37"
                }
            }
        }
    ]
}
{% endecharts %}

#### 2020年5月分布情况

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis",
        showDelay: 0,
        axisPointer: {
            type: "cross",
            lineStyle: {
                type: "dashed",
                width: 1
            }
        }
    },
    legend: {
        data: ["3吨料车", "5吨加长平板", "5吨平板", "5吨翻斗"],
        x: "center",
        y: "bottom"
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: false
            },
            dataZoom: {
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
    xAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "次",
            nameLocation: "end"
        }
    ],
    yAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "公里"
        }
    ],
    series: [
        {
            type: "scatter",
            name: "3吨料车",
            data: [[55, 1320.33], [0, 0], [51, 1589.81], [21, 484.08], [67, 1236.15], [23, 474.77], [0, 0], [0, 0], [0, 0], [53, 1161.3], [65, 1113.4], [64, 1298.84], [0, 0], [80, 1486.4], [12, 212.84], [13, 285.76], [19, 402.75], [0, 0], [45, 951.56], [73, 1144.73], [68, 1282.06], [44, 870.97], [47, 944.45], [58, 1306.65], [0, 0], [47, 852.75], [0, 0], [80, 1770.73], [31, 1044.81], [0, 0], [0, 0], [75, 1628.45], [83, 1706.28], [7, 87.95], [64, 1115.01], [88, 1500.02], [0, 0], [63, 1234.32], [64, 1250.97], [63, 1451.68], [94, 2007.7], [55, 1330.56], [62, 1459.68], [68, 1510.69], [49, 1130.27], [65, 1329.04], [13, 300.15], [66, 1515.08], [51, 1367.39], [58, 1288.64], [76, 1735.25], [71, 1208.37], [0, 0], [28, 678.39], [54, 1411.92], [0, 0], [0, 0], [56, 1501.89], [52, 1399.24], [68, 1406.3], [52, 1106.06], [44, 920.48]]
        },
        {
            type: "scatter",
            name: "5吨加长平板",
            data: [[34, 728.86], [0, 0]]
        },
        {
            type: "scatter",
            name: "5吨平板",
            data: [[70, 1128.69], [78, 1270.24], [74, 1254.35], [0, 0], [74, 1584.08], [45, 690.45], [33, 862.99], [55, 1124.68], [0, 0], [27, 537.02], [33, 611.08], [33, 572.85], [11, 154.39], [31, 623.54], [0, 0], [0, 0], [50, 1106.01], [59, 933.92], [0, 0], [31, 707.59], [33, 669.88]]
        },
        {
            type: "scatter",
            name: "5吨翻斗",
            data: [[0, 0], [48, 950.24], [50, 874.79], [31, 614.39], [35, 648.68], [49, 912.79], [43, 743.47]],
            itemStyle: {
                normal: {
                    color: "#1DBB37"
                }
            }
        }
    ]
}
{% endecharts %}

#### 2020年6月分布情况

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis",
        showDelay: 0,
        axisPointer: {
            type: "cross",
            lineStyle: {
                type: "dashed",
                width: 1
            }
        }
    },
    legend: {
        data: ["3吨料车", "5吨加长平板", "5吨平板", "5吨翻斗"],
        x: "center",
        y: "bottom"
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: false
            },
            dataZoom: {
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
    xAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "次",
            nameLocation: "end"
        }
    ],
    yAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "公里"
        }
    ],
    series: [
        {
            type: "scatter",
            name: "3吨料车",
            data: [[61, 1492.17], [0, 0], [77, 2589.99], [13, 269.69], [61, 1702], [17, 447.78], [0, 0], [0, 0], [0, 0], [71, 2635.12], [66, 1511.35], [66, 1947.49], [0, 0], [59, 1693.05], [33, 767.47], [18, 274.94], [19, 405.09], [0, 0], [58, 845.26], [74, 1840.72], [76, 1515.39], [46, 917.47], [38, 1162.67], [39, 1648.85], [0, 0], [57, 1386.61], [0, 0], [88, 2831.41], [51, 2029.04], [70, 2573.78], [0, 0], [47, 847.4], [86, 1549.76], [16, 776.01], [78, 1975.34], [106, 1744.23], [0, 0], [46, 938.46], [92, 1872.81], [69, 1276.56], [82, 1749.66], [57, 2159.09], [64, 2283.19], [91, 2669.63], [28, 934.49], [76, 2242.77], [45, 1148.93], [69, 2207.4], [59, 1641.66], [52, 1932.16], [62, 2298.29], [81, 1334.04], [0, 0], [28, 1219.6], [65, 1791.33], [22, 460.21], [0, 0], [30, 860.49], [73, 3306.19], [59, 2161.86], [35, 817.14], [39, 835.51]]
        },
        {
            type: "scatter",
            name: "5吨加长平板",
            data: [[29, 423.18], [0, 0]]
        },
        {
            type: "scatter",
            name: "5吨平板",
            data: [[96, 1697.77], [99, 1792.1], [90, 1387.44], [0, 0], [91, 1385.44], [63, 1120.06], [52, 918.18], [75, 1312.94], [0, 0], [57, 1281.9], [33, 610.99], [47, 901.71], [34, 669.43], [39, 959.73], [49, 805.4], [53, 702.28], [28, 766.17], [54, 907.86], [5, 115.37], [34, 702.53], [42, 894.94]]
        },
        {
            type: "scatter",
            name: "5吨翻斗",
            data: [[13, 242.69], [40, 764.22], [63, 1231.76], [49, 934.06], [63, 1189.15], [30, 798.82], [57, 865.92]],
            itemStyle: {
                normal: {
                    color: "#1DBB37"
                }
            }
        }
    ]
}
{% endecharts %}

#### 2020年7月分布情况

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis",
        showDelay: 0,
        axisPointer: {
            type: "cross",
            lineStyle: {
                type: "dashed",
                width: 1
            }
        }
    },
    legend: {
        data: ["3吨料车", "5吨加长平板", "5吨平板", "5吨翻斗"],
        x: "center",
        y: "bottom"
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: false
            },
            dataZoom: {
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
    xAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "次",
            nameLocation: "end"
        }
    ],
    yAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "公里"
        }
    ],
    series: [
        {
            type: "scatter",
            name: "3吨料车",
            data: [[41, 1351.29], [0, 0], [68, 2007.79], [33, 484.46], [61, 3148.89], [0, 0], [0, 0], [0, 0], [0, 0], [64, 2515.86], [52, 1318.34], [53, 2301.07], [1, 0], [55, 1159.34], [42, 698.43], [31, 635.02], [35, 776.21], [0, 0], [79, 1657.98], [71, 2572.18], [81, 3041.59], [54, 1711.51], [45, 1534.08], [48, 3069.75], [0, 0], [51, 1687.29], [0, 0], [77, 2887.51], [20, 1118.3], [65, 3100.98], [0, 0], [62, 1368.65], [65, 1759.63], [5, 96.97], [75, 1551.34], [69, 1451.14], [12, 439.8], [35, 797.52], [81, 1533.3], [48, 986.69], [66, 1213.1], [63, 2450.48], [64, 2190.09], [60, 2193.6], [34, 1344.17], [63, 2266.3], [43, 1778.25], [50, 1661.12], [39, 1041.19], [56, 1860.53], [64, 2522.29], [54, 1118.44], [0, 0], [56, 1729.2], [71, 2810.16], [0, 0], [35, 1002.02], [33, 1174.1], [55, 2177.16], [43, 963.76], [69, 1034.62], [74, 1282.16]]
        },
        {
            type: "scatter",
            name: "5吨加长平板",
            data: [[38, 841.68], [0, 0]]
        },
        {
            type: "scatter",
            name: "5吨平板",
            data: [[52, 1110.48], [55, 1099.88], [73, 1100.43], [0, 0], [48, 1052.64], [36, 575.8], [37, 723.79], [39, 911.12], [34, 1015.92], [29, 972.35], [25, 380.74], [21, 563.32], [24, 635.85], [30, 469.34], [58, 1039.1], [58, 1239.74], [43, 1108.68], [52, 863.12], [14, 239.01], [37, 635.69], [42, 782.23]]
        },
        {
            type: "scatter",
            name: "5吨翻斗",
            data: [[59, 1322.88], [27, 679.59], [40, 807.31], [38, 738.88], [57, 1309.5], [50, 1042.73], [50, 1134.54]],
            itemStyle: {
                normal: {
                    color: "#1DBB37"
                }
            }
        }
    ]
}
{% endecharts %}

#### 2020年8月分布情况

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis",
        showDelay: 0,
        axisPointer: {
            type: "cross",
            lineStyle: {
                type: "dashed",
                width: 1
            }
        }
    },
    legend: {
        data: ["3吨料车", "5吨加长平板", "5吨平板", "5吨翻斗"],
        x: "center",
        y: "bottom"
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: false
            },
            dataZoom: {
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
    xAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "次",
            nameLocation: "end"
        }
    ],
    yAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "公里"
        }
    ],
    series: [
        {
            type: "scatter",
            name: "3吨料车",
            data: [[29, 1398.47], [0, 0], [59, 2310.45], [13, 243.63], [79, 2060.94], [0, 0], [0, 0], [0, 0], [0, 0], [41, 997.13], [49, 1367.96], [63, 1974.76], [24, 694.1], [65, 1359.38], [39, 645.44], [34, 388.9], [33, 566.55], [0, 0], [71, 1416.68], [74, 2255.44], [79, 1962.95], [48, 1775.6], [49, 1296.03], [41, 2041.03], [0, 0], [62, 1765.61], [59, 1913.77], [73, 2378.92], [39, 1809.99], [63, 1875.51], [5, 100.73], [68, 1460.91], [57, 1091], [10, 123.48], [98, 1691.04], [84, 1163.47], [33, 650.04], [51, 757.16], [59, 1094.35], [70, 1185.73], [75, 1717.49], [58, 1407.02], [48, 1010.29], [76, 2446.92], [36, 1043.24], [65, 2016.44], [48, 1464.9], [63, 2031.12], [44, 1023.26], [42, 1237.95], [67, 2940.19], [49, 1048.85], [0, 0], [72, 2615.35], [56, 937.1], [0, 0], [42, 1514.68], [22, 1292.77], [57, 1698.68], [69, 1073.01], [58, 754.83], [71, 1364.4]]
        },
        {
            type: "scatter",
            name: "5吨加长平板",
            data: [[26, 841.68], [0, 0]]
        },
        {
            type: "scatter",
            name: "5吨平板",
            data: [[70, 1528.49], [74, 1400.36], [54, 643.06], [53, 824.34], [63, 1035.11], [34, 503.51], [47, 899.58], [38, 797.49], [38, 1191.2], [38, 612.03], [13, 217.37], [27, 690.89], [25, 369.97], [32, 589.36], [72, 1068.38], [78, 1273.06], [48, 764.74], [53, 593.35], [53, 701.74], [42, 598.5], [34, 394.52]]
        },
        {
            type: "scatter",
            name: "5吨翻斗",
            data: [[47, 757.52], [49, 767.46], [52, 881.77], [73, 1199.13], [55, 914.39], [37, 358.24], [32, 661.15]],
            itemStyle: {
                normal: {
                    color: "#1DBB37"
                }
            }
        }
    ]
}
{% endecharts %}

#### 2020年9月分布情况

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis",
        showDelay: 0,
        axisPointer: {
            type: "cross",
            lineStyle: {
                type: "dashed",
                width: 1
            }
        }
    },
    legend: {
        data: ["3吨料车", "5吨加长平板", "5吨平板", "5吨翻斗"],
        x: "center",
        y: "bottom"
    },
    toolbox: {
        show: true,
        feature: {
            mark: {
                show: false
            },
            dataZoom: {
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
    xAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "次",
            nameLocation: "end"
        }
    ],
    yAxis: [
        {
            type: "value",
            power: 1,
            precision: 2,
            scale: true,
            name: "公里"
        }
    ],
    series: [
        {
            type: "scatter",
            name: "3吨料车",
            data: [[68, 3417.77], [0, 0], [74, 3206.97], [14, 317.23], [97, 3583.67], [19, 1079.53], [3, 53.08], [0, 0], [14, 1023.56], [0, 0], [25, 1007.17], [62, 1881.9], [55, 2889.06], [74, 2204.24], [51, 1113.14], [67, 1088.4], [43, 888.7], [0, 0], [61, 1132.16], [83, 2107.65], [55, 1893.73], [68, 2685.05], [79, 3818.77], [32, 2082.13], [0, 0], [66, 1751.1], [35, 2086.19], [80, 3273.53], [50, 2692.69], [53, 5777.94], [112, 1978.56], [119, 1965.8], [84, 1609.97], [12, 97.79], [128, 1983.97], [88, 1458.21], [22, 336.22], [72, 1316.4], [69, 1394.27], [64, 1031.12], [86, 1545.45], [79, 4245.84], [0, 77.91], [76, 3866.38], [47, 3471.52], [66, 3561.35], [3, 30.62], [96, 3364.23], [64, 2590.91], [34, 832.3], [76, 3928.71], [46, 1297.88], [0, 0], [90, 3995.18], [61, 2992.99], [0, 0], [37, 1459.61], [50, 3203.63], [66, 3728.01], [58, 842.95], [38, 680.92], [69, 1378.84]]
        },
        {
            type: "scatter",
            name: "5吨加长平板",
            data: [[32, 537.04], [11, 288.8]]
        },
        {
            type: "scatter",
            name: "5吨平板",
            data: [[74, 1508.13], [87, 1937.44], [73, 1539.2], [62, 1296.06], [66, 1070.31], [38, 858.63], [35, 894.18], [54, 1007.98], [28, 856.09], [27, 829.88], [14, 571.14], [15, 372.65], [9, 222.63], [18, 731.15], [80, 1257.52], [63, 1113.37], [43, 1052.67], [47, 858.47], [42, 1119.87], [43, 1011.5], [35, 924.27]]
        },
        {
            type: "scatter",
            name: "5吨翻斗",
            data: [[52, 1054.2], [41, 913.88], [52, 1173.19], [31, 644.72], [59, 1197.79], [8, 104.71], [55, 926.68]],
            itemStyle: {
                normal: {
                    color: "#1DBB37"
                }
            }
        }
    ]
}
{% endecharts %}

###  车辆类型统计分析
#### 车型数量占比

{% echarts 400 '100%' %}
{
    title: {
        text: "",
        subtext: "",
        sublink: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "right",
        data: ["3吨料车", "5吨平板", "5吨翻斗", "5吨加长平板"],
        y: "center"
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
            },
            magicType: {
                show: false
            }
        }
    },
    calculable: true,
    series: [
        {
            type: "pie",
            name: "数量占比",
            data: [
                {
                    value: 63,
                    name: "3吨料车"
                },
                {
                    value: 23,
                    name: "5吨平板"
                },
                {
                    value: 7,
                    name: "5吨翻斗"
                },
                {
                    value: 2,
                    name: "5吨加长平板"
                }
            ]
        }
    ]
}
{% endecharts %}


* 统计日期范围：`3吨料车` `5吨加长平板` `5吨平板` `5吨翻斗`
* 数据结论：
> `3吨料车`：`66.32%`
> `5吨加长平板`：`2.1%`
> `5吨平板`：`24.21%`
> `5吨翻斗`：`7.37%`

* 车型运力分析占比（暂时不用统计）
https://rhtect.github.io/2020/07/24/Huibao-Seizedvehicle/

###  能耗分析
* 暂时空着

###  里程分析
#### 车辆类型里程对比统计

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["3吨料车", "5吨平板", "5吨翻斗", "5吨加长平板"],
        x: "center",
        y: "bottom"
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
            data: ["201911", "201912", "202001", "202002", "202003", "202004", "202005", "202006", "202007", "202008", "202009"],
            name: "月"
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "公里"
        }
    ],
    series: [
        {
            type: "line",
            name: "3吨料车",
            data: [24257.01, 56927.87, 39389.08, 40329.53, 65337.65, 59568.76, 57435.04, 80305.88, 85223.15, 76165.56, 116808.05]
        },
        {
            type: "line",
            name: "5吨平板",
            data: [4394.85, 10149.04, 4899.36, 7778.88, 12129.74, 10472.21, 13831.76, 18932.24, 16519.23, 16697.05, 21033.14]
        },
        {
            type: "line",
            name: "5吨翻斗",
            data: [1225.06, 3940.4, 2395.66, 1952.07, 3839.88, 3965.19, 4744.36, 6026.62, 7035.43, 5539.66, 6015.17]
        },
        {
            type: "line",
            name: "5吨加长平板",
            data: [370.74, 755.16, 393.56, 370.03, 479.58, 375.41, 728.86, 423.18, 841.68, 294.65, 825.84]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2019年11月-2020年9月
* 对比车型：`3吨料车` `5吨加长平板` `5吨平板` `5吨翻斗`
* 对比数据：不同料车月度行驶里程数对比
* 数据结论
> 各种车型大部分一次出入井时长可以控制在8小时内
> 各种车型均存在一次出入井时长超过8小时的情况


#### 车辆类型行驶里程占比统计

{% echarts 400 '100%' %}
{
    title: {
        text: "",
        subtext: "",
        sublink: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "right",
        data: ["3吨料车", "5吨平板", "5吨翻斗", "5吨加长平板"],
        y: "center"
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
            },
            magicType: {
                show: false
            }
        }
    },
    calculable: true,
    series: [
        {
            type: "pie",
            name: "公里",
            data: [
                {
                    value: 701747.58,
                    name: "3吨料车"
                },
                {
                    value: 136837.5,
                    name: "5吨平板"
                },
                {
                    value: 46679.5,
                    name: "5吨翻斗"
                },
                {
                    value: 5858.69,
                    name: "5吨加长平板"
                }
            ],
            center: ["35%", "50%"],
            radius: [0, "69%"]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2019年11月-2020年9月
* 对比车型：`3吨料车` `5吨加长平板` `5吨平板` `5吨翻斗`
* 对比数据：不同料车月度行驶里程数对比
* 数据结论
> 各种车型大部分一次出入井时长可以控制在8小时内
> 各种车型均存在一次出入井时长超过8小时的情况

 
#### 执行车队里程对比统计

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["生产车队二队", "生产车队三队"],
        x: "center",
        y: "bottom"
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
            data: ["2019-11", "2019-12", "2020-01", "2020-02", "2020-03", "2020-04", "2020-05", "2020-06", "2020-07", "2020-08", "2020-09"],
            name: "月"
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "公里"
        }
    ],
    series: [
        {
            type: "line",
            name: "生产车队二队",
            data: [19282.71, 46063.28, 33690.29, 37113.42, 56022.38, 53166.8, 47598.65, 71450.88, 75746.03, 66946.88, 102909.64]
        },
        {
            type: "line",
            name: "生产车队三队",
            data: [10180.67, 23961.93, 12349.63, 10594.58, 21756.2, 18530.78, 25723.97, 30850.17, 30244.73, 28697.19, 36805.78]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2019年11月-2020年9月
* 对比车型：`生产车队二队`  `生产车队三队`
* 对比数据：不同车队月度行驶里程数对比
* 数据结论
> 各种车型大部分一次出入井时长可以控制在8小时内
> 各种车型均存在一次出入井时长超过8小时的情况

#### 执行车队里程占比统计

{% echarts 400 '100%' %}
{
    title: {
        text: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "right",
        data: ["生产车队二队", "生产车队三队", "其他项目部"],
        y: "center"
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
            type: "pie",
            name: "公里",
            data: [
                {
                    value: 609990.96,
                    name: "生产车队二队"
                },
                {
                    value: 249695.63,
                    name: "生产车队三队"
                },
                {
                    value: 31436.68,
                    name: "其他项目部"
                }
            ],
            center: ["38%", "50%"]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2019年11月-2020年9月
* 对比车型：`生产车队二队`  `生产车队三队` `其他项目部`
* 对比数据：不同车队月度行驶里程数占比
* 数据结论
* `生产车队二队`  `生产车队三队`每月有效里程数走势基本一致，车队任务分配强度在合理范围。
* 从2020年年初起，执行车队月度里程数稳定提升。

* 执行车队与里程数分析（月度）
{% echarts 400 '100%' %}
{% endecharts %}


### 工作时长分析

#### 执行车队工时对比统计

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["生产车队二队", "生产车队三队"],
        x: "center",
        y: "bottom"
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
            data: ["2019-11", "2019-12", "2020-01", "2020-02", "2020-03", "2020-04", "2020-05", "2020-06", "2020-07", "2020-08", "2020-09"],
            name: "月"
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "小时"
        }
    ],
    series: [
        {
            type: "line",
            name: "生产车队二队",
            data: [1928, 4398, 2491, 2927, 4588, 3926, 4252, 4426, 4633, 3897, 4740]
        },
        {
            type: "line",
            name: "生产车队三队",
            data: [904, 2199, 971, 847, 1963, 1592, 2209, 2562, 2470, 2305, 2789]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2019年11月-2020年9月
* 对比车型：`生产车队二队`  `生产车队三队`
* 对比数据：不同车队月度工时对比
* 数据结论
* `生产车队二队`  `生产车队三队`每月有效工时走势基本一致，车队任务分配强度在合理范围。
* 从2020年年初起，执行车队月度工作时长稳定提升。

#### 执行车队工时占比统计

{% echarts 400 '100%' %}
{
    title: {
        text: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "right",
        data: ["生产车队二队", "生产车队三队", "其他项目部"],
        y: "center"
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
            type: "pie",
            name: "公里",
            data: [
                {
                    value: 42206,
                    name: "生产车队二队"
                },
                {
                    value: 20811,
                    name: "生产车队三队"
                },
                {
                    value: 2531,
                    name: "其他项目部"
                }
            ],
            center: ["38%", "50%"]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2019年11月-2020年9月
* 对比车型：`生产车队二队`  `生产车队三队` `其他项目部`
* 对比数据：不同车队月度工时占比
* 数据结论
> 各种车型大部分一次出入井时长可以控制在8小时内
> 各种车型均存在一次出入井时长超过8小时的情况

* 车型与运行里程数分析（月度）
* 执行车队与里程数分析（月度）







#### 车辆类型工时对比统计

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["3吨料车", "5吨平板", "5吨翻斗", "5吨加长平板"],
        x: "center",
        y: "bottom"
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
            data: ["201911", "201912", "202001", "202002", "202003", "202004", "202005", "202006", "202007", "202008", "202009"],
            name: "月"
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "公里"
        }
    ],
    series: [
        {
            type: "line",
            name: "3吨料车",
            data: [2267, 5159, 2849, 3148, 5383, 4468, 5068, 5078, 5414, 4601, 5820]
        },
        {
            type: "line",
            name: "5吨加长平板",
            data: [40, 73, 35, 30, 47, 31, 64, 40, 77, 30, 68]
        },
        {
            type: "line",
            name: "5吨平板",
            data: [465, 1156, 467, 631, 1079, 845, 1198, 1627, 1349, 1391, 1549]
        },
        {
            type: "line",
            name: "5吨翻斗",
            data: [127, 371, 200, 148, 335, 345, 406, 513, 569, 484, 503]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2019年11月-2020年9月
* 对比车型：`3吨料车` `5吨加长平板` `5吨平板` `5吨翻斗`
* 对比数据：不同料车月度行驶里程数对比
* 数据结论
> 各种车型大部分一次出入井时长可以控制在8小时内
> 各种车型均存在一次出入井时长超过8小时的情况
* 统计日期范围：2019年11月-2020年9月
* 对比车型：`生产车队二队`  `生产车队三队`
* 对比数据：不同车队月度工时对比
* 数据结论
* `生产车队二队`  `生产车队三队`每月有效工时走势基本一致，车队任务分配强度在合理范围。
* 从2020年年初起，执行车队月度工作时长稳定提升。

#### 车辆类型工时占比统计

{% echarts 400 '100%' %}
{
    title: {
        text: "",
        subtext: "",
        sublink: "",
        x: "center"
    },
    tooltip: {
        trigger: "item",
        formatter: "{a} <br/>{b} : {c} ({d}%)"
    },
    legend: {
        orient: "vertical",
        x: "right",
        data: ["3吨料车", "5吨平板", "5吨翻斗", "5吨加长平板"],
        y: "center"
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
            },
            magicType: {
                show: false
            }
        }
    },
    calculable: true,
    series: [
        {
            type: "pie",
            name: "总计",
            data: [
                {
                    value: 2267,
                    name: "3吨料车"
                },
                {
                    value: 535,
                    name: "5吨加长平板"
                },
                {
                    value: 11757,
                    name: "5吨平板"
                },
                {
                    value: 4001,
                    name: "5吨翻斗"
                }
            ]
        }
    ]
}
{% endecharts %}

* 统计日期范围：2019年11月-2020年9月
* 对比车型：`3吨料车` `5吨加长平板` `5吨平板` `5吨翻斗`
* 对比数据：不同料车月度行驶里程数对比
* 数据结论
> 各种车型大部分一次出入井时长可以控制在8小时内
> 各种车型均存在一次出入井时长超过8小时的情况


###  效率分析
* 车型工作效率比例：里程数/时长 （月度）
{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["3吨料车", "5吨平板", "5吨翻斗", "5吨加长平板"],
        x: "center",
        y: "bottom"
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
            data: ["2019-11", "2019-12", "2020-01", "2020-02", "2020-03", "2020-04", "2020-05", "2020-06", "2020-07", "2020-08", "2020-09"],
            name: "月"
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "公里"
        }
    ],
    series: [
        {
            type: "line",
            name: "3吨料车",
            data: [18.45710476, 19.80132739, 26.210254, 23.11236185, 21.89264947, 27.10661359, 22.03945987, 30.33825964, 26.89217728, 28.07322409, 31.77011544]
        },
        {
            type: "line",
            name: "5吨加长平板",
            data: [9.2685, 10.34465753, 11.24457143, 12.33433333, 10.20382979, 12.11, 11.3884375, 10.5795, 10.93090909, 9.821666667, 12.14470588]
        },
        {
            type: "line",
            name: "5吨平板",
            data: [9.451290323, 8.779446367, 10.4911349, 12.32786054, 11.24164968, 12.39314793, 11.54570952, 11.63628765, 12.24553744, 12.00363048, 13.57852808]
        },
        {
            type: "line",
            name: "5吨翻斗",
            data: [9.646141732, 10.62102426, 11.9783, 13.18966216, 11.46232836, 11.49330435, 11.68561576, 11.74779727, 12.36455185, 11.44557851, 11.95858847]
        }
    ]
}
{% endecharts %}

* 执行车队工作效率比例：里程数/时长 （月度）

{% echarts 400 '100%' %}
{
    title: {
        text: ""
    },
    tooltip: {
        trigger: "axis"
    },
    legend: {
        data: ["3吨料车", "5吨平板", "5吨翻斗", "5吨加长平板"],
        x: "center",
        y: "bottom"
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
            data: ["2019-11", "2019-12", "2020-01", "2020-02", "2020-03", "2020-04", "2020-05", "2020-06", "2020-07", "2020-08", "2020-09"],
            name: "月"
        }
    ],
    yAxis: [
        {
            type: "value",
            name: "公里"
        }
    ],
    series: [
        {
            type: "line",
            name: "生产车队二队",
            data: [10, 10.47, 13.52, 12.68, 12.21, 13.54, 11.19, 16.14, 16.35, 17.18, 21.71]
        },
        {
            type: "line",
            name: "生产车队三队",
            data: [11.26, 10.9, 12.72, 12.51, 11.08, 11.64, 11.65, 12.04, 12.24, 12.45, 13.2]
        },
        {
            type: "line",
            name: "其他项目部",
            data: [11.71, 10.79, 11.66, 14.88, 13.68, 15.7, 12.43, 12.54, 11.86, 10.04, 12.08]
        }
    ]
}
{% endecharts %}

###  车次分析
* 用车申请次数（月度）
* 实际出井次数（月度）


{% echarts 400 '100%' %}

{% endecharts %}