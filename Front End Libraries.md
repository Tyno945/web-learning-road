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

### 重点学习

1. document ready function

```html
<script>
  $(document).ready(function() {

  });
</script>
```
2. 掌握Jquery选择器

```javascript
$(".target:nth-child(3)").addClass("animated bounce");
$(".target:odd").addClass("animated shake");
$("body").addClass("animated hinge");
```

3. 常用方法

```javascript
// .addClass()
$(document).ready(function() {
    $("button").addClass("animated bounce");
    $(".well").addClass("animated shake");
    $("#target3").addClass("animated fadeOut");
  });

// .removeClass()

$("button").removeClass("btn-default");

// Change the CSS .css()

$("#target1").css("color", "blue");

//  .prop() that allows you to adjust the properties of elements

$("button").prop("disabled", true);

// 修改Text和HTML text()和html()

$("h3").html("<em>jQuery Playground</em>");

// .remove() that will remove an HTML element entirely

$("#target4").remove();

//  Use appendTo to Move Elements .appendTo()

$("#target4").appendTo("#left-well");

// Clone an Element .clone() that makes a copy of an element

$("#target2").clone().appendTo("#right-well");

//  parent() that allows you to access the parent of whichever element you've selected

$("#left-well").parent().css("background-color", "blue");

// children() that allows you to access the children of whichever element you've selected

$("#left-well").children().css("color", "blue");
```


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


## Introduction to the React Challenges

React combines HTML with JavaScript functionality to create its own markup language, JSX.With JSX, it is used to create components, handle state and props, utilize event listeners and certain life cycle methods to update data as it changes.

* Create a Simple JSX Element
* Create a Complex JSX Element
* Add Comments in JSX
* Render HTML Elements to the DOM
* Define an HTML Class in JSX
* Learn About Self-Closing JSX Tags
* Create a Stateless Functional Component
* Create a React Component
* Create a Component with Composition
* Use React to Render Nested Components
* Compose React Components
* Render a Class Component to the DOM
* Write a React Component from Scratch
* Pass Props to a Stateless Functional Component
* Pass an Array as Props
* Use Default Props
* Override Default Props
* Use PropTypes to Define the Props You Expect
* Access Props Using this.props
* Review Using Props with Stateless Functional Components
* Create a Stateful Component
* Render State in the User Interface
* Render State in the User Interface Another Way
* Set State with this.setState
* Bind 'this' to a Class Method
* Use State to Toggle an Element
* Write a Simple Counter
* Create a Controlled Input
* Create a Controlled Form
* Pass State as Props to Child Components
* Pass a Callback as Props
* Use the Lifecycle Method componentWillMount
* Use the Lifecycle Method componentDidMount
* Add Event Listeners
* Manage Updates with Lifecycle Methods
* Optimize Re-Renders with shouldComponentUpdate
* Introducing Inline Styles
* Add Inline Styles in React
* Use Advanced JavaScript in React Render Method
* Render with an If/Else Condition
* Use && for a More Concise Conditional
* Use a Ternary Expression for Conditional Rendering
* Render Conditionally from Props
* Change Inline CSS Conditionally Based on Component State
* Use Array.map() to Dynamically Render Elements
* Give Sibling Elements a Unique Key Attribute
* Use Array.filter() to Dynamically Filter an Array
* Render React on the Server with renderToString

### 重点学习

1. JSX基本语法规则

* JSX使用Babel来编译成

* 在花括号里直接写JavaScript`{ 'this is treated as JavaScript code' }`

* JSX只能赋值一个元素，多个元素必须内嵌到一个母元素

* 注释{/* */}

* React's rendering API known as ReactDOM

```JSX
const JSX = (
  <div>
    <h1>Hello World</h1>
    <p>Lets render this to the DOM</p>
  </div>
);

ReactDOM.render(JSX, document.getElementById("challenge-node"));
```

* 类命名，JSX uses className,用camelCase规则

* JSX Tags must Self-Closing

 > A `<div>`, on the other hand, can be written as `<div />` or `<div></div>`. The difference is that in the first syntax version there is no way to include anything in the `<div />`.

1. 组件

```javascript
// a Stateless Functional Component
const DemoComponent = function() {
  return (
    <div className='customClass' />
  );
};

// Create a React Component
class Kitten extends React.Component {
  constructor(props) {
    super(props);
  }

  render() {
    return (
      <h1>Hi</h1>
    );
  }
}


const ChildComponent = () => {
  return (
    <div>
      <p>I am the child</p>
    </div>
  );
};

// compose multiple React components together
class ParentComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>I am the parent</h1>
        { /* change code below this line */ }
        <ChildComponent />

        { /* change code above this line */ }
      </div>
    );
  }
};

// Compose React Components
class Fruits extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h2>Fruits:</h2>
        { /* change code below this line */ }
          <NonCitrus />
          <Citrus />
         { /* change code above this line */ }
      </div>
    );
  }
};

class TypesOfFood extends React.Component {
  constructor(props) {
     super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        { /* change code below this line */ }
        <Fruits />
        { /* change code above this line */ }
        <Vegetables />
      </div>
    );
  }
};


// Render a Class Component to the DOM
class TypesOfFood extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h1>Types of Food:</h1>
        {/* change code below this line */}
          <Fruits />
          <Vegetables />
        {/* change code above this line */}
      </div>
    );
  }
};

// change code below this line
ReactDOM.render(<TypesOfFood />, document.getElementById("challenge-node"))
```

3. 组件参数

```javascript
// 传递参数到函数组件
const CurrentDate = (props) => {
  return (
    <div>
      { /* change code below this line */ }
      <p>The current date is: {props.date}</p>
      { /* change code above this line */ }
    </div>
  );
};

class Calendar extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h3>What date is it?</h3>
        { /* change code below this line */ }
        <CurrentDate date={Date()} />
        { /* change code above this line */ }
      </div>
    );
  }
};

// 传递数组参数
const ChildComponent = (props) => <p>{props.colors.join(', ')}</p>

<ParentComponent>
  <ChildComponent colors={["green", "blue", "red"]} />
</ParentComponent>


// 默认参数和规定参数类型
const Items = (props) => {
  return <h1>Current Quantity of Items in Cart: {props.quantity}</h1>
};

Items.propTypes = {
  quantity: PropTypes.number.isRequired
};

Items.defaultProps = {
  quantity: 0
};

class ShoppingCart extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return <Items /> 
  }
};

// 传递参数到类组件
class ReturnTempPassword extends React.Component {
  constructor(props) {
    super(props);

  }
  render() {
    return (
        <div>
            { /* change code below this line */ }
            <p>Your temporary password is: <strong>{this.props.tempPassword}</strong></p>
            { /* change code above this line */ }
        </div>
    );
  }
};

class ResetPassword extends React.Component {
  constructor(props) {
    super(props);

  }
  render() {
    return (
        <div>
          <h2>Reset Password</h2>
          <h3>We've generated a new temporary password for you.</h3>
          <h3>Please reset this password from your account settings ASAP.</h3>
          { /* change code below this line */ }
          <ReturnTempPassword tempPassword="11111111" />
          { /* change code above this line */ }
        </div>
    );
  }
};
```

4. 状态

```javascript
// 初始化状态及使用状态
class StatefulComponent extends React.Component {
  constructor(props) {
    super(props);
    // initialize state here
    this.state = {
      name: "Felix"
    };
  }
  render() {
    const name = this.state.name;
    return (
      <div>
        <h1>{name}</h1>
      </div>
    );
  }
};

// 使用类方法更改状态

class Counter extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
    // change code below this line
    this.increment = this.increment.bind(this);
    this.decrement = this.decrement.bind(this);
    this.reset = this.reset.bind(this);
    // change code above this line
  }
  // change code below this line
  increment(){
    this.setState({
      count: this.state.count + 1
    })
  }
  decrement(){
    this.setState({
      count: this.state.count - 1
    })
  }
  reset(){
    this.setState({
      count: 0
    })
  }
  // change code above this line
  render() {
    return (
      <div>
        <button className='inc' onClick={this.increment}>Increment!</button>
        <button className='dec' onClick={this.decrement}>Decrement!</button>
        <button className='reset' onClick={this.reset}>Reset</button>
        <h1>Current Count: {this.state.count}</h1>
      </div>
    );
  }
};
```

5. 事件触发状态变更

```javascript
class MyForm extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      input: '',
      submit: ''
    };
    this.handleChange = this.handleChange.bind(this);
    this.handleSubmit = this.handleSubmit.bind(this);
  }
  handleChange(event) {
    this.setState({
      input: event.target.value
    });
  }
  handleSubmit(event) {
    // change code below this line
    event.preventDefault()
    this.setState({
      submit: this.state.input
    });
    // change code above this line
  }
  render() {
    return (
      <div>
        <form onSubmit={this.handleSubmit}>
          { /* change code below this line */ }
          <input type='input' value={this.state.input} onChange={this.handleChange} />
          { /* change code above this line */ }
          <button type='submit'>Submit!</button>
        </form>
        { /* change code below this line */ }
        <h1>{this.state.submit}</h1>
        { /* change code above this line */ }
      </div>
    );
  }
};

// 母组件和子组件的数据传输
class MyApp extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      inputValue: ''
    }
    this.handleChange = this.handleChange.bind(this);
  }
  handleChange(event) {
    this.setState({
      inputValue: event.target.value
    });
  }
  render() {
    return (
       <div>
        { /* change code below this line */ }
        <GetInput input={this.state.inputValue} handleChange={this.handleChange}/>
        <RenderInput input={this.state.inputValue} />
        { /* change code above this line */ }
       </div>
    );
  }
};

class GetInput extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h3>Get Input:</h3>
        <input
          value={this.props.input}
          onChange={this.props.handleChange}/>
      </div>
    );
  }
};

class RenderInput extends React.Component {
  constructor(props) {
    super(props);
  }
  render() {
    return (
      <div>
        <h3>Input Render:</h3>
        <p>{this.props.input}</p>
      </div>
    );
  }
};
```

6. 组件的生命周期方法

* componentWillMount()

* componentDidMount()

* componentWillReceiveProps()

* shouldComponentUpdate()

* componentWillUpdate()

* componentDidUpdate()

* componentWillUnmount()

```javascript
// componentWillMount()
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
  }
  componentWillMount() {
    // change code below this line
    console.log("Hello");
    // change code above this line
  }
  render() {
    return <div />
  }
};

// componentDidMount()
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      activeUsers: null
    };
  }
  componentDidMount() {
    setTimeout( () => {
      this.setState({
        activeUsers: 1246
      });
    }, 1000);
  }
  render() {
    return (
      <div>
        <h1>Active Users: { this.state.activeUsers }</h1>
      </div>
    );
  }
};

// Add Event Listeners
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      message: ''
    };
    this.handleEnter = this.handleEnter.bind(this);
    this.handleKeyPress = this.handleKeyPress.bind(this);
  }
  // change code below this line
  componentDidMount() {
    document.addEventListener("keydown", this.handleKeyPress);
  }
  componentWillUnmount() {
    document.removeEventListener("keydown", this.handleKeyPress);
  }
  // change code above this line
  handleEnter() {
    this.setState({
      message: this.state.message + 'You pressed the enter key! '
    });
  }
  handleKeyPress(event) {
    if (event.keyCode === 13) {
      this.handleEnter();
    }
  }
  render() {
    return (
      <div>
        <h1>{this.state.message}</h1>
      </div>
    );
  }
};

// Manage Updates componentWillReceiveProps()
class Dialog extends React.Component {
  constructor(props) {
    super(props);
  }
  componentWillUpdate() {
    console.log('Component is about to update...');
  }
  // change code below this line
  componentWillReceiveProps(nextProps) {
    console.log(this.props);
    console.log(nextProps);
  }
  componentDidUpdate() {
    console.log('component has updated');
  }
  // change code above this line
  render() {
    return <h1>{this.props.message}</h1>
  }
};

class Controller extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      message: 'First Message'
    };
    this.changeMessage = this.changeMessage.bind(this);
  }
  changeMessage() {
    this.setState({
      message: 'Second Message'
    });
  }
  render() {
    return (
      <div>
        <button onClick={this.changeMessage}>Update</button>
        <Dialog message={this.state.message}/>
      </div>
    );
  }
};

// shouldComponentUpdate() The method must return a boolean value that tells React whether or not to update the component
class OnlyEvens extends React.Component {
  constructor(props) {
    super(props);
  }
  shouldComponentUpdate(nextProps, nextState) {
    console.log('Should I update?');
     // change code below this line
    return nextProps.value % 2 == 0 ? true : false;
     // change code above this line
  }
  componentWillReceiveProps(nextProps) {
    console.log('Receiving new props...');
  }
  componentDidUpdate() {
    console.log('Component re-rendered.');
  }
  render() {
    return <h1>{this.props.value}</h1>
  }
};

class Controller extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      value: 0
    };
    this.addValue = this.addValue.bind(this);
  }
  addValue() {
    this.setState({
      value: this.state.value + 1
    });
  }
  render() {
    return (
      <div>
        <button onClick={this.addValue}>Add</button>
        <OnlyEvens value={this.state.value}/>
      </div>
    );
  }
};
```

## Introduction to the Redux Challenges

Redux is a predictable state container for JavaScript apps.

* Create a Redux Store
* Get State from the Redux Store
* Define a Redux Action
* Define an Action Creator
* Dispatch an Action Event
* Handle an Action in the Store
* Use a Switch Statement to Handle Multiple Actions
* Use const for Action Types
* Register a Store Listener
* Combine Multiple Reducers
* Send Action Data to the Store
* Use Middleware to Handle Asynchronous Actions
* Write a Counter with Redux
* Never Mutate State
* Use the Spread Operator on Arrays
* Remove an Item from an Array
* Copy an Object with Object.assign


```javascript
const INCREMENT = 'INCREMENT'; // define a constant for increment action types
const DECREMENT = 'DECREMENT'; // define a constant for decrement action types

const counterReducer = (state = 0, action) => {
    switch (action.type) {
        case INCREMENT:
            return state + 1;

        case DECREMENT:
            return state - 1;
        
        default:
            return state;
    }
}; // define the counter reducer which will increment or decrement the state based on the action it receives

const incAction = () => {
    return {
        type: INCREMENT
    };
}; // define an action creator for incrementing

const decAction = () => {
    return {
        type: DECREMENT
    };
}; // define an action creator for decrementing

const store = Redux.createStore(counterReducer); // define the Redux store here, passing in your reducers

store.dispatch(incAction());
console.log(store.getState());
store.dispatch(decAction());
console.log(store.getState());
```

### 重点学习

1. Redux Store的创建和获取

```javascript
// In Redux, there is a single state object that's responsible for the entire state of your application

const reducer = (state = 5) => {
  return state;
}

// Redux methods are available from a Redux object
// For example: Redux.createStore()

const store = Redux.createStore(reducer)

// Get State from the Redux Store
const store = Redux.createStore(
  (state = 5) => state
);

// change code below this line
let currentState = store.getState()
```
2. 动作actions

```javascript
// In Redux, all state updates are triggered by dispatching actions. An action is simply a JavaScript object that contains information about an action event that has occurred.
const action = {
  type: 'LOGIN'
}
// An action creator is simply a JavaScript function that returns an action.
function actionCreator() {
  return action;
}

// Dispatch an Action Event
const store = Redux.createStore(
  (state = {login: false}) => state
);

const loginAction = () => {
  return {
    type: 'LOGIN'
  }
};

// Dispatch the action here:
store.dispatch(loginAction());


// Reducers in Redux are responsible for the state modifications that take place in response to actions. The reducer is simply a pure function that takes state and action, then returns new state.

const LOGIN = 'LOGIN';

const LOGOUT = 'LOGOUT';

const defaultState = {
  authenticated: false
};

const authReducer = (state = defaultState, action) => {

  switch (action.type) {

    case LOGIN:
      return {
        authenticated: true
      }

    case LOGOUT:
      return {
        authenticated: false
      }

    default:
      return state;

  }

};

const store = Redux.createStore(authReducer);

const loginUser = () => {
  return {
    type: LOGIN
  }
};

const logoutUser = () => {
  return {
    type: LOGOUT
  }
};
```

3. 监听器

```javascript
const ADD = 'ADD';

const reducer = (state = 0, action) => {
  switch(action.type) {
    case ADD:
      return state + 1;
    default:
      return state;
  }
};

const store = Redux.createStore(reducer);

// global count variable:
let count = 0;

// change code below this line
store.subscribe(() => {
  count ++;
})
// change code above this line

store.dispatch({type: ADD});
console.log(count);
store.dispatch({type: ADD});
console.log(count);
store.dispatch({type: ADD});
console.log(count);

```

4. 合并Reducers

```javascript

// Combine Multiple Reducers
const INCREMENT = 'INCREMENT';
const DECREMENT = 'DECREMENT';

const counterReducer = (state = 0, action) => {
  switch(action.type) {
    case INCREMENT:
      return state + 1;
    case DECREMENT:
      return state - 1;
    default:
      return state;
  }
};

const LOGIN = 'LOGIN';
const LOGOUT = 'LOGOUT';

const authReducer = (state = {authenticated: false}, action) => {
  switch(action.type) {
    case LOGIN:
      return {
        authenticated: true
      }
    case LOGOUT:
      return {
        authenticated: false
      }
    default:
      return state;
  }
};

const rootReducer = Redux.combineReducers({
  count: counterReducer,
  auth: authReducer
});

const store = Redux.createStore(rootReducer);

```

5. 传入带数据的动作

```javascript
//  You can also send specific data along with your actions
const ADD_NOTE = 'ADD_NOTE';

const notesReducer = (state = 'Initial State', action) => {
  switch(action.type) {
    // change code below this line
    case ADD_NOTE:
      return action.text;
    // change code above this line
    default:
      return state;
  }
};

const addNoteText = (note) => {
  // change code below this line
  return {
    type: ADD_NOTE,
    text: note
  }
  // change code above this line
};

const store = Redux.createStore(notesReducer);

console.log(store.getState());
store.dispatch(addNoteText('Hello!'));
console.log(store.getState());
```

6. 中间件处理异步动作

```javascript
const REQUESTING_DATA = 'REQUESTING_DATA'
const RECEIVED_DATA = 'RECEIVED_DATA'

const requestingData = () => { return {type: REQUESTING_DATA} }
const receivedData = (data) => { return {type: RECEIVED_DATA, users: data.users} }

const handleAsync = () => {
  return function(dispatch) {
    // dispatch request action here
    store.dispatch(requestingData());
    setTimeout(function() {
      let data = {
        users: ['Jeff', 'William', 'Alice']
      }
      // dispatch received data action here
      store.dispatch(receivedData(data));
    }, 2500);
  }
};

const defaultState = {
  fetching: false,
  users: []
};

const asyncDataReducer = (state = defaultState, action) => {
  switch(action.type) {
    case REQUESTING_DATA:
      return {
        fetching: true,
        users: []
      }
    case RECEIVED_DATA:
      return {
        fetching: false,
        users: action.users
      }
    default:
      return state;
  }
};

const store = Redux.createStore(
  asyncDataReducer,
  Redux.applyMiddleware(ReduxThunk.default)
);
```

7. State是不可更改的

```javascript
const ADD_TO_DO = 'ADD_TO_DO';

// A list of strings representing tasks to do:
const todos = [
  'Go to the store',
  'Clean the house',
  'Cook dinner',
  'Learn to code',
];

const immutableReducer = (state = todos, action) => {
  switch(action.type) {
    case ADD_TO_DO:
      // don't mutate state here or the tests will fail
      /* let arr = state.map(x => x);
      arr.push(action.todo);
      return arr; */
      return state.concat(action.todo);

      /* return ([...state, action.todo]) */
    default:
      return state;
  }
};

// an example todo argument would be 'Learn React',
const addToDo = (todo) => {
  return {
    type: ADD_TO_DO,
    todo: todo
  }
}

const store = Redux.createStore(immutableReducer);


// Remove an Item from an Array

const immutableReducer = (state = [0,1,2,3,4,5], action) => {
  switch(action.type) {
    case 'REMOVE_ITEM':
      // don't mutate state here or the tests will fail
      let arr = state.map(x => x);
      arr.splice(action.index, 1);
      return arr; 

      /*let arr = [...state];
      arr.splice(action.index, 1);
      return arr; */
    default:
      return state;
  }
};

const removeItem = (index) => {
  return {
    type: 'REMOVE_ITEM',
    index
  }
}

const store = Redux.createStore(immutableReducer);

// Copy an Object with Object.assign
// const newObject = Object.assign({}, obj1, obj2);

const defaultState = {
  user: 'CamperBot',
  status: 'offline',
  friends: '732,982',
  community: 'freeCodeCamp'
};

const immutableReducer = (state = defaultState, action) => {
  switch(action.type) {
    case 'ONLINE':
      // don't mutate state here or the tests will fail
      return Object.assign({}, defaultState, {status: 'online'});
    default:
      return state;
  }
};

const wakeUp = () => {
  return {
    type: 'ONLINE'
  }
};

const store = Redux.createStore(immutableReducer);
```

## Introduction to the React and Redux Challenges

* Getting Started with React Redux
* Manage State Locally First
* Extract State Logic to Redux
* Use Provider to Connect Redux to React
* Map State to Props
* Map Dispatch to Props
* Connect Redux to React
* Connect Redux to the Messages App
* Extract Local State into Redux
* Moving Forward From Here

## Vue

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