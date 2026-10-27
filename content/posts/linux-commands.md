---
title: "Linux 常用命令速查"
date: 2026-10-20T10:00:00+08:00
draft: false
categories: ["Linux"]
tags: ["命令", "文件管理", "文本处理"]
summary: "整理 Linux 下最常用的目录、文件管理与文本处理命令，附典型示例。"
---

## 一、目录导航

| 命令 | 作用 | 示例 |
|------|------|------|
| `pwd` | 显示当前工作目录的绝对路径 | `pwd` |
| `cd` | 切换目录 | `cd /etc`、`cd ~`、`cd ..` |
| `ls` | 列出目录内容 | `ls -l`、`ls -la` |

Linux 采用以根目录 `/` 为起点的单根树形目录结构：`/bin` 存放基本命令，`/etc` 存放系统配置，`/home` 存放普通用户主目录，`/root` 为超级用户主目录，`/tmp` 为临时目录。

## 二、文件管理

- `touch file` 创建空文件；`mkdir -p a/b` 递归创建目录
- `cp file dir/` 复制；`cp -r dir backup` 递归复制目录
- `mv old new` 移动或重命名；`rm -rf dir` 递归删除
- `ln -s target link` 创建软链接；`ln target link` 创建硬链接

## 三、文本处理

- `cat` 显示全部内容；`less` 分页浏览；`head -n` / `tail -n` 查看首尾
- `grep pattern file` 检索；`grep -i` 忽略大小写、`-v` 反向匹配、`-n` 显示行号
- `sed` 流式替换：`sed 's/old/new/g' file`
- `awk` 按列处理：`awk '{print $1}' file`
