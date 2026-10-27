---
title: "使用 Hugo 搭建个人博客"
date: 2026-10-27T20:00:00+08:00
draft: false
categories: ["Hugo"]
tags: ["博客", "建站", "GitHub Pages"]
summary: "记录从安装 Hugo、创建站点、安装 PaperMod 主题到部署 GitHub Pages 的完整过程。"
---

## 一、安装与创建站点

```bash
sudo apt install hugo
hugo new site blog
cd blog
```

## 二、安装主题

使用 `git submodule` 引入 PaperMod 主题，便于版本管理：

```bash
git submodule add https://github.com/adityatelange/hugo-PaperMod.git themes/PaperMod
```

## 三、配置 hugo.toml

设置 `theme = "PaperMod"`，并配置首页、关于、标签、分类、归档、搜索六大菜单项；同时配置 `[outputs] home = ["HTML", "RSS", "JSON"]` 以启用搜索功能。

## 四、本地预览与部署

```bash
hugo server --bind 0.0.0.0 -D   # 本地预览
hugo                            # 生成 public/ 静态文件
```

本博客即通过上述步骤搭建，并部署到 GitHub Pages 供外网访问。
