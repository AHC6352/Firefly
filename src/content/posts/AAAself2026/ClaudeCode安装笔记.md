---
title: "windowsClaudeCode安装"
published: 2026-06-12
updated: 2026-06-12
pinned: false  #是否置顶
description: "介绍如题"
tags: [单片机,开发]
category: 单片机开发
draft: true
author: anan
---


## 网站

[id]: https://daheiai.com/cc-install.html "参考教程网站"
 [参考教程网站][id] 


 ## 安装git

 [id]: https://git-scm.com/book/zh/v2/%E8%B5%B7%E6%AD%A5-%E5%AE%89%E8%A3%85-Git "git安装"
  [git安装官方教程][id] 

## 安装ClaudeCode本体

### 1.开始安装

在开始菜单中搜索管理员终端（PowerShell）

复制以下命令到终端并回车
```markdown
irm https://daheiai.com/cc.ps1 | iex
```

等待下载完成，大约30分钟左右

![完成页面](./2026img/claudedownload.png)

这里会显示安装目录所在位置

例：
```markdown
C:\Users\90506\.local\bin\claude.exe
```

可以通过复制这一行名令来启动你的Claude

*或者将其配置到你的环境变量中，输入Claude便可启动

![出现了无法连接的报错](./2026img/cldfail.png)

这里报错是正常的，这个时候需要接入API

接下来下载CC-Switch

### 2.下载CC-Switch

该软件是一个管理模型的多功能工具

[id]: https://wwayc.lanzoub.com/iiHKV3n29yhe "下载"
[Windows下载CC-Switch][id]

点进上方链接下载CC-Switch
下载完成后桌面上自动添加快捷方式

### 3.购买deepseek模型

[id]: https://platform.deepseek.com/usage "API开放平台"
[API开放平台][id]

点进上方链接或者从deepseek官网进入deepseekAPI开放平台

后面根据页面提示操作登陆并充值一定额度

### 4.创建一个API

![](./2026img/APIKEY.png)

![](./2026img/APIKEY2.png)
点击进入左侧的API keys，进入后再点击创建 API key，名字随便取，下一步会显示API key，注意这个APIkey只有在创建的时候会显示一次，所以需要复制并保存在一个地方（随便一个方便查看的地方）。如果丢失了这个key那就只能重新创建了

### 5.在CC-Switch中添加模型

打开CC-Switch

点击这个+号
![](./2026img/AA2.png)


选择deepseek并选择添加
![](./2026img/AA3.png)




