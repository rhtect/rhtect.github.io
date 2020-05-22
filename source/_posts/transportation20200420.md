---
title: 辅助运输20200420
date: 2020-04-17 18:59:38
updated: 2020-04-17 18:59:38
categories: 计划任务
tags: 辅助运输
mathjax: ture
password: ruihua123
---

### 服务端
**母玉峰**

#### 特种车辆避让
* 到达目的地提醒
> 到达点提醒距离：$Range \leq 30m$
> 触发距离通过配置文件配置
> 通过车辆定位卡号识别
* 目的地管理可配置提醒地点

#### 周边障碍物预警模块

* 筛选碰撞消息符合条件的消息 
> > 筛选障碍物类型
>> > 固定障碍物：`红绿灯`、`路口`等
>> > 移动障碍物：`车辆`、`人员`等
> > 筛选位移范围：  $Range_i \leq Distance \leq Range_j$
> > 筛选方向（详见`寻路算法`）
> > 筛选时间范围 $Time \nleq \Delta t$ 

* 调用`寻路算法`找到当前车辆行驶的路径
> > 获取附近障碍物轨迹坐标集合
> > 计算附近障碍物距离锚点（井口）位移
> > 确认障碍物与当前车辆的位置关系

* 搭建AB Test 派车框架
> 不影响正常派车
> 完成车队自动指派`威龙` `塔通`功能
> 矿本部申请指派 `塔通车队`
> 其他申请指派 `威龙车队`
* 执行车队指派操作
> 提交排班后自动派车
> 优先指派条件
> 1)司机驾驶类型
> 2)空闲状态优先（按照以往派车习惯）
> 3)执行任务时长

* 研究 Elastic Search 自然语音分类框架
> 对所有申请订单的备注部分进行分类。

* 账户管理后台 （部署塔山服务器）


### 客户端
**花雷 左俊**

#### 车载终端APP

* 修复平板视频首次连接黑屏的问题
* 调整UI细节
* 增加视频巡检记录的功能（本地录像）
> 可以本地存储
> 可以切换摄像头
* 语音播报特种车辆避让信息

#### 领导端APP
* 根据UI设计开发领导端APP
> * 实时井下车辆数量统计功能
> * 实时井下人数统计功能
> * 实时违章数量统计功能
> * 当日司机出勤情况统计功能
> * 区域车辆分布功能
> * 出入井方向车辆统计功能
> * 出勤统计功能
> * 派车统计功能
> * 车辆24小时出入井统计功能
> * 按类型统计井下车辆功能
> * 实时车辆地图功能
> * 用车申请、审批统计功能
> * 车辆司机统计功能
> * 用车申请、审批消息功能
> * 车辆出入道闸消息功能
> * 车辆长时间不移动消息功能
> * 出勤上报功能
> * 用车申请功能
> * 用车审批功能
> * 指派车队功能
> * 车队派车功能
> * 监控井上、井下司机及车辆状况功能

#### 周边障碍物预警模块
> 判断行驶方向
> 判断障碍物前后位置
> 障碍物距离去抖动：抖动范围：$Range \leq 30cm$

### 里程统计
* 统计功能部署到魏强矿
* 凌晨`2：00`统计上一天的里程数据

### 井下红绿灯控制  (孙虎)
* 加入车辆位置信息
* 增加红路灯触发距离: $Range \leq 30m$
* 绿灯5秒闪烁
* 红绿灯触发距离可以配置
* 多控制器分开独立控制
* 判断十字路口方向

```python
# python


# status =  -1， -2，0， 1， 2 对应 灭灯 红灯闪烁、绿灯闪烁、灭灯、红灯亮起、绿灯亮起


flashDuration = 1 #定义闪烁时长 每秒钟闪烁1次
flashTimes = 5 #定义闪烁次数
trafficIds = [] #信号定控制器数组

# 程序入口
#收集定位卡
activeTraffics = receivePositios(positions) 
#控制信号灯
trafficsControl(activeTraffics)

# 接收车辆位置信息
def receivePositios(positions):
	# positions 车辆位置信息
	activeTraffics = {} #创建需要触发的控制器数组
	for trafficId in trafficIds :
		activeTraffic = {} #创建需要触发的控制器字典
		activePositions = []; #创建控制器数组
		for position in positions :			
			active = judgeTrafficStatus(trafficId, position)
			if active:
				activePositions.append(position) #添加车辆信息
			else :
				continue
		if positions.len() > 0: #数组不为0，执行以下操作
			activeTraffic = {trafficId, activePositions} #保存控制器和满足触发条件车辆信息
			activeTraffics.append(activeTraffic)
	
	return activeTraffics # 返回 控制器数组



# 判断触发条件
def judgeTrafficStatus(trafficId, position):
	# trafficId 红绿灯Id
	# position 车辆信息
	# 判断触发条件
	# 1. 判断行车方向: 靠近 或者 远离
	# 2. 判断车辆距离红路灯的位置 小于触发值
    return true # 返回 是否触发

# 控制器触发函数
def trafficsControl(activeTraffics):
	# 控制器数组
	for activeTraffic in activeTraffics :
		trafficControl(activeTraffic, 2，60)
    return

# 控制器触发函数
def trafficControl(activeTraffic, status, duration):
	# activeTraffic 控制器字典信息 包含车辆位置信息
	addresses = activeTraffic.addresses # 获取控制器地址
	for address in addresses :
		switchLedColour(activeTraffic, status，duration)
    return

# 切换信号灯
def switchLedColour(address, status, duration):
	# activeTraffic 
	# add
	if status == 1: #红灯
		showLedRed(address,duration)
	    return
	else: #绿灯 绿灯最后N秒闪烁
		duration_1 = flashDuration *  flashTimes
		showLedGreen(address,duration - duration_1)
		# duration - duration_1 秒后执行下边方法
		# 倒计时或者回调
		showLedFlash(address, -status，duration_1)
	    return

# 信号灯变红
def showLedRed(address，duration):
	 # 绿灯亮起
	 # 持续时间：duration
	return

# 信号灯变绿
def showLedGreen(address，duration):
	 # 绿灯亮起
	 # 持续时间：duration
	return

# 信号灯闪烁
def showLedFlash(address, status，duration):
	 # 控制传入信号灯的状态status：信号灯闪烁
	 # 持续时间：duration
	return
```

### 设计手机版辅运系统（焦黎阳）
* 完善领导端APP页面设计
* 配合工程师调整细节
* 设计车载终端APP`出车` `收车`页面
* 设计车辆信息页面
> 车牌号、车辆类型、定位卡号
> 司机照片、司机姓名、定位卡号、工作时长、下井时长、车载终端信号状态、语音通话按钮、视频通话按钮
> 显示附近的三个任务
> 指派任务按钮
