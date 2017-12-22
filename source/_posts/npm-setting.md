---
title: npm淘宝源设置
date: 2017-05-25 19:25:03
tags:
- mpm
- node.js
- 前端
---
### npm淘宝源设置
1. 通过config命令
```
npm config set registry https://registry.npm.taobao.org 
npm info underscore 
```
1. 命令行指定
```
npm --registry https://registry.npm.taobao.org info underscore 
```
1. 编辑npm所在目录的npmrc文件中修改
   Windows所在的目录一般默认在`C:\Users\Administrator\AppData\Roaming\npm\etc`
   Linux所在的目录为~/
```
registry = https://registry.npm.taobao.org
```

### nvm安装与配置
参考：
1. [推酷-使用nvm管理不同版本的node与npm](http://www.tuicool.com/articles/Vzquy2)

### npm淘宝源与node淘宝源
[npm淘宝镜像](http://npm.taobao.org/)