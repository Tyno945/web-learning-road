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

## 参考

[使用Hexo+Github一步步搭建属于自己的博客](https://www.cnblogs.com/fengxiongZz/p/7707219.html)

[使用Travis CI自动部署Hexo到GitHub](https://dmego.me/2017/10/13/deylpoy-hexo-with-TravisCI.html)