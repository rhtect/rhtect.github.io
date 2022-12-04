---
title: 综合演示脚本
date: 2022-10-10 21:39:30
categories: 演示脚本
tags: 研发中心
mathjax: ture
password: password2
---
## 大数据底座

## 地质保障平台
### 成果概述
基于闻老师前面介绍的大数据中台架构，我们研发了地质保障系统。系统具有分子化、全要素、开放性特点，例如这里我们通过统一编码的方式，把地质保障当中的基础数据矿界、图例、水平、采区、工作面、巷道、井筒、硐室等等进行了分子化存储，接下来可以看到，我们利用这些分子化的数据能够自动生成采掘工程平面图等二维图件，能够自动生成工作面地质体等三维透明地质体，能够对整个工作面进行数字孪生，实现远程操控。
### 一键成图
首先，介绍一下我们的CAD辅助设计平台，这是我们联合清华共同研发的国产CAD平台，针对矿山地测业务，实现了采掘工程平面、充水性图、柱状图、剖面图、主要巷道图、主要保护煤柱图等等各类地测图件的一键生成。点击【1:5000采掘工程平面图】，可以看到左下角的数据加载进度条，系统正在处理大数据融合平台存储的分子化数据，使其能够自动绘制到图中。目前生成的1：5000采掘工程平面图是华电煤业不连沟煤矿。可以从图中看到各个工作面、巷道、断层等等分子化的数据，这些元素的绘制，我们依据的是国家标准规定的标准图例，这样也避免了人工手绘造成的不标准不规范情况发现。同时，因为这些数据进行了分子化存储，通过我们开放的标准接口，可以开放给安全生产技术管理系统、人员定位系统等其他系统使用，具有明显的开放性。
### 一键成体
介绍一下我们的三维地质建模系统，除了二维图的一键生成，我们同样实现了三维的数据驱动。点击【生成地质体】可以看到左下角进度条正在加载数据，视图里正在加载钻孔数据、断层数据等。基于这些分子化的基础数据，结合一些空间数据的插值算法，我们生成了地层曲面模型，然后是地质体模型。
通过三维模型的剖切功能，我们可以透明化的掌握前方未采区域的地质情况，结合采煤情况，实现每进一刀，煤层赋存情况、断层等复杂构造的情况，进而为工作面的安全生产提供解决方案，给出可采线，顶板线，底板线，断层落差等数据。
### 数字孪生，远程操控
介绍一下我们的采煤控制系统，利用大数据融合平台集成的各类分子化传感器数据，结合地质保障系统生成的地质体，构建了数字孪生采煤工作面场景。可以对工作面地质情况进行漫游，看到上层的顶板情况，下层的底板等起伏变化情况，中间闪红的是断层构造，左右两侧是进风和回风巷，采煤机会沿着这个方向进刀来回割煤。这是华电煤业不连沟矿的6220工作面，煤层厚度最高21.6米，采用的是放顶煤生产工艺。
这是系统跟机状态，可以看到采煤机正在割煤，以及液压支架的推拉架动作。可以对远程采煤机进行远程操控，例如控制采煤机右摇臂的升降。
打开三视图，上面是上下两巷道的剖面图，下面视图放大，上部分是顶视图，可以看到每天的回采米数，采煤机、刮板机、液压支架、转载机等三机移架动作情况，每采一刀后，各支架是否拉直情况等。下部分是前视图，可以看到当前煤层的顶板线、底板线，以及系统给出的橘红色可采线，还有采煤机的截割线，通过不断揭露的数据，修正地质体模型，进而用来动态规划采煤机的截割，可以实现采煤机的记忆截割到智能截割的转变。
打开视频预览，可以结合现场视频和三维动态模型，全盘撑控整个工作面的状况，具有比在工作面现场还能知道更多的信息。
这是两巷的情况，可以看到转载机、皮带机的情况，可以看到井下设备串车情况、集控室的情况，未来可以在地面，利用5G等技术，对井下设备进行操控。
地质保障系统由于时间关系，暂时介绍到这里。

## 生产技术管理平台
### 基本信息
* 网页地址：http://123.57.104.55:5000/
* 矿井：小纪汗
* 供电系统图图纸名称：小纪汗井下供电系统图_20221009
* 绘图单元名称：东盘区第一变电所、西盘区第一变电所

### 功能展示
* 首页整体情况展示
![生产技术管理平台](%E7%94%9F%E4%BA%A7%E7%AE%A1%E7%90%86.png)
<font color="red"> **旁白：**</font> 首先，生产技术管理系统是煤矿除了地质保障以外的全业务管理平台，包括`机电协同设计系统` `供电协同设计系统`  `通风协同设计系统` `采掘协同设计系统` `供排水协同设计系统` `应急救援协同设计系统` `辅助运输协同设计系统` `主运输协同设计系统` `人员定位协同设计系统` `通信联络协同设计系统` 等十个系统。这是目前矿上最重要的业务模块。我们的平台具有开放的能力，以后如果需要加入新的业务，可以通过标准化编码规则快速增加。下边我以 `供电协同设计系统` 为例来展示`分子化` `全要素` `开放性`在生产技术管理平台的具体实现。

* 供电系统主页展示
![](16653981899873.jpg)
 <font color="blue"> **操作：**</font>演示示例`小纪汗`，由上到下依次点击功能列表，展示功能全貌。
  <font color="red"> **旁白：**</font> 进入 `供电协同设计系统` 后，我们可以看到系统对用户的权限做了限制，当前是集团账号，我们切换到`小纪汗`矿查看对应内容。系统包括4大部分：`图纸管理` `后台管理` `类型管理` `台账管理`。
  
*   后台管理展示
![](16654044952464.jpg)
 <font color="blue"> **操作：**</font>演示示例`全部后台功能`，首先展示设备管理、材料管理、地点管理；其次展示图签管理和绘图单元，绘图单元展示`东盘区第一变电所`  `西盘区第一变电所`；最后展示配置巡回检查记录。
 <font color="red"> **旁白：**</font> 不单是大数据平台和地质保障平台由`分子化`元素组成，生产技术管理平台的后台管理模块通过对设备、地点、材料等几部分对业务数据融合，实现业务全生命周期`分子化`管理。绘图单元与图例管理模块则体现了供电业务图协同驱动成图的`分子化`管理。配置巡回检查记录主要是用来定制各种业务检修台账是系统`开放性`的一个展现方式。

* 类型管理展示
![](16654078810850.jpg)
 <font color="blue"> **操作：**</font>演示示例`铠装电缆` `UP-3*120+1*35`，按序号依次点击，展示类型的编辑和预览。
<font color="red"> **旁白：**</font> 类型管理模块对系统使用的材料类型进行在线管理（供电系统这里指电缆），可以对材料类型进行增删改查的操作。选择一个已有的材料类型还可为其添加型号：需输入型号代号、电压等级、动力线截面积、地线截面积等属性。

* 台账管理展示
 ![](16654097700052.jpg)
 <font color="blue"> **操作：**</font>演示示例`全部台账的列表`，由上到下依次点击。
 <font color="red"> **旁白：**</font> 台账管理模块管理了各业务部门常用的台账，供电协同设计系统目前管理的模块有：`巡回检查台账` `变配电所台账` `设备巡检记录` `设备检修记录`。同时，因为我们做到了业务属性的`分子化`，所以可以根据各集团，各煤款的使用习惯定制台账属性与样式。目前在`后台管理`中已经可以自定义检修台账，后续会继续在系统`开放性`上发力，定制更多类型的记录台账。
  
*   图纸管理展示
    ![](16653984830105.jpg)
    ![](16653989414434.jpg)
    <font color="blue"> **操作：**</font>演示示例`小纪汗矿2021年5000（二盘区）——井下电气设备布置图_202210102022183`，按序号依次点击，展示图纸的编辑和预览，描述一下图层的关系。
    <font color="red"> **旁白：**</font> 我们来看一下`图纸管理`，图纸管理展现出供电业务`全类型业务图纸`，图纸类型可以通过系统的开放性手动配置。`井下电气设备图`的数据分别来自融合平台，它引用了地质保障平台的采掘工程平面图为底图，可以添加需要的业务图层来展示设备、设施的布置情况。因为设备、设施的管理是分子化的，所以当设备、设施的位置或运行状态发生变化后，就可以增量体现在当前图纸上。
    
    ![](16654042081995.jpg)
    <font color="blue"> **操作：**</font>演示示例`小纪汗井下供电系统图_20221009`，按序号依次点击，展示图纸的编辑和预览。
    <font color="red"> **旁白：**</font> 接下来看一下供电系统图，这里主要是以后台管理和类型管理的`分子化`为依托，选取图纸所需元素，包括图纸范围内的会图单元、图签、图例、明细栏等。可一键成图，简化手动绘制的复杂工序，提高绘图人员的工作效率。同时，系统还支持对图纸的上报功能，以此达到对图纸留底，便于图纸的管理。




