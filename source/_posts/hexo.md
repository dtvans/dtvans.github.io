---
title: hexo
date: 2024-03-13 09:31:52
categories: 大器晚成
tags: [利器]
keywords: Hexo
description: Hexo博客的安装配置与使用
---

Hexo是快速、简洁且高效的博客框架

<!--more--> 

官网 https://hexo.io/zh-cn/

# 安装与配置

```bash
$ npm i hexo -g
$ npm update hexo -g
```

## deploy

需安装插件 `npm i hexo-deployer-git -s`, 配置 `_config.yml` 如下内容

```yaml
deploy:
  type: git
  repo: git@github.com:dtvans/dtvans.github.io.git
  branch: master
  message: 自定义提交消息，默认为Site updated: {{ now('YYYY-MM-DD HH:mm:ss') }}
```

可使用 `deploy` 指令进行部署，如下

```sh
$ hexo d
```

# 常用指令

```bash
# 新建文章
$ hexo n [layout] <title>

$ hexo n hello # 无参时由配置中的 `default_layout` 选项决定
$ hexo n post hello-post
$ hexo n page hello-page 
$ hexo n draft hello-draft

# 生成静态文件
$ hexo g
$ hexo g --watch # 监视文件变化

# 启动本地静态服务器
$ hexo s # 自动监视文件变化并更新
$ hexo s -s # 静态模式
$ hexo s -p 5000 # 指定端口
$ hexo s -i 127.0.0.1 # 指定绑定的ip
$ hexo s -o # 启动静态服务器并打开浏览器

# 清理缓存文件
$ hexo clean
```



# 标题头



```
title: 文章标题
layout: post
date: 2014-03-03 19:07:43
comments: true
categories: Blog
tags: [Hexo]
keywords: Hexo, Blog
description: 简单描述
```

