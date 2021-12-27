---
title: 生产技术管理系统GIS部分功能演示演示流程
date: 2021-12-13 18:22:32
categories: 汇报
tags: [生产技术管理, 董莹]
mathjax: ture
password: management
---

### 汇报内容

一、可视化编辑

- 原型地址：[https://a0eowa.axshare.com/#id=y4up4o&p=图纸可视化编辑](https://a0eowa.axshare.com/#id=y4up4o&p=%E5%9B%BE%E7%BA%B8%E5%8F%AF%E8%A7%86%E5%8C%96%E7%BC%96%E8%BE%91)

- 演示步骤
    1. 入口：右上方标签选择可视化
    
    ![Untitled](Untitled.png)
    
    2. 图层面板
    
       - 列表分类展示：业务图层、当前图层
    
       - 图层显示隐藏：列表项前眼睛图标
    
       - 图层面板可展开收缩：点击图层面板右侧标签
         
           ![Untitled](Untitled%201.png)
           
    
       - 图层搜索
           1. 输入框输入“供电”，点击右侧放大镜触发（功能实际为输入过程匹配，每输入一个字下方展示可选结果，此处原型这样展示）
           
           ![Untitled](Untitled%202.png)
           
           2. 下方搜索结果框选中第一项，此时图层列表选中对应图层（原型中为列表第一项），地图中高亮此图层下元素
           
           ![Untitled](Untitled%203.png)
    
    3. 修改位置
    
       - 导线点定位
           1. 点击井下变电所，弹出修改位置，点击右侧图标
           
           ![Untitled](Untitled%204.png)
           
           2. 修改位置面板选择“导线点定位”，图中井下变电所位置出现【原】图标
           
           ![Untitled](Untitled%205.png)
           
           3. 导线点名称输入框输入“导线点”，选择“1号导线点”，地图中对应位置出现【现】图标
           
           ![Untitled](Untitled%206.png)
           
           4. 导线点前后选择“前”，距离填写任意数字，修改目标位置坐标Z值为任意值，对应图中【现】位置不断变化，下方目标位置坐标也不断变化
           
           ![Untitled](Untitled%207.png)
           
           5. 点击确定，修改位置面板关闭，井下变电所位置执行修改
           
           ![Untitled](Untitled%208.png)
           
    
       - 自定义定位
           1. 点击汽轮机，弹出修改位置选择框，点击修改图标
              
               ![Untitled](Untitled%209.png)
               
           2. 修改位置面板选择自定义定位，地图中原位置标识【原】图标
              
               ![Untitled](Untitled%2010.png)
               
           3. 点选如下图中黑色圆圈表示位置（原型中未标识此黑点），之后此位置出现【现】图标
              
               ![Untitled](Untitled%2011.png)
               
           4. 点击确认执行位置修改
              
               ![Untitled](Untitled%2012.png)
           
    
       - 地点定位
           1. 点击采区变电所上18数字指针上方展开包含的设备列表，点击某一列表右侧修改位置图标，右侧弹出修改位置面板，图中原位置出现【原】图标
              
               ![Untitled](Untitled%2013.png)
               
               ![Untitled](Untitled%2014.png)
               
           2. 修改位置面板选择地点定位
              
               ![Untitled](Untitled%2015.png)
               
           3. 地点名称输入框输入“井下变电所”，选择下方结果
              
               ![Untitled](Untitled%2016.png)
               
           4. 点击确认执行位置修改
              
               ![Untitled](Untitled%2017.png)
               

二、获取坐标

- 原型地址： [https://a0eowa.axshare.com/#id=1lc1po&p=地点管理&g=1](https://a0eowa.axshare.com/#id=1lc1po&p=%E5%9C%B0%E7%82%B9%E7%AE%A1%E7%90%86&g=1)

- 演示步骤：
    1. 入口：新增某个地点，填写信息后跳转到编辑详细信息部分，点击定位服务
    
    ![Untitled](Untitled%2018.png)
    
    ![Untitled](Untitled%2019.png)
    
    2. 右侧选择三种定位方式，输入信息同可视化编辑部分，地图中出现对应位置的指针
       - 此时不演示一个方式确认后再选择另一个方式，只在同一个页面演示完一个不点击确认获取，演示另一个，最后一个确认获取关闭此页面
    
    
    ![Untitled](Untitled%2020.png)
    
    3. 点击确认获取按钮，弹窗二次确认
    
    ![Untitled](Untitled%2021.png)
    
    4.跳转回表单填写页面，此时自动填写位置坐标
    
    ![Untitled](Untitled%2022.png)
