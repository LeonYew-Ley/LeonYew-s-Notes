# 机电比赛UI部分功能划分

## 功能概述
使用小程序向单片机机器发送指令信号（可能需要机器端用 python脚本实现 GET REQUEST 获取信号的操作），类似米家智能网关或是 Apple HomeKit

## 呈现平台
微信小程序

## 需要技术
微信 HTML, JS, CSS(WXSS), Python（单片机上），AT 指令发送

## 功能分布
<img alt="picture 0" src="https://cdn.jsdelivr.net/gh/LeonYew-SWPU/FileTem@main/imgs/2024/01/20240331-112754.jpg" width="600" />  

|左侧|中间|右侧|
|--|--|--|
|圆盘遥感/十字方向键|操作区，信息显示区|指令区|
|操控机器地盘移动|操作导轨移动，显示指令发送时间、发送状态等信息|向机器发送信号|

## 参考视频
- 机电其他团队的 UI 展示视频
- [开源+手把手教学：微信小程序通过阿里云控制和接收单片机数据](https://www.bilibili.com/video/BV1kj41117Rz/)
- [开源：32单片机通过ESP8266与微信小程序通信](https://www.bilibili.com/video/BV1fH4y1U7TE/)
- [合集·十天完成蓝牙通信工具小程序开发](https://space.bilibili.com/357684226/channel/collectiondetail?sid=596089)
- [秒懂——微信小程序控制伺服电机，程序简单上手](https://www.bilibili.com/video/BV1EM411H7vW/)
- [微信小程序和ESP32的蓝牙通讯，看了的基本都会了，除非不会](https://www.bilibili.com/video/BV1oq4y1q7sC/)