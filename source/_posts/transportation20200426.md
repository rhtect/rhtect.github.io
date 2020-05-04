---
title: 辅助运输20200426
date: 2020-04-25 18:59:38
updated: 2020-04-25 18:59:38
categories: 计划任务
tags: 辅助运输
mathjax: ture
password: ruihua123
---

### 服务端
**母玉峰**

* 支持魏墙矿
> * 里程统计入口：加在出勤统计里，与 `车辆` `司机`并列
> * 超速提醒限制2分钟(需要后台配置时间)
> * 消息提醒降低滚动速度，不满一屏是不滚动
> * ~~不同车辆设置不同速度上限~~(王迪 5月10日前)
> * 只显示超速和长时间未移动信息，其他隐藏
> * 导出超速车辆信息
> * 视频监控接入辅运系统

* 障碍物预警
* 应急广播功能
> 利用消息推送播放本地语音的方式实现
* 违章提醒功能
> 在魏墙矿违章后台基础上增加


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

* 大型车避让增加消息队列
* 语音播报前增加提示音
* 车载终端显示当前时速
* 修复平板视频首次连接黑屏的问题
* 调整UI细节


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
* [ ] 判断行驶方向
* [ ] 判断障碍物前后位置
* [ ] 障碍物距离去抖动：抖动范围：$Range \leq 30cm$

### 井下红绿灯控制  (孙虎)
* [x] 收集车辆定位卡信息
* [ ] 筛选满足触发条件的车辆
* [ ] 判断车辆行驶方向
* [x] 判断信号灯与车辆距离
* [ ] 判断丁字路口与十字路口（可以后台配置）
* [ ] 自动独立控制信号灯
* [ ] 自动批量控制信号灯
* [x] 手动独立控制信号灯
* [x] 手动批量控制信号灯
* [x] 信号灯常亮
* [x] 信号灯闪烁
* [ ] 违章信息提醒（违章信息发生时推送消息）
* [ ] 违章管理后台（简单记录一下闯红灯信息 参考超速提醒）
* [ ] 交通信号灯功能测试

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
		if canSwitchLedColour == true: 
			switchLedColour(activeTraffic, status，duration)
    return	

# 切换信号灯
def switchLedColour(address, status, duration):
	# activeTraffic 
	# add
	canSwitchLedColour = true
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

# 信号灯熄灭
def showLedOff(address, status):
	 # 控制传入信号灯的状态status：信号灯熄灭
	showLedFinished(address)
	return

# 信号灯工作结束
def showLedFinished(address, status):
	 # 控制传入信号灯的状态status：信号灯熄灭
	resetStatus(address)
	return

# 信号状态初始化
def resetStatus(address):
	 # 控制传入信号灯的状态status：信号灯熄灭
	canSwitchLedColour = false
	return
```

### 设计手机版辅运系统（焦黎阳）
* 车载终端显示当前时速
* 车载终端显示前方红绿灯的状态
* 车载终端显示距离前方红绿等的距离
* 完善领导端APP页面设计
* 配合工程师调整细节
* 设计车载终端APP`出车` `收车`页面
