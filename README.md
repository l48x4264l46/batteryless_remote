# 无电池遥控器

## 1 项目概述
由于普通遥控器的电池在使用一段时间后需要定期更换，我思索着有没有方法能做到***不换电池一直使用***。最终找到了通过按压发电模块作为电源的方法。本项目是该想法的一个具体实现。

## 2 功能介绍
### 2.1 使用前准备工作(操作一次即可)
* 通过Type-C线给遥控器供电
* 将无电池遥控器的信号接收口对准被录制遥控器的发射口
* 选中无电池遥控器的一个按钮，作为待录制按键，然后将其按下
* 按下被录制遥控器的被录制按键
* 等待无电池遥控器的指示灯亮起，表示录制完成
* 写下按键功能名字，贴到对应按键下方
### 2.2 基础使用方法
* 拿起无电池遥控器对准需要控制的设备(空调，电视等)
* 按下需要使用的功能按钮
* 继续按压无电池遥控器，直到听到咔嚓声，完成控制过程

## 3 基础原理解析
由于目前红外编解码缺乏统一的国际标准，因此不同厂商之间的红外标准会各不一样。但是从原理上来说就分为两种：

* 脉冲宽度调制(PWM)
* 脉冲位置调制(PPM)

软件实现上只需要兼容这两种方法就可以实现对大多数红外信号的编解码控制。