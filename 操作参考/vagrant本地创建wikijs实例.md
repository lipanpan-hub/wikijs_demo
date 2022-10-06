---
title: Vagrant 本地创建 WIKIJS 实例
description: 
published: true
date: 2022-10-06T02:46:29.042Z
tags: 
editor: markdown
dateCreated: 2022-10-06T01:22:34.608Z
---

## 0x00 前置条件
你的电脑已经 安装好了 vagrant 和对应的虚拟机软件
并且 你已经大概了解了vagrant 的使用 


## 0x01 把 vagrant box 添加到本地 vagrant 系统

首先 拿到我们的 vagrant box 文件
把 vagrant box 从网盘下载到本地的目录当中
当前仅仅有适配 hyperv 虚拟机的 vagrant box 后续会适配其他虚拟机软件


比如 我的 浏览器 会把 文件下载到本地的 `C:\Users\lipanpan\Downloads` 目录当中

以`超级管理员权限` 打开terminal工具 并且进入到这个目录 
```
cd C:\Users\lipanpan\Downloads
```
通过 下面命令 把box添加到自己的vagrant系统当中
```
vagrant box add --name 给box起个名字  box文件
```

添加完成之后 可以通过 下面命令 查看添加的box 
```
vagrant box list
```

## 0x02 用 vagrant box name 初始化 Vagranfile
初始化 vagrantfile 之前 首先 新建一个文件夹 用来存放我们的项目 和 vagrantfile 

```
mkdir wikijs
cd wikijs

vagrant init 刚才给box起的名字
```
执行完成之后 就能通过ls/dir 命令在当前文件夹下看到 vagrantfile文件了 

## 0x03 轻松创建 wikijs 实例 

执行 下面命令 用 hyperv虚拟机 创建 wikijs 实例 

```
vagrant up --provider hyperv 
```

使用hyperv虚拟机创建wikijs实例的过程vagrant会提示你 选择虚拟交换机 并且输入smb的账号和密码

```
default: 1) 外部虚拟交换机(不共享)
default: 2) 内部网络虚拟交换机
default: 3) 共享网口外部网络虚拟交换机
default: 4) 专用网络虚拟交换机
default: 5) Default Switch
    
这里直接选择对应的数字就行了, 如果没有虚拟交换机 则需要自己在hyperv软件中自行创建
```

```
default: Username (user[@domain]): lipanpan
default: Password (will be hidden): 密码在这里输入,输入后是不会有任何显示的
		
SMB 的账号密码就是自己当前登录账号的账号和密码 
```








