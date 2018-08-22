# Front End Libraries

## Introduction to the Bootstrap Challenges

* Use Responsive Design with Bootstrap Fluid Containers
* Make Images Mobile Responsive
* Center Text with Bootstrap
* Create a Bootstrap Button
* Create a Block Element Bootstrap Button
* Taste the Bootstrap Button Color Rainbow
* Call out Optional Actions with btn-info
* Warn Your Users of a Dangerous Action with btn-danger
* Use the Bootstrap Grid to Put Elements Side By Side
* Ditch Custom CSS for Bootstrap
* Use a span to Target Inline Elements
* Create a Custom Heading
* Add Font Awesome Icons to our Buttons
* Add Font Awesome Icons to all of our Buttons
* Responsively Style Radio Buttons
* Responsively Style Checkboxes
* Style Text Inputs as Form Controls
* Line up Form Elements Responsively with Bootstrap
* Create a Bootstrap Headline
* House our page within a Bootstrap container-fluid div
* Create a Bootstrap Row
* Split Your Bootstrap Row
* Create Bootstrap Wells
* Add Elements within Your Bootstrap Wells
* Apply the Default Bootstrap Button Style
* Create a Class to Target with jQuery Selectors
* Add id Attributes to Bootstrap Elements
* Label Bootstrap Wells
* Give Each Element a Unique id
* Label Bootstrap Buttons
* Use Comments to Clarify Code

### 重点学习

1. 响应式布局

```html
<div class="container">
  <div class="row">
    <div class="col-sm">
      One of three columns
    </div>
    <div class="col-sm">
      One of three columns
    </div>
    <div class="col-sm">
      One of three columns
    </div>
  </div>
</div>
```

2. 响应断点

```css
// Extra small devices (portrait phones, less than 576px)
// No media query for `xs` since this is the default in Bootstrap

// Small devices (landscape phones, 576px and up)
@media (min-width: 576px) { ... }

// Medium devices (tablets, 768px and up)
@media (min-width: 768px) { ... }

// Large devices (desktops, 992px and up)
@media (min-width: 992px) { ... }

// Extra large devices (large desktops, 1200px and up)
@media (min-width: 1200px) { ... }
```

3. 常用class

```html
**Images

Responsive images
<img src="..." class="img-fluid" alt="Responsive image">

Image thumbnails
<img src="..." alt="..." class="img-thumbnail">

Aligning images
<img src="..." class="rounded float-left" alt="...">
<img src="..." class="rounded float-right" alt="...">
<!-- 水平居中 -->
<img src="..." class="rounded mx-auto d-block" alt="...">

<div class="text-center">
  <img src="..." class="rounded" alt="...">
</div>


Picture
​<picture>
  <source srcset="..." type="image/svg+xml">
  <img src="..." class="img-fluid img-thumbnail" alt="...">
</picture>


**Text
<p class="text-justify">Ambitioni dedisse scripsisse iudicaretur. Cras mattis iudicium purus sit amet fermentum. Donec sed odio operae, eu vulputate felis rhoncus. Praeterea iter est quasdam res quas ex communi. At nos hinc posthac, sitientis piros Afros. Petierunt uti sibi concilium totius Galliae in diem certam indicere. Cras mattis iudicium purus sit amet fermentum.</p>
<p class="text-left">Left aligned text on all viewport sizes.</p>
<p class="text-center">Center aligned text on all viewport sizes.</p>
<p class="text-right">Right aligned text on all viewport sizes.</p>
```

4. 常用组件

```html

**Buttons

<button type="button" class="btn btn-outline-primary">Primary</button>
<button type="button" class="btn btn-primary btn-lg">Large button</button>
<button type="button" class="btn btn-primary btn-lg btn-block">Block level button</button>
```

5. Font Awesome


## Introduction to jQuery

Query's most recognizable characteristic is its dollar sign ($) syntax. With it, you can easily manipulate elements, create animations and handle input events.

* Learn How Script Tags and Document Ready Work
* Target HTML Elements with Selectors Using jQuery
* Target Elements by Class Using jQuery
* Target Elements by id Using jQuery
* Delete Your jQuery Functions
* Target the Same Element with Multiple jQuery Selectors
* Remove Classes from an Element with jQuery
* Change the CSS of an Element Using jQuery
* Disable an Element Using jQuery
* Change Text Inside an Element Using jQuery
* Remove an Element Using jQuery
* Use appendTo to Move Elements with jQuery
* Clone an Element Using jQuery
* Target the Parent of an Element Using jQuery
* Target the Children of an Element Using jQuery
* Target a Specific Child of an Element Using jQuery
* Target Even Elements Using jQuery
* Use jQuery to Modify the Entire Page

## Introduction to the Sass Challenges

Sass, or "Syntactically Awesome StyleSheets", is a language extension of CSS. 

Sass can extend the CSS language because it is a preprocessor. 

* Store Data with Sass Variables
* Nest CSS with Sass
* Create Reusable CSS with Mixins
* Use @if and @else to Add Logic To Your Styles
* Use @for to Create a Sass Loop
* Use @each to Map Over Items in a List
* Apply a Style Until a Condition is Met with @while
* Split Your Styles into Smaller Chunks with Partials
* Extend One Set of CSS Styles to Another Element

```scss
// Sass Variables

$main-fonts: Arial, sans-serif;
$headings-color: green;

//To use variables:
h1 {
  font-family: $main-fonts;
  color: $headings-color;
}

// Nest CSS with Sass
nav {
  background-color: red;

  ul {
    list-style: none;

    li {
      display: inline-block;
    }
  }
}

// Create Reusable CSS with Mixins
@mixin box-shadow($x, $y, $blur, $c){ 
  -webkit-box-shadow: $x, $y, $blur, $c;
  -moz-box-shadow: $x, $y, $blur, $c;
  -ms-box-shadow: $x, $y, $blur, $c;
  box-shadow: $x, $y, $blur, $c;
}

div {
  @include box-shadow(0px, 0px, 4px, #fff);
}

// Use @if and @else to Add Logic To Your Styles

@mixin text-effect($val) {
  @if $val == danger {
    color: red;
  }
  @else if $val == alert {
    color: yellow;
  }
  @else if $val == success {
    color: green;
  }
  @else {
    color: black;
  }
}


//  Use @for to Create a Sass Loop
@for $i from 1 through 12 {
  .col-#{$i} { width: 100%/12 * $i; }
}

// Use @each to Map Over Items in a List
@each $color in blue, red, green {
  .#{$color}-text {color: $color;}
}

$colors: (color1: blue, color2: red, color3: green);

@each $key, $color in $colors {
  .#{$color}-text {color: $color;}
}

// Apply a Style Until a Condition is Met with @while
$x: 1;
@while $x < 13 {
  .col-#{$x} { width: 100%/12 * $x;}
  $x: $x + 1;
}

// Split Your Styles into Smaller Chunks with Partials
// if all your mixins are saved in a partial named "_mixins.scss"
@import 'mixins'

// Extend One Set of CSS Styles to Another Element
.panel{
  background-color: red;
  height: 70px;
  border: 2px solid green;
}

.big-panel{
  @extend .panel;
  width: 150px;
  font-size: 2em;
}
```

### 重点学习

1. SASS变量
2. SASS嵌套语法
3. 类似函数的Mixins
4. 控制语句@if, @for, @while, @each
5. 文件组织和导入@import
6. 复用@extend

[Google FireBase的简单介绍和使用](https://www.jianshu.com/p/eeb760c63a53)

[解决FireBase login验证失败问题](https://www.jianshu.com/p/ad160afee2d8)

[github issue](https://github.com/firebase/firebase-tools/issues/155)

```
Update. Just made login working.

    run Git Bash or any Linux-like command line tool
    execute these commands, substitute your proxy instead

export HTTP_PROXY="http://proxy.XXXXXXXX.com:80/"
export HTTPS_PROXY="http://proxy.XXXXXXXX.com:80/"

    after this I was able to login using

firebase login --interactive

    useful links

```

[菜鸟Vue.js教程](http://www.runoob.com/vue2/vue-tutorial.html)

```html
<!-- 反转字符串 message.split('').reverse().join('') -->
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Vue 测试实例 - 菜鸟教程(runoob.com)</title>
<script src="https://cdn.bootcss.com/vue/2.2.2/vue.min.js"></script>
</head>
<body>
<div id="app">
  {{ message.split('').reverse().join('') }}
</div>

<script>
new Vue({
  el: '#app',
  data: {
    message: 'Runoob!'
  }
})
</script>
</body>
</html>
```

v-for 默认行为试着不改变整体，而是替换元素。迫使其重新排序的元素，你需要提供一个 key 的特殊属性：

`<div v-for="item in items" :key="item.id">  {{ item.text }}</div>`


### computed vs methods

我们可以使用 methods 来替代 computed，效果上两个都是一样的，但是 computed 是基于它的依赖缓存，只有相关依赖发生改变时才会重新取值。而使用 methods ，在重新渲染的时候，函数总会重新调用执行。

可以说使用 computed 性能会更好，但是如果你不希望缓存，你可以使用 methods 属性。

prop 是[单向绑定](https://vuejs.org/v2/guide/components.html#One-Way-Data-Flow)的：当父组件的属性变化时，将传导给子组件，但是不会反过来。

父组件是使用 props 传递数据给子组件，但如果子组件要把数据传递回去，就需要使用自定义事件！

[Vuex]( http://vuex.vuejs.org/en/)


### Vue.js 路由

```html
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>Vue 测试实例 - 菜鸟教程(runoob.com)</title>
<script src="https://cdn.bootcss.com/vue/2.4.2/vue.min.js"></script>
<script src="https://cdn.bootcss.com/vue-router/2.7.0/vue-router.min.js"></script>
</head>
<body>
<div id="app">
  <h1>Hello App!</h1>
  <p>
    <!-- 使用 router-link 组件来导航. -->
    <!-- 通过传入 `to` 属性指定链接. -->
    <!-- <router-link> 默认会被渲染成一个 `<a>` 标签 -->
    <router-link to="/foo">Go to Foo</router-link>
    <router-link to="/bar">Go to Bar</router-link>
  </p>
  <!-- 路由出口 -->
  <!-- 路由匹配到的组件将渲染在这里 -->
  <router-view></router-view>
</div>

<script>
// 0. 如果使用模块化机制编程，導入Vue和VueRouter，要调用 Vue.use(VueRouter)

// 1. 定义（路由）组件。
// 可以从其他文件 import 进来
const Foo = { template: '<div>foo</div>' }
const Bar = { template: '<div>bar</div>' }

// 2. 定义路由
// 每个路由应该映射一个组件。 其中"component" 可以是
// 通过 Vue.extend() 创建的组件构造器，
// 或者，只是一个组件配置对象。
// 我们晚点再讨论嵌套路由。
const routes = [
  { path: '/foo', component: Foo },
  { path: '/bar', component: Bar }
]

// 3. 创建 router 实例，然后传 `routes` 配置
// 你还可以传别的配置参数, 不过先这么简单着吧。
const router = new VueRouter({
  routes // （缩写）相当于 routes: routes
})

// 4. 创建和挂载根实例。
// 记得要通过 router 配置参数注入路由，
// 从而让整个应用都有路由功能
const app = new Vue({
  router
}).$mount('#app')

// 现在，应用已经启动了！
</script>
</body>
</html>
```