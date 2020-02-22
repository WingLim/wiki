---
title: "Git"
description: "记录一些比较有用的Git命令"
date: 2020-02-22T22:50:06+08:00
draft: false
---
## Submodules

### 添加

```bash
git submodule add <url>
```

### 更新

```bash
git submodule update --remote --merge
```

### 恢复

克隆一个带 submodule 的 repo 时，通过下面这条命令下载 submodule

```bash
git submodule update --init --recursive
```

### 删除

```bash
# 删除 submodule 目录及源码
rm -rf <submodule_folder>
# 删除 submodule 目录
rm -rf .git/module/<your_submodule>
# 删除 .gitmodules 中 submodule 相关条目
vim .gitmodules
# 删除配置项中 submodule 相关条目
vim .git/config
```





## 分支

### 查看

```bash
git branch -a
```



### 创建并切换

```bash
git checkout -b <branch>
```



### 切换

```bash
git checkout master
```



### 删除

#### 本地分支

```bash
git branch -d <branch>
```

#### 远程分支

```bash
git push origin --delete <branch>
```



### 合并

```bash
git merge <branch>
```



## 标签

### 创建

```bash
git tag <tagname> <commit>
```



## 替换本地改动

即恢复文件到上一次 commit

```bash
git check -- <filename>
```



丢弃本地所有改动和提交

```bash
git fetch origin
git reset --hard origin/master
```



## 一些指南

[图解Git](http://marklodato.github.io/visual-git-guide/index-zh-cn.html)