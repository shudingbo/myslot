---
title: My Project
description: 我的开源项目
published: 1
date: 2021-12-05T03:18:54.424Z
tags: my opensource project
editor: markdown
dateCreated: 2021-11-21T06:49:52.654Z
---

# [Sex-Pomelo](/my-project/sex-pomelo)
网易pomelo的维护版本。[ **[Api]** ]  [ **[Wiki]** ]  [ **[Github]** ] 


[![NPM version][npm-image-pomelo]][npm-url-pomelo]
[![NPM version][npm-image-down]][npm-url-pomelo]

## 2.3.0
[详细](https://gitee.com/shudingbo/sex-pomelo/raw/master/History.md)
1. 更新路由压缩组件
原有组件会扫描所有 handler，生成字典，这样会导致接口意外暴漏，导致安全问题。
现在更新为只有手动设置的路由才会暴漏并压缩。改动为通过 dictionary.json 设置可以压缩的路由。

2. 增加i18n内置组件
通过 pomelo.i18n开启，配置参数如下


---
[npm-image-pomelo]: https://img.shields.io/npm/v/@sex-pomelo/sex-pomelo.svg?label=sex-pomelo
[npm-url-pomelo]: https://github.com/sex-pomelo/sex-pomelo
[npm-image-down]: https://img.shields.io/npm/dw/@sex-pomelo/sex-pomelo?label=down
[Api]: https://shudingbo.github.io/sex-pomelo-doc/api/index.html
[Wiki]: https://github.com/NetEase/pomelo/wiki
[Github]: https://github.com/sex-pomelo



