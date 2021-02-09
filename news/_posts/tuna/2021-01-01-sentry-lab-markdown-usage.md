---
category: news
layout: news
title: "SentryLab「markdown」语法介绍&批注"
author: Bin4xin
---

---
**SentryLab 站点markdown语法相关简介和学习批注；用于记录、参考，也欢迎各位联系投稿，会及时发布并第一时间通知，若需投稿直接发送md文件到`chihou.pro@gmail.com`即可。**

---


目录
------
- [目录](#%E7%9B%AE%E5%BD%95)
- [0x01 文件名称样式](#0x01-%E6%96%87%E4%BB%B6%E5%90%8D%E7%A7%B0%E6%A0%B7%E5%BC%8F)
- [0x02 头部基本样式](#0x02-%E5%A4%B4%E9%83%A8%E5%9F%BA%E6%9C%AC%E6%A0%B7%E5%BC%8F)
- [0x03 多样化展示信息](#0x03-%E5%A4%9A%E6%A0%B7%E5%8C%96%E5%B1%95%E7%A4%BA%E4%BF%A1%E6%81%AF)
- [0x04 如何改变文本的样式](#0x04-%E5%A6%82%E4%BD%95%E6%94%B9%E5%8F%98%E6%96%87%E6%9C%AC%E7%9A%84%E6%A0%B7%E5%BC%8F)
- [0x05 生成一个适合你的列表](#0x05-%E7%94%9F%E6%88%90%E4%B8%80%E4%B8%AA%E9%80%82%E5%90%88%E4%BD%A0%E7%9A%84%E5%88%97%E8%A1%A8)
- [0x06 文章参考](#0x06-%E6%96%87%E7%AB%A0%E5%8F%82%E8%80%83)

## 0x01 文件名称样式
`year-month-day-文章名称-尾缀.md`；实例：`2021-01-01-sentry-lab-markdown-usage.md`

相关：
- 文章标题根据文件名自动生成时间；
- 文章访问路由自动生成，按需可强制路由配置。

## 0x02 头部基本样式
文头基本样式，相关：
- 文章分类、位置；
- 文章名称、作者等具体信息；
- 文章访问路径，部分可强制置顶路由。

具体`category`和`layout`可以参考下表：

{: .table}
help | news | blog | events
-------|----------|----------|------
{about.}近期研究 | {about.}置顶文章 | {www.}博客页面 | {www.}置顶文章

news头部：
```js
---
category: news
layout: news
title: "SentryLab「blog markdown」语法介绍&批注"
author: bin4xin
---
```
event头部：
```js
---
layout: event
title: "「起源」：我与ERRORS"
date: 2019-09-11
time: 19:30-20:00
place: 合肥·安徽
author: Bin4xin

categories:
  - event
tags:
  - 笔记
  - 起源
---
```

blog头部：
```js
---
layout: post
title: "随笔记：Oracle数据库的渗透测试"
date: 2020-10-29
author: Bin4xin
categories:
    - blog
    - Sql-Inject
    - 笔记
permalink: /blog/2020/Oracle-sql/
---
```

help头部：
```js
---
layout: help
category: help
mirrorid: ShiroDeser
permalink: /help/ShiroDeser/
---
```
以上供参考
## 0x03 多样化展示信息

- 表格1效果如上：

```js
{: .table}
help | news | blog | events
-------|----------|----------|------
{about.}近期研究 | {about.}置顶文章 | {www.}博客页面 | {www.}置顶文章
同时配置category: news
```

- 表格2效果如下：

|    TYPE   |ASCII                          |HTML
|----------------|-------------------------------|-----------------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|

---
```js
|    TYPE   |ASCII                          |HTML
|----------------|-------------------------------|-----------------------------|
|Single backticks|`'Isn't this fun?'`            |'Isn't this fun?'            |
|Quotes          |`"Isn't this fun?"`            |"Isn't this fun?"            |
|Dashes          |`-- is en-dash, --- is em-dash`|-- is en-dash, --- is em-dash|
```
- 外部资源引用

链接: [link](https://www.csdn.net/).

图片: ![Alt](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9hdmF0YXIuY3Nkbi5uZXQvNy83L0IvMV9yYWxmX2h4MTYzY29tLmpwZw)

```js
链接: [link](https://www.csdn.net/).
图片: ![Alt](https://imgconvert.csdnimg.cn/aHR0cHM6Ly9hdmF0YXIuY3Nkbi5uZXQvNy83L0IvMV9yYWxmX2h4MTYzY29tLmpwZw)
```
## 0x04 如何改变文本的样式

*强调文本* _强调文本_

**加粗文本** __加粗文本__

~~删除文本~~

> 引用文本

```js
*强调文本* _强调文本_
**加粗文本** __加粗文本__
~~删除文本~~
> 引用文本
```
## 0x05 生成一个适合你的列表

- 项目1
  - 项目2
    - 项目3

- [ ] 未完成任务
- [x] 已完成任务

---
```js
- 项目1
  - 项目2
    - 项目3

- [ ] 未完成任务
- [x] 已完成任务
```

## 0x06 文章参考
为了方便各位理解，我这里放上了一篇篇幅较短的文章供各位参考

**[《博客2.0测试置顶文章》](/news/welcome-to-2.0-blog/)**

MARKDOWN代码：
```js
---
layout: news
title: "博客2.0测试置顶文章"
date: 2020-11-07
author: Bin4xin
category: news
---

这是一个测试置顶

* 考虑在公告窗口实现`置顶`操作
* 实操下来发现路由结构如下：
  - 新闻-公告窗口相互绑定`site.url/news`，`readmore`功能同样跳转;
  - 帮助-个人希望实现对于近期的一些研究，如`struts2,shiro`;但是部分功能路由和json文件对应的`site.url/help`路由暂时无法得知如何代码。

***
* 2020-11-08更新：
发现路由信息：
  - `_data/options.yml`配置文件可以选择配置`force_redirect_help`功能，即强制路由跳转至`help/*{redirect_url}`
  - 可以选择配置`unlist`选项、`new`显示等。
以上。
```

以上；希望能给各位有些帮助。
