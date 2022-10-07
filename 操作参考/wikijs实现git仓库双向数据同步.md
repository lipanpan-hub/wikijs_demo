---
title: WIKIJS 实现 GIT 仓库双向数据同步
description: 
published: true
date: 2022-10-07T01:15:41.996Z
tags: 
editor: markdown
dateCreated: 2022-10-07T01:15:40.337Z
---

# WIKIJS 开启 GIT双向数据同步


首先建立 一个 git仓库,  github/gitee 都行, 私有仓库/公开仓库 都行

然后 初始化仓库 创建 一个 main/master 分支 

为仓库 添加 ssh public key 记得 `这个key要有读写权限`, 如果没有读写权限是不行的 


然后就是设置 wikijs 这边, 按照方框当中的提示设置就行了 无任何难度 

![snipaste_2022-10-06_10-59-09.png](/images/snipaste_2022-10-06_10-59-09.png)

