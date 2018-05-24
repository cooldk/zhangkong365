# Doc
## FUNCTION
###### daily
	daily([8])是一个 transition 指标，他会在每天0:00:00值为1
###### hour
	hour([8]) 会返回当前index下的小时
###### minute
	minute() 会返回当前index下的分钟
###### match
	match (1,A[1..index]) 会返回指标 A 在当前 index 前上一个值为 1 的 index
###### sum
	sum (B[match (1,A[1..index])..index]) 会返回 从指标A上一个值为1的位置开始到当前的累积求和
	
## API
###### Auth

###### 创建指标

## Component
### Mobile
###### 文本
###### 指标
###### 指标（小）

## 数据接入 & 设备参考设计

###### 注意
- 新手指引： [起步走 - 接入传感器数据](www.zhangkong365.com) 

### 概念

掌控可以接入任何符合传输协议的时序数据，他可以是由传感器获得的实时状态数据，也可以是设备工作的过程数据。


###### 指标（Indicator）
- 物联网的数据接入概念
- 指标的格式定义(Float)
- 指标是唯一的
- 指标ID的生成是通过掌控来完成
- 可以通过 [API](www.zhangkong365.com) 来自动创建指标

### 连接
#### MQTT

您可以通过MQTT的方式上报数据

| 名称 | 参数 |
|:--|:--|
| 地址 | iothub.thingworks.cn |
| 端口 | 1883 |
|topic|/publish|

#### Application layer protocol

传输协议由json格式构成，每个包可以是由一个或者多个指标构成。ts如不写的话会以服务器的默认接受时间为准。指标的id是由掌控系统生成，请到[后台]()指标中，选择添加一个指标。或者使用api程序添加指标。

传输格式举例如下：

	{ "ts": 1526456617616, "indicators": [ { "id": "805156F9-DA19-49BF-A8BC-97CD714B83DE", "value": 11974 }, { "id": "ffff", "value": 11974 } ] }
	

	


### 最佳实践

###### 设备部署
- 设备部署的时候需要对指标进行命名

###### 安全
password

###### 连接

#### 安装引导

