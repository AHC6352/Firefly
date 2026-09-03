---
title: "FreeRTOS笔记"
published: 2026-08-23
updated: 2026-08-23
pinned: false  #是否置顶
description: "关于FreeRTOS的一些笔记"
tags: [单片机, ]
category: 单片机开发
draft: false
author: anan
---


## 相关链接

- [FreeRTOS官网](https://www.freertos.org/zh-cn-cmn-s)

## 关于移植

### 系统配置文件修改

FreeRTOSConfig.h中添加如下3个配置：
```c
#define xPortPendSVHandler PendSV_Handler
#define vPortSVCHandler SVC_Handler
#define INCLUDE_xTaskGetSchedulerState 1
```




### stm32f1xx_it.c
#### 该文件中添加以下引用
```c
#include "FreeRTOS.h"
#include "task.h"
```

在文件中把mx自动生成的PendSV_Handler，SVC_Handler注释



#### 添加SysTick时钟中断服务函数
```c
extern void xPortSysTickHandler(void);

void SysTick_Handler(void)
{
    /* USER CODE BEGIN SysTick_IRQn 0 */

/* USER CODE END SysTick_IRQn 0 */

    /* USER CODE BEGIN SysTick_IRQn 1 */
    if (xTaskGetSchedulerState() != taskSCHEDULER_NOT_STARTED) 
    {
        xPortSysTickHandler();
    }
    /* USER CODE END SysTick_IRQn 1 */
}
```


### cubemx

#### 时基源
将默认的systick改为其他定时器，注意为了使delay可以抢占其他正在进行的中断，抢占优先级改为1


### 配置文件说明
- [官网中文说明](https://www.freertos.org/zh-cn-cmn-s/Documentation/02-Kernel/03-Supported-devices/02-Customization)

## 系统配置文件说明
不想写

## 数据类型
略
## 命名规范
略
## 使用

```c
BaseType_t xTaskCreate
(
    TaskFunction_t pxTaskCode,                  /* 指向任务函数的指针 */
    const char * const pcName,                  /* 任务名字，最大长度configMAX_TASK_NAME_LEN */
    const configSTACK_DEPTH_TYPE usStackDepth,  /* 任务堆栈大小，默认单位4字节 */
    void * const pvParameters,                  /* 传递给任务函数的参数 */
    UBaseType_t uxPriority,                     /* 任务优先级，范围：0 ~ configMAX_PRIORITIES - 1 */
    TaskHandle_t * const pxCreatedTask          /* 任务句柄，就是任务的任务控制块 */
)   
```





