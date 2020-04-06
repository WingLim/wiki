---
title: Lim Wiki
description: Lim Wiki
date: 2020-01-26T04:15:05+09:00
draft: false
bookToc: false
---
# Lim's Wiki

## 介绍

这里是 WingLim 的个人 Wiki

博客地址：[二木浮生记](https://limxw.com)

Tech 部分记录了代码相关的东西，例如一些工具的配置，一些编程技巧

Courses 部分则是大学课程相关的内容

这里用来记录平时遇到的一些零散的知识，等知识积累足够多后再提炼总结成博客

## 搭建流程

这个 Wiki 是通过 [hugo](https://gohugo.io/) 和 [hugo-book](https://github.com/alex-shpak/hugo-book) 主题生成的。

同时添加了 Mathjax [^1]来解析数学公式，因为在 Hugo 中，Latex 的换行语法和 Markdown 语法解析会有冲突，导致原主题使用的 Katex 没办法换行。

使用了 Github Actions [^ 2]来自动构建和部署 Hugo 页面到 Github Page

在服务器上使用了 Caddy 来配置 Git webhooks。

当 Github Actions 构建完毕并部署到 Github Page 上时会触发 webhook。

Caddy 会拉取 repo 的 gh-page 分支到服务器上，完成在服务器上的部署。

[^1]: https://github.com/WingLim/wiki/blob/master/layouts/partials/docs/inject/footer.html



[^ 2]: https://github.com/WingLim/wiki/blob/master/.github/workflows/hugo.yml