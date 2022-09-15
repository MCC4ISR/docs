## JOIN_ROOM

加入一个房间

|key|value|type|
|:-:|:-:|:-:|
|id|用于接收反馈|string|
|room_id|要加入的房间编号|Array<int>|
|pwd|加入密码|string?|

加入的房间号格式为`[1,1]`

加入有密码的房间时需要附带密码，没有密码的房间则不需要

## LEFT_ROOM

离开当前房间，如果未在房间中则不会有任何反应

|key|value|type|
|:-:|:-:|:-:|
|id|用于接收反馈|string|
|tarn_owner|是否更换房主|boolen|

如果房主离开房间而不选择更换房主，则房间被解散

## CHAT

客户端聊天

|key|value|type|
|:-:|:-:|:-:|
|id|用于接收反馈|string|
|text|聊天内容|string|

如果在房间内则自动转换为房间内私聊，房间内私聊只有同方的人才能收到

## CMD

|key|value|type|
|:-:|:-:|:-:|
|id|用于接收反馈|string|
|cmd|执行的命令|string|

详见：命令