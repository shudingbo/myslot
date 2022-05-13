---
title: 杂项
description: 记录学习过程中的一些杂项
published: 1
date: 2022-05-13T03:47:15.429Z
tags: c#
editor: markdown
dateCreated: 2022-05-13T03:47:15.429Z
---

# where T : class, new()

这是针对泛型类型的约束
```where T : class```
意思是 T 必须是引用类型

```where T : new()```
意思 T 必要要有一个无参的构造函数。此约束将允许您执行类似于```T field=new T()```的操作。

合并后就是下面的写法

``` c#
where T : class, new()
```