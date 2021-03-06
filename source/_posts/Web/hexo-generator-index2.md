---
title: Hexo带过滤功能的首页插件
date: 2016-07-21 20:40:30
category: [Web]
tags: [Hexo, Node.js]
toc: true
---
## 简介

带过滤功能的[Hexo]首页生成器插件。在官方的首页生成器基础上添加了过滤指定分类/标签的功能。比如，在首页只显示指定分类下面的文章列表。

[English](https://github.com/Jamling/hexo-generator-index2/blob/master/README.md)

## 安装

``` bash
$ npm install hexo-generator-index2 --save
$ npm uninstall hexo-generator-index --save
```

## 配置

``` yaml
index_generator:
  per_page: 10
  order_by: -date
  include:
    - category Web # 只包含Web分类下的文章
  exclude:
    - tag Hexo # 不包含标签为Hexo的文章

```

- **per_page**: Posts displayed per page. (0 = disable pagination)
- **order_by**: Posts order. (Order by date descending by default)
- **include**: Posts filter include option
- **exclude**: Posts filter exclude option

除了include和exclude，其它如<var>per_page</var>和<var>order_by</var>都是原有的官方首页生成器选项，不必更改。

Include/exclude 选项格式为`属性 值`（注意，属性与值中间有个英文的空格），可选的属性有：

- category: 文章分类
- tag: 文章标签
- path: 文章源路径


## 传送门

https://github.com/Jamling/hexo-generator-index2

[Hexo]: http://hexo.io/
