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

## 参考

[使用Hexo+Github一步步搭建属于自己的博客](https://www.cnblogs.com/fengxiongZz/p/7707219.html)

[使用Travis CI自动部署Hexo到GitHub](https://dmego.me/2017/10/13/deylpoy-hexo-with-TravisCI.html)