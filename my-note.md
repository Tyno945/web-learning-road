## Vue.js 2 and Bootstrap 4 Web Development


1. 开发环境准备，安装VScode，安装node及npm
2. 安装vue-cli

`npm install --global vue-cli`

在国内使用淘宝NPM镜像会快很多。参考[http://npm.taobao.org/](http://npm.taobao.org/)

```
$ npm install -g cnpm --registry=https://registry.npm.taobao.org
$ cnpm install [name]
```
3. 搭建一个Vue项目


`vue init <template-name><project-name>`

The following templates are available:

* **webpack**: This is a full-featured webpack setup with vue-loader. It supports hot reload, linting, testing, all kind of pre-processors, and so on.
* **webpack-simple**: This is a simple webpack setup that is useful for quick prototyping.
* **browserify**: This is a full-featured browserify setup with vueify that also supports hot reload, linting, and unit testing.
* **browserify-simple**: This is a simple browserify setup with vueify that can be used for quick prototyping.
* **simple**: This generates a simple HTML page that includes Vue.js. It is perfect for quick feature exploration.

`vue init webpack my-project`

    在国内直接安装会很慢，先手动安装webpack包。
    $ cnpm install webpack --save-dev
    $ vue init webpack my-project

4. 了解Vue项目的目录结构

5. 学习并掌握Vue

* [参考菜鸟Vue.js教程](http://www.runoob.com/vue2/vue-tutorial.html)
* [官方文档](https://vuejs.org/)