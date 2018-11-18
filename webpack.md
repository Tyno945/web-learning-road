# Webpack 学习

[浅入浅出webpack](https://juejin.im/post/5afa9cd0f265da0b981b9af9)

## 基础搭建

1. 新建一个空文件夹webpack-test，运行npm init生成package.json文件
2. 同时全局和本地安装webpack，webpack-dev-server，webpack-cli

```
npm i webpack webpack-dev-server webpack-cli -g
npm i webpack webpack-dev-server webpack-cli --save-dev
```

3. 新建webpack.config.js文件

```js
module.exports = {
  entry: './main.js',
  output: {
    filename: 'bundle.js'
  }
};

```
4. 新建main.js

```js
document.write('<h1>Hello World</h1>');
```

5. 新建index.html

```html
<html>
  <body>
    <script type="text/javascript" src="bundle.js"></script>
  </body>
</html>
```

6. 使用webpack命令编译,使用webpack-dev-server运行本地web服务器

* `webpack` – building for development
* `webpack -p` – building for production (minification)
* `webpack --watch` – for continuous incremental building
* `webpack -d` – including source maps
* `webpack --colors` – making building output pretty

7. 在package.json中自定义scripts脚本

```json
// package.json
{
  // ...
  "scripts": {
    "dev": "webpack-dev-server --devtool eval --progress --colors",
    "deploy": "NODE_ENV=production webpack -p"
  },
  // ...
}
```


## 遇到问题
1. [升级node.js和npm](https://segmentfault.com/a/1190000009025883)

```bash
# 升级node.js
npm install -g n
n stable
# 升级npm
sudo npm install npm@latest -g
```

2. [安装webpack-cli](https://segmentfault.com/a/1190000013699050)

3. demo08 npm run build错误

webpack版本和html-webpack-plugin版本不兼容，均升级到最新版即可