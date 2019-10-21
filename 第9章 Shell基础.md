# 第9章 Shell基础
---

### 9-1 shell概述

shell是一个命令行解释器，向用户提供一个向linux内核发送请求的以便以便运行程序的界面系统及程序，用户可以向shell来启动，挂起停止甚至编写程序

shell还是一个功能强大的编程语言，容易编写和调试，灵活性较强

shell是解释执行的脚本语言，在shell中可以直接调用Linux系统命令，

```echo $SHELL``` #查看当前的shell

系统登录时的shell为shell还可以登录其他的shell为子shell

### 9-2 脚本执行方式

```echo [选项] "[输出内容]"```

-e 支持反斜杠\控制的字符转换

- \a警告音
- \b退格
- \n换行
- \r回车
- \t&nbsp;Tab
- \v垂直制表符
- \onn八进制ASCII输出
- \xhh 十六进制ASCII输出

输出内容```\e[1;31m xxxxx \e[0m```,带颜色输出

- 30m&nbsp;black
- 31m&nbsp;red
- 32m&nbsp;green
- 33m&nbsp;yellow
- 34m&nbsp;blue
- 35m&nbsp;magenta
- 36m&nbsp;cyan
- 37m&nbsp;white

脚本第一句是```#!/bin/bash```表示为标准的Linux脚本

\#后内容为注释

脚本执行：

```chmod 755 hello.sh```
```bash hello.sh```
```./hello.sh``` or ```/root/hello.sh```

### 9-3 别名与快捷键

```alias ```#查看系统中的别名

```alias 别名：'原命令'```

重启后将实效

```vi ~/.bashrc``` #写入环境变量配置文件，永久生效(reboot)

也可以调用```source .bashrc```直接生效

命令生效顺序：

1. 绝对路径或相对路径执行的命令
2. 别名
3. Bash内部命令
4. 按照$PATH环境变凉定义的目录查找顺序找到的第一个命令

别名将覆盖系统命令

快捷键：

- ctrl+C &nbsp;强制终止
- clear / ctrl+L &nbsp;清屏
- ctrl+U &nbsp;从光标处删除至行前
- ctrl+A &nbsp;光标移动至行首
- ctrl+E &nbsp;光标移动至行尾
- ctrl+Z &nbsp;命令放入后台
- ctrl+V &nbsp;历史命令中搜索

### 9-4 历史命令

### 9-5输出重定向