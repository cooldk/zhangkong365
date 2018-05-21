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

## DATA ACCESS

###### Application layer protocol

	{"hello":world}
	
###### MQTT
iothub.thingworks.cn:1883
	
## Component
### Mobile
###### 文本
###### 指标
###### 指标（小）

