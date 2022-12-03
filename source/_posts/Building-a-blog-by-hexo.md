---
title: Building a blog by hexo
date: 2022-11-30 22:41:50
tags:
  - blog
categories:
  - Tool
---

Sometimes, when alonescar records somthing, he needs a tool to fastly show it.

[Hexo](https://hexo.io/zh-cn/index.html) is that tool.

This post is to record how to use `hexo` to build a blog and show posts.

alonescar hope the post:
* fastly
* easily
* simply

<!--more-->

## Hexo is based on `node.js`
So we need `node.js` environment

## Install `hexo`

```
sudo npm i hexo-cli -g
```

If you have some errors or wait much time, you can choose not install it globally.

```
npm i hexo-cli
```

Then you need to use `./node_modules/hexo-cli/bin/hexo` to replace `hexo`

## Init blog
```
hexo init blogname
cd blogname
npm i
```
