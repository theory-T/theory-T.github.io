---
title: "Shell 脚本编程入门"
date: 2026-10-22T15:00:00+08:00
draft: false
categories: ["Shell"]
tags: ["脚本", "Bash", "编程"]
summary: "从 shebang、变量、条件判断到循环与调试，掌握 Bash 脚本的基本写法。"
---

## 一、脚本基础

Shell 脚本是包含若干命令的文本文件，首行 `#!/bin/bash` 称为 shebang，用于声明解释器。写完脚本后需要赋予执行权限：

```bash
chmod +x script.sh
./script.sh
```

## 二、变量与输入

```bash
age=22                  # 赋值时等号两侧不能有空格
read -p "Input: " name  # 从键盘读取输入
echo "Hello, $name"
```

## 三、条件判断与循环

```bash
if [ "$age" -ge 20 ]; then
    echo "adult"
else
    echo "minor"
fi

for i in "$@"; do
    echo "$i"
done
```

## 四、调试

使用 `bash -x script.sh` 可以逐行打印执行过程，方便定位逻辑错误。
