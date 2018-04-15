---
layout:     post
title:      SQL Server
subtitle:   
date:       2018-04-14
author:     Daryl
header-img: img/enoshima.jpg
catalog: true
tags:
    - code
---

> 总结个人在配置环境和使用方面踩的坑和经验

## SQL Server

首先是尝试在Ubuntu上安装了SQL Server，只需复制官网上的命令执行即可，体验非常好，命令行工具和其他的工具都没什么差错地完成了。

GUI工具使用了SQL Operation Studio，用着感觉还可以，比原始的命令行工具确实好用了不少，其GUI和vscode类似（怕是直接copy过来的）。

然后尝试了在Windows上安装，最后还是退出了，因为杂七杂八的事情太多。。。甚至还要装python。很怕这么一折腾把我的环境搞爆了（之前装VS2017的python环境就把我原始的环境搞爆了）于是临时退出了。

这里就再写一点命令行工具的使用吧（这才是正文）：

#### 最基本的使用：
```sql
sqlcmd -S localhost -U SA -P [password]
```
这个就是打开命令行交互界面。但是我尝试了一下，似乎不能换行。。？还是不太好用

#### 执行脚本：
```sql
sqlcmd -S localhost -U SA -P [password] -i my.sql -o output.txt
```
执行`my.sql`脚本，输出结果到`output.txt`里


总结：命令行太tm难用了，还是用GUI吧。

