# Javascript Algorithms And Data Structures Certification

## Basic JavaScript

JavaScript is a high-level programming language that all modern web browsers support. It is also one of the core technologies of the web, along with HTML and CSS that you may have learned previously. This section will cover basic JavaScript programming concepts, which range from variables and arithmetic to objects and loops.

### 知识点

* Comment Your JavaScript Code
* Declare JavaScript Variables
* Storing Values with the Assignment Operator
* Initializing Variables with the Assignment Operator
* Understanding Uninitialized Variables
* Understanding Case Sensitivity in Variables
* Add Two Numbers with JavaScript
* Subtract One Number from Another with JavaScript
* Multiply Two Numbers with JavaScript
* Divide One Number by Another with JavaScript
* Increment a Number with JavaScript
* Decrement a Number with JavaScript
* Create Decimal Numbers with JavaScript
* Multiply Two Decimals with JavaScript
* Divide One Decimal by Another with JavaScript
* Finding a Remainder in JavaScript
* Compound Assignment With Augmented Addition
* Compound Assignment With Augmented Subtraction
* Compound Assignment With Augmented Multiplication
* Compound Assignment With Augmented Division
* Declare String Variables
* Escaping Literal Quotes in Strings
* Quoting Strings with Single Quotes
* Escape Sequences in Strings
* Concatenating Strings with Plus Operator
* Concatenating Strings with the Plus Equals Operator
* Constructing Strings with Variables
* Appending Variables to Strings
* Find the Length of a String
* Use Bracket Notation to Find the First Character in a String
* Understand String Immutability
* Use Bracket Notation to Find the Nth Character in a String
* Use Bracket Notation to Find the Last Character in a String
* Use Bracket Notation to Find the Nth-to-Last Character in a String
* Word Blanks
* Store Multiple Values in one Variable using JavaScript Arrays
* Nest one Array within Another Array
* Access Array Data with Indexes
* Modify Array Data With Indexes
* Access Multi-Dimensional Arrays With Indexes
* Manipulate Arrays With push()
* Manipulate Arrays With pop()
* Manipulate Arrays With shift()
* Manipulate Arrays With unshift()
* Shopping List
* Write Reusable JavaScript with Functions
* Passing Values to Functions with Arguments
* Global Scope and Functions
* Local Scope and Functions
* Global vs. Local Scope in Functions
* Return a Value from a Function with Return
* Understanding Undefined Value returned from a Function
* Assignment with a Returned Value
* Stand in Line
* Understanding Boolean Values
* Use Conditional Logic with If Statements
* Comparison with the Equality Operator
* Comparison with the Strict Equality Operator
* Practice comparing different values
* Comparison with the Inequality Operator
* Comparison with the Strict Inequality Operator
* Comparison with the Greater Than Operator
* Comparison with the Greater Than Or Equal To Operator
* Comparison with the Less Than Operator
* Comparison with the Less Than Or Equal To Operator
* Comparisons with the Logical And Operator
* Comparisons with the Logical Or Operator
* Introducing Else Statements
* Introducing Else If Statements
* Logical Order in If Else Statements
* Chaining If Else Statements
* Golf Code
* Selecting from Many Options with Switch Statements
* Adding a Default Option in Switch Statements
* Multiple Identical Options in Switch Statements
* Replacing If Else Chains with Switch
* Returning Boolean Values from Functions
* Return Early Pattern for Functions
* Counting Cards
* Build JavaScript Objects
* Accessing Object Properties with Dot Notation
* Accessing Object Properties with Bracket Notation
* Accessing Object Properties with Variables
* Updating Object Properties
* Add New Properties to a JavaScript Object
* Delete Properties from a JavaScript Object
* Using Objects for Lookups
* Testing Objects for Properties
* Manipulating Complex Objects
* Accessing Nested Objects
* Accessing Nested Arrays
* Record Collection
* Iterate with JavaScript While Loops
* Iterate with JavaScript For Loops
* Iterate Odd Numbers With a For Loop
* Count Backwards With a For Loop
* Iterate Through an Array with a For Loop
* Nesting For Loops
* Iterate with JavaScript Do...While Loops
* Profile Lookup
* Generate Random Fractions with JavaScript
* Generate Random Whole Numbers with JavaScript
* Generate Random Whole Numbers within a Range
* Use the parseInt Function
* Use the parseInt Function with a Radix
* Use the Conditional (Ternary) Operator
* Use Multiple Conditional (Ternary) Operators

### 重点学习

1. 注释

As you write code, you should regularly add comments to clarify the function of parts of your code. Good commenting can help communicate the intent of your code—both for others and for your future self.

```javascript
// This is an in-line comment.

/* This is a
multi-line comment */

// 函数注释

/**
 * 抓取远端API的结构
 * https://developers.douban.com/wiki/?title=movie_v2
 * @param  {String} api    api 根地址
 * @param  {String} path   请求路径
 * @param  {Objece} params 参数
 * @return {Promise}       包含抓取任务的Promise
 */
module.exports = function (api, path, params) {
  return new Promise((resolve, reject) => {
    wx.request({
      url: `${api}/${path}`,
      data: Object.assign({}, params),
      header: { 'Content-Type': 'json' },
      success: resolve,
      fail: reject
    })
  })
}
```
2. 变量、数据类型和运算符

In computer science, data is anything that is meaningful to the computer. JavaScript provides seven different data types which are `undefined, null, boolean, string, symbol, number, and object`.

Write variable names in JavaScript in camelCase.

理解浮点数在计算机的表示

```
十进制0.1计算机表示
 =>二进制为：0.0001100110011[0011…](循环0011,无限循环)   
 =>指数表示：尾数为1.1001100110011001100…1100（共52位，除了小数点左边的必须为1的数据），指数为-4（-4+1023 = 1019 二进制移码为 01111111011）,符号位为0  
 => 计算机存储为：0 01111111011 10011001100110011…11001  
 => 因为尾数最多52位，所以实际存储的值为0.00011001100110011001100110011001100110011001100110011001  
```
掌握数值运算

掌握字符串转义字符

掌握字符串操作

掌握数组操作

3. 函数

## ES6

## Regular Expressions
## Debugging
## Basic Data Structures
## Basic Algorithm Scripting
## Object Oriented Programming
## Functional Programming
## Intermediate Algorithm Scripting
## JavaScript Algorithms and Data Structures Projects