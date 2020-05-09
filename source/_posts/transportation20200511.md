---
title: 辅助运输20200511
date: 2020-05-09 17:48:31
updated: 2020-05-09 17:48:31
categories: 计划任务
tags: 辅助运输
mathjax: ture
password: ruihua123
---

### 服务端
**母玉峰**

#### 支持魏墙矿

> * 魏强矿功能完善
> * 视频监控接入辅运系统

#### 障碍物预警（5月12日前安成）
* [ ] 判断行驶方向
* [ ] 判断障碍物前后位置
* [ ] 障碍物距离去抖动
* [ ] 障碍物消息推送
* [ ] 选障碍物类型识别

#### 应急广播功能
* [ ] 利用消息推送播放本地语音的方式实现

#### 违章提醒功能
* [ ] 在魏墙矿违章后台基础上增加

### 客户端
**花雷 左俊**

#### 车载终端APP

* 车载终端显示当前时速
* 修复平板视频首次连接黑屏的问题

#### 障碍物预警
* [ ] 判断行驶方向
* [ ] 判断障碍物前后位置
* [ ] 障碍物距离去抖动
* [ ] 障碍物消息推送
* [ ] 选障碍物类型识别

#### 应急广播功能
* [ ] 利用消息推送播放本地语音的方式实现
#### 违章提醒功能
* [ ] 在魏墙矿违章后台基础上增加

#### 领导端APP
* [ ] 登录
* [ ] 首页
* [ ] 我的
* [ ] 统计页
* [ ] 用车申请-默认列表
* [ ] 用车申请-待审批列表页
* [ ] 用车申请-详情
* [ ] 用车申请-审批编辑详情
* [ ] 出勤管理-首页
* [ ] 出勤管理-司机管理列详情
* [ ] 出勤管理-车辆管理列详情
* [ ] 基础功能数据处理
* [ ] 基础功能控件



### 井下红绿灯控制  (孙虎)
* [x] 收集车辆定位卡信息
* [x] 筛选满足触发条件的车辆
* [ ] 判断车辆行驶方向
* [x] 判断信号灯与车辆距离
* [ ] 判断丁字路口与十字路口（可以后台配置）
* [x] 自动独立控制信号灯
* [x] 自动批量控制信号灯
* [x] 手动独立控制信号灯
* [x] 手动批量控制信号灯
* [x] 信号灯常亮
* [x] 信号灯闪烁
* [ ] 违章信息提醒（违章信息发生时推送消息）
* [ ] 违章管理后台（简单记录一下闯红灯信息 参考超速提醒）
* [ ] 交通信号灯功能测试

### 路口管理后台 (孙虎)
* 管理后台`增` `删` `改` `查`。
* 配置控制器是否生效
* 支持导入导出EXCEL配置文件

* `新增`和`修改`的字段
> 红绿灯方向：0 不生效；1 2 4 8 红绿灯方向
> 表预留两个字段 
> 状态相同的方向为相同分组
> 分组数量在0～4个之间
```
控制器IP
控制器对应红绿灯A 
控制器对应红绿灯B
控制器对应红绿灯C
控制器对应红绿灯D
控制器对应红绿灯E
控制器对应红绿灯F
控制器是否启用
是否删除
```

* 后台显示项目
> * 序号
> * 控制器材IP地址
> * 控制器对应红绿灯A
> * 控制器对应红绿灯B
> * 控制器对应红绿灯C
> * 控制器对应红绿灯D
> * 控制器是否启用
> * 操作

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

* 完善领导端APP页面设计

