---
title: "Edulite 05 电机开发"
published: 2026-06-07
updated: 2026-06-07
pinned: false  #是否置顶
description: "Edulite 05 电机的基本参数、驱动板信息及上位机下载"
tags: [单片机, 电机开发, CAN通信]
category: 单片机开发
draft: false
author: anan
---

## 相关链接

- [EDULITE05 电机官网](https://www.robstride.com/products/eduLite05)
- [GitHub](https://github.com/RobStride)
- [Gitee](https://gitee.com/robstride)

## 一、电机基础信息

### 标准使用状态

1. **额定电压：48 VDC**
2. **使用电压范围：15V—60 VDC**
3. 额定负载（CW）：1.8 N.m（散热板尺寸 70mm×70mm）
4. 运转方向：CW/CCW（从出轴方向看）
5. 使用姿势：出轴方向为水平或者垂直
6. 标准使用温度：25±5℃
7. 使用温度范围：-20～50℃
8. 标准使用湿度：65%
9. 使用湿度范围：5～85%，无凝露
10. 保存温度范围：-30～70℃
11. 绝缘等级：Class B

### 部分电气参数

1. 空载转速：430 rpm±10%
2. 空载电流：0.14 Arms±10%
3. 额定负载：1.8 N.m±10%（转速 100rpm 下测试所得）
4. 额定负载相电流(峰值)：2.6 Apk±10%
5. 峰值负载：6 N.m
6. 最大负载相电流(峰值)：11 Apk±10%
7. 绝缘电阻/定子绕组：DC 500VAC, 100M Ohms
8. 耐高压/定子与机壳：600 VAC, 1s, 2mA
9. 电机反电势：7.4 Vrms/krpm ±10%
10. 转矩常数（有效值）：0.94 N.m/Arms

## 二、驱动板部分信息

![接口定义](2026e05img/接口定义图.png)

额定工作电压 48VDC

允许最大电压 60VDC

CAN 总线比特率 1Mbps

编码器分辨率 14bit

板端接口型号 XT30PB(2+2)-M.G.B

线端接口型号 XT30(2+2)-F.G.B

## 三、上位机

[上位机下载](https://gitee.com/robstride/MotorStudio/releases/tag/V26.03.01)

使用说明请参考手册。
