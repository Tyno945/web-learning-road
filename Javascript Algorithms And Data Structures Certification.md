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

* 理解浮点数在计算机的表示

```
十进制0.1计算机表示
 =>二进制为：0.0001100110011[0011…](循环0011,无限循环)   
 =>指数表示：尾数为1.1001100110011001100…1100（共52位，除了小数点左边的必须为1的数据），指数为-4（-4+1023 = 1019 二进制移码为 01111111011）,符号位为0  
 => 计算机存储为：0 01111111011 10011001100110011…11001  
 => 因为尾数最多52位，所以实际存储的值为0.00011001100110011001100110011001100110011001100110011001  
```
* 掌握数值运算

* 掌握字符串转义字符

* 掌握字符串操作

* 掌握数组操作

3. 函数

函数定义,函数参数，函数作用域，函数返回值

4. 理解队列

5. 掌握判断，掌握比较运算和逻辑运算

```
if (condition is true) {
  statement is executed
}
---------------------------

if (condition1) {
  statement1
} else if (condition2) {
  statement2
} else if (condition3) {
  statement3
. . .
} else {
  statementN
}
---------------------------

switch(num) {
  case value1:
    statement1;
    break;
  case value2:
    statement2;
    break;
...
  case valueN:
    statementN;
    break;
}
...
  default:
    defaultStatement;
    break;
```

6. 对象

对象定义，对象属性的查改增删

## ES6

ECMAScript is a standardized version of JavaScript with the goal of unifying the language's specifications and features. 

The most recent standardized version is called ECMAScript 6 (ES6), released in 2015. This new version of the language adds some powerful features that will be covered in this section of challenges, including:


* Arrow functions
* Classes
* Modules
* Promises
* Generators
* let and const

### 知识点

* Explore Differences Between the var and let Keywords
* Compare Scopes of the var and let Keywords
* Declare a Read-Only Variable with the const Keyword
* Mutate an Array Declared with const
* Prevent Object Mutation
* Use Arrow Functions to Write Concise Anonymous Functions
* Write Arrow Functions with Parameters
* Write Higher Order Arrow Functions
* Set Default Parameters for Your Functions
* Use the Rest Operator with Function Parameters
* Use the Spread Operator to Evaluate Arrays In-Place
* Use Destructuring Assignment to Assign Variables from Objects
* Use Destructuring Assignment to Assign Variables from Nested Objects
* Use Destructuring Assignment to Assign Variables from Arrays
* Use Destructuring Assignment with the Rest Operator to Reassign Array Elements
* Use Destructuring Assignment to Pass an Object as a Function's Parameters
* Create Strings using Template Literals
* Write Concise Object Literal Declarations Using Simple Fields
* Write Concise Declarative Functions with ES6
* Use class Syntax to Define a Constructor Function
* Use getters and setters to Control Access to an Object
* Understand the Differences Between import and require
* Use export to Reuse a Code Block
* Use * to Import Everything from a File
* Create an Export Fallback with export default
* Import a Default Export

### 重点学习

1. 用let和const声明变量

* 块级作用域
* 常量声明用大写字母，下划线分隔
* 利用Object.freeze函数使对象不可修改

2. 掌握箭头函数

* 高阶函数map(), filter(), and reduce()与箭头函数的配合

3. 函数默认参数，`...`rest运算符

```javascript
function howMany(...args) {
  return "You have passed " + args.length + " arguments.";
}
console.log(howMany(0, 1, 2)); // You have passed 3 arguments

/* 直接使用Math.max(arr)会返回NaN */
var arr = [6, 89, 3, 45];
var maximus = Math.max.apply(null, arr); // returns 89

const arr = [6, 89, 3, 45];
const maximus = Math.max(...arr); // returns 89
```
4. 掌握解构赋值

```javascript
const [a, b, ...arr] = [1, 2, 3, 4, 5, 7];
console.log(a, b); // 1, 2
console.log(arr); // [3, 4, 5, 7]

/* 函数参数是对象的解构赋值 */
const stats = {
  max: 56.78,
  standard_deviation: 4.34,
  median: 34.54,
  mode: 23.87,
  min: -0.75,
  average: 35.85
};
const half = (function() {
  "use strict"; // do not change this line

  // change code below this line
  return function half({max, min}) {
    // use function argument destructuring
    return (max + min) / 2.0;
  };
  // change code above this line

})();
console.log(stats); // should be object
console.log(half(stats)); // should be 28.015
```

5. 掌握模板字符串

6. 对象缩写

```javascript
const getMousePosition = (x, y) => ({
  x: x,
  y: y
});

const getMousePosition = (x, y) => ({ x, y });

const person = {
  name: "Taylor",
  sayHello: function() {
    return `Hello! My name is ${this.name}.`;
  }
};

const person = {
  name: "Taylor",
  sayHello() {
    return `Hello! My name is ${this.name}.`;
  }
};
```

7. 掌握`class`构造函数

8. 掌握`getter` 和 `setter`

9. 区分`import` and `require`，掌握`export`和`export default`

## Regular Expressions

Regular expressions are special strings that represent a search pattern. Also known as "regex" or "regexp", they help programmers match, search, and replace text.

### 知识点

* Using the Test Method
* Match Literal Strings
* Match a Literal String with Different Possibilities
* Ignore Case While Matching
* Extract Matches
* Find More Than the First Match
* Match Anything with Wildcard Period
* Match Single Character with Multiple Possibilities
* Match Letters of the Alphabet
* Match Numbers and Letters of the Alphabet
* Match Single Characters Not Specified
* Match Characters that Occur One or More Times
* Match Characters that Occur Zero or More Times
* Find Characters with Lazy Matching
* Find One or More Criminals in a Hunt
* Match Beginning String Patterns
* Match Ending String Patterns
* Match All Letters and Numbers
* Match Everything But Letters and Numbers
* Match All Numbers
* Match All Non-Numbers
* Restrict Possible Usernames
* Match Whitespace
* Match Non-Whitespace Characters
* Specify Upper and Lower Number of Matches
* Specify Only the Lower Number of Matches
* Specify Exact Number of Matches
* Check for All or None
* Positive and Negative Lookahead
* Reuse Patterns Using Capture Groups
* Use Capture Groups to Search and Replace
* Remove Whitespace from Start and End

## Debugging
## Basic Data Structures
## Basic Algorithm Scripting
## Object Oriented Programming
## Functional Programming
## Intermediate Algorithm Scripting
## JavaScript Algorithms and Data Structures Projects