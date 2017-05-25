---
title: hexo安装与配置
date: 2017-05-25 19:04:55
tags:
- node.js
- hexo
### 安装
前置条件：
1. git
2. Node.js
3. Github上创建新的blog

在上述安装完成后，在git Bash上执行：
```
npm install hexo-cli -g
```
安装完成后，在本地需要进行编写blog的文件目录下输入命令
```
npm init
hexo init
npm install
```
完成上述命令后，即可在本地运行博客
```
hexo s -g
```
在浏览器输入`http://localhost:4000`即可访问

### 配置

#### 配置文件为当前所在目录下的`_config.yml文件
```
#博客名称
title: 我的博客
#副标题
subtitle: 一天进步一点
#简介
description: 记录生活点滴
#博客作者
author: John Doe
#博客语言
language: zh-CN
#时区
timezone:

#博客地址,与申请的GitHub一致
url: http://elfwalk.github.io
root: /
#博客链接格式
permalink: :year/:month/:day/:title/
permalink_defaults:

source_dir: source
public_dir: public
tag_dir: tags
archive_dir: archives
category_dir: categories
code_dir: downloads/code
i18n_dir: :lang
skip_render:

new_post_name: :title.md # File name of new posts
default_layout: post
titlecase: false # Transform title into titlecase
external_link: true # Open external links in new tab
filename_case: 0
render_drafts: false
post_asset_folder: false
relative_link: false
future: true
highlight:
  enable: true
  line_number: true
  auto_detect: true
  tab_replace:

default_category: uncategorized
category_map:
tag_map:

#日期格式
date_format: YYYY-MM-DD
time_format: HH:mm:ss

#分页，每页文章数量
per_page: 10
pagination_dir: page

#博客主题
theme: landscape

#发布设置
deploy: 
  type: git
  #elfwalk改为你的github用户名
  repository: https://github.com/elfwalk/elfwalk.github.io.git
  branch: master
```
> 注意事项：上述输入的文字，必须在每个`:`后留一个空格，否则会报错

#### 写第一篇文章
```
hexo new 'hexo'
```
然后在`当前目录\source\_posts`下，找到新建立的`hexo.md`进行编辑
```
title: hello
date: 2015-07-01 22:37:23
categories:
  - 日志
  - 二级目录
tags:
  - hello
---

摘要:
<!--more-->
正文:
```

#### 发布
```
npm install hexo-deployer-get --save
hexo d -g
```

参考网页：
[1]. [CSDN-零基础免费搭建个人博客-hexo+github](http://blog.csdn.net/jzooo/article/details/46781805)
[2]. [简书-Hexo安装和配置](http://www.jianshu.com/p/b7886271e21a)