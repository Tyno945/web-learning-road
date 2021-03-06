# Hexo

## What is Hexo?

[Hexo](https://hexo.io/) is a fast, simple and powerful blog framework. You write posts in Markdown (or other languages) and Hexo generates static files with a beautiful theme in seconds.

## Installation and initialization

### Requirements
Installing Hexo is quite easy. However, you do need to have a couple of other things installed first:
* Node.js
* Git

If your computer already has these, congratulations! Just install Hexo with npm:

    $ npm install -g hexo-cli

### Setup & Configuration

Once Hexo is installed, run the following commands to initialise Hexo in the target `<folder>`.

```
$ hexo init <folder>
$ cd <folder>
$ npm install
```

You can modify site settings in `_config.yml` or in an alternate config file.

### Commands

[reference](https://hexo.io/docs/commands)

## Basic Usage

### Writing

There are three default layouts in Hexo: `post, page and draft`. 

#### write a draft

    $ hexo new draft <title>
    $ hexo publish [layout] <title>

#### write a post

To create a new post, you can run the following command:

    $ hexo new [post] <title>

#### write a page

    $ hexo new page <title>

### Front-matter

Front-matter is a block of YAML or JSON at the beginning of the file that is used to configure settings for your writings. 

### Data Files

Sometimes you may need to use some data in templates which is not directly available in your posts, or you want to reuse the data elsewhere. For such use cases, Hexo 3 introduced the new Data files. This feature loads YAML or JSON files in source/_data folder so you can use them in your site.

### Server

Your website will run at http://localhost:4000 by default. When the server is running, Hexo will watch for file changes and update automatically so it’s not necessary to manually restart the server.

    $ hexo server

In static mode, only files in the public folder will be served and file watching is disabled. You have to run hexo generate before starting the server. Usually used in production.

    $ hexo server -s

### Generating

Generating static files with Hexo is quite easy and fast.

    $ hexo generate

Deploy After Generating

    $ hexo generate --deploy
    $ hexo deploy --generate

### Deployment

1.Install hexo-deployer-git.

    $ npm install hexo-deployer-git --save

2.Edit _config.yml

```yml
deploy:
  type: git   
  repo: <repository url>  #https://bitbucket.org/JohnSmith/johnsmith.bitbucket.io
  branch: [branch] #published
  message: [message]  #leave this blank
```
3.Upload your site: `hexo clean && hexo deploy`

## Customization

### Permalinks

You can specify the permalinks for your site in `_config.yml` or in the front-matter for each post.

#### Examples

Given a post named `hello-world.md` in the `source/_posts` folder with the following content.

``` yaml
title: Hello World
date: 2013-07-14 17:01:34
categories:
- foo
- bar
```

Setting | Result
--- | ---
`:year/:month/:day/:title/` | 2013/07/14/hello-world
`:year-:month-:day-:title.html` | 2013-07-14-hello-world.html
`:category/:title` | foo/bar/hello-world

### Themes

To start using your theme, modify the `theme` setting in your site’s `_config.yml`. A theme should have the following structure:

``` plain
.
├── _config.yml
├── languages
├── layout
├── scripts
└── source
```

### Templates

[Templates](https://hexo.io/docs/templates) define the presentation of your website by describing what each page should look like.

### Variables

#### Global Variables

Variable | Description | Type
--- | --- | ---
`site` | Sitewide information. | `object`; see [Site Variables]
`page` | Page specific information and custom variables set in front-matter. | `object`; see [Page Variables]
`config` | Site configuration. | `object` (your site's _config file)
`theme` | Theme configuration. Inherits from site configuration. | `object` (your theme's _config file)
`_` (single underscore) | Lodash library | see [Lodash](https://lodash.com/  "Lodash" target="_blank") documentation
`path` | Path of current page | `string`
`url` | Full URL of current page | `string`
`env` | Environment variables | ???

### Helpers

Helpers are used in templates to help you insert snippets quickly.

**Examples:**

``` js
<%- css('style.css') %>
// <link rel="stylesheet" href="/style.css" type="text/css">

<%- css(['style.css', 'screen.css']) %>
// <link rel="stylesheet" href="/style.css" type="text/css">
// <link rel="stylesheet" href="/screen.css" type="text/css">
```

### Internationalization (i18n)

You can use internationalization to present your site in different languages. The default language is set by modifying the `language` setting in `_config.yml`.

Language files can be YAML or JSON files. You should put them into the `languages` folder in the theme. 

``` yaml
language: zh-tw

language:
- zh-tw
- en
```

### Plugins

Hexo has a powerful plugin system, which makes it easy to extend functions without modifying the source code of the core module. 

## 高级技巧

### 部署发布到多个服务器

```yaml
deploy:
  type: git
  repository: 
    github: git@github.com:Tyno945/Tyno945.github.io.git
    coding: git@git.dev.tencent.com:Felix945/Felix945.git
  branch: master
```
配置好后一键部署：

    $ hexo clean && hexo g -d

部署成功的前提是已经配置好github和coding的SSH，并通过命令`$ ssh -T git@git.dev.tencent.com`建立好首次通信。

### 永久链接更改

文章的front matter设置一个新的变量english_title，修改博文的URL显示为english_title，`permalink: :year/:month/:day/:english_title/`，便于修改中文标题

```yaml
---
title: Hexo搭建博客系列：（三）使用MarkDown和七牛云写博文
english_title: Hexo3    #注意连接符是下划线
date: 2017-06-13 13:26:55
tags: [Hexo系列, MarkDown+七牛云, 有道云笔记] 
categories: Hexo系列
---
```

## 参考

[从0到1搭建一个属于自己的博客网站(总纲)](https://www.jianshu.com/p/166339826a7a)

[Hexo+GitHub搭建博客网站](https://blog.csdn.net/wsmrzx/article/details/81477123)

[使用Hexo+Github一步步搭建属于自己的博客](https://www.cnblogs.com/fengxiongZz/p/7707219.html)

[使用Travis CI自动部署Hexo到GitHub](https://dmego.me/2017/10/13/deylpoy-hexo-with-TravisCI.html)

[Hexo主题学习](http://theme-next.iissnan.com/)

[hexo博客同时部署至github和Coding](https://blog.csdn.net/u011303443/article/details/51509351)

[hexo添加文章更新时间](https://www.jianshu.com/p/ae3a0666e998)