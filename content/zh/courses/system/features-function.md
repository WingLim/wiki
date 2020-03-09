---
title: "操作系统的特征与功能"
date: 2020-02-27T10:22:05+08:00
draft: true
---

## 特征

### 并发



### 共享

指系统中的资源可供内存中多个并发执行的进程共同使用

#### 互斥共享方式

1. 在一段时间内只允许一个进程访问资源
2. 临界资源：在一段时间内只允许一个进程访问的资源

#### 同时访问方式

1. 宏观上在一段时间内允许多个进程“同时”访问资源
2. 微观上是交替访问

### 虚拟

指通过某种技术把一个物理实体变为若干个逻辑上的对应物



### 异步

1. 进程是以人们不可预知的速度向前推进的
2. 导致的原因：竞争资源

## 功能

### 处理机管理

对处理机进行分配--进程和线程的管理和调度

### 存储器管理

对内存进行分配、保护、扩充及地址映射

### 设备管理

接收用户程序的 I/O 请求，分配设备，启动设备

### 文件管理

文件的存取、信息的共享与保护、文件存储空间管理

### 提供用户接口

命令接口、图形接口、程序接口