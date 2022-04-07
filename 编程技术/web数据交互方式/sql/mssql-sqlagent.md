---
title: linux mssql agent 不能执行
description: linux mssql agent 不能执行
published: 1
date: 2022-04-07T11:32:29.630Z
tags: mssql
editor: markdown
dateCreated: 2022-04-07T11:32:29.630Z
---

执行 计划任务提示错误如下:

```
The SQLServerAgent is not currently running, so it cannot be notified of this action. error:22022
```

## 原因
Linux 下的 sql agent 通过 hostname 与 sql server 进行连接，但是 sql server 只取了 hostname的前**15**个字符，例如 linux 的 host name 为 ip-192-168-1-111-internal, sql agent 获取的 hostname截断为 ip-192-168-1-11, 导致 agent不能连接到sql server。

## 解决方案

### 方案1
在安装 mssql前设置机子的hostname 为 长度小于15的字符
 * 更改 /etc/hostname
 *  在 /etc/hosts 下增加记录
   - 你的Ip   hostname   hostname

### 方案2
mssql已经安装完成。
* 查询 sqlserver 的 server name ```Select @@servername```
* 更改 /etc/hostname 和 /etc/hosts

参考： [官方文档](https://docs.microsoft.com/zh-cn/sql/linux/sql-server-linux-setup-sql-agent?view=sql-server-ver15#EnableAgentAfterCU4)



