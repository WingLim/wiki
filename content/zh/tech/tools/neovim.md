---
title: "Neovim"
date: 2020-02-23T15:19:16+08:00
draft: false
---

## 构建准备

### 一般要求

1. Clang or GCC `4.4+` 版本
2. 添加了 TLS/SSL 编译的 CMake `2.8.12+` 版本

## Ubuntu / Debian

```bash
sudo apt-get install ninja-build gettext libtool libtool-bin autoconf automake cmake g++ pkg-config unzip
```

在 Ubuntu 16.04 / Debian Jessie 和更高版本中需要安装 `libtool-bin`

## CentOS / RHEL / Fedora

```bash
sudo yum -y install ninja-build libtool autoconf automake cmake gcc gcc-c++ make pkgconfig unzip patch
```

## Arch Linux

```bash
sudo pacman -S base-devel cmake unzip ninja
```

## macOS

1. 安装 Xcode 和 Homebrew

2. 安装 Xcode commandline tools `xcode-select --install`

3. 安装其他依赖

   ```bash
   brew install ninja libtool automake cmake pkg-config gettext
   ```




## 开始编译

```bash
# 克隆源码
git clone https://github.com/neovim/neovim.git
cd neovim
# 切换到 stable 分支
git checkout stable

# Release 版
make CMAKE_BUILD_TYPE=Release
# 带 Debug 信息的 Release 版
make CMAKE_BUILD_TYPE=RelWithDebInfo

sudo make install
```

