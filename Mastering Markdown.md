## 什么是Markdown？

Markdown是一种轻量及易用的标记语法，它可以使普通文本内容具有一定的格式。

Markdown 的优点如下：

* 纯文本，所以兼容性极强，可以用所有文本编辑器打开。
* 让你专注于文字而不是排版。
* 格式转换方便，Markdown 的文本你可以轻松转换为 html、电子书等。
* Markdown 的标记语法有极好的可读性。

## Markdown语法

### 标题

```md
# This is an <h1> tag
## This is an <h2> tag
###### This is an <h6> tag
```

### 强调

```md
*This text will be italic*
_This will also be italic_

**This text will be bold**
__This will also be bold__

_You **can** combine them_
```

### 列表

```md
## Unordered
* Item 1
* Item 2
  * Item 2a
  * Item 2b

- Dashes work just as well
- And if you have sub points, put two spaces before the dash or star:
  - Like this
  - And this

## Ordered
1. Item 1
1. Item 2
1. Item 3
   1. Item 3a
   1. Item 3b
```

### 图片

```md
![GitHub Logo](/images/logo.png)
Format: ![Alt Text](url)
```

### 链接

```md
[GitHub](http://github.com)
Format: [Alt Text](url)
```

### 引用

```md
As Kanye West said:

> We're living the future so
> the present is our past.
```

### 代码

```md
There are many different ways to style code with GitHub's markdown. If you have inline code blocks, wrap them in backticks: `var example = true`.  If you've got a longer block of code, you can indent with four spaces:

    if (isAwesome){
      return true
    }

GitHub also supports something called code fencing, which allows for multiple lines without indentation:

    ```
    if (isAwesome){
      return true
    }
    ```

And if you'd like to use syntax highlighting, include the language:

    ```javascript
    if (isAwesome){
      return true
    }
    ```
```

### 任务清单

```md
- [x] This is a complete item
- [ ] This is an incomplete item
```

### 表格

```md
| Tables | Are | Cool | 
| ------------- |:-------------:| -----:| 
| col 3 is | right-aligned | $1600 | 
| col 2 is | centered | $12 | 
| zebra stripes | are neat | $1 |
```

| Tables | Are | Cool | 
| ------------- |:-------------:| -----:| 
| col 3 is | right-aligned | $1600 | 
| col 2 is | centered | $12 | 
| zebra stripes | are neat | $1 |

### 表情符号

```md
:sparkles: :camel: :boom:
```

## GitHub Flavored Markdown（GFM）

GitHub.com使用自己的Markdown语法版本[GFM](https://help.github.com/articles/basic-writing-and-formatting-syntax/)，它提供了一组额外的有用特性，其中许多特性使得在GitHub.com上处理内容变得更加容易。

## 参考

[Mastering Markdown](https://guides.github.com/features/mastering-markdown/)

[献给写作者的 Markdown 新手指南](https://www.jianshu.com/p/q81RER)

[Markdown写作浅谈](https://www.jianshu.com/p/PpDNMG)