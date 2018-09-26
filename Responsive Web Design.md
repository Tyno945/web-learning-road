# Responsive Web Design

## Introduction to Basic HTML & HTML5

HTML, or HyperText Markup Language, is a markup language used to describe the structure of a web page. It uses a special syntax or notation to organize and give information about the page to the browser. Elements usually have opening and closing tags that surround and give meaning to content. For example, there are different tag options to place around text to show whether it is a heading, a paragraph, or a list.

* Say Hello to HTML Elements
* Headline with the h2 Element
* Inform with the Paragraph Element
* Fill in the Blank with Placeholder Text
* Uncomment HTML
* Comment out HTML
* Delete HTML Elements
* Introduction to HTML5 Elements
* Add Images to Your Website
* Link to External Pages with Anchor Elements
* Link to Internal Sections of a Page with Anchor Elements
* Nest an Anchor Element within a Paragraph
* Make Dead Links Using the Hash Symbol
* Turn an Image into a Link
* Create a Bulleted Unordered List
* Create an Ordered List
* Create a Text Field
* Add Placeholder Text to a Text Field
* Create a Form Element
* Add a Submit Button to a Form
* Use HTML5 to Require a Field
* Create a Set of Radio Buttons
* Create a Set of Checkboxes
* Check Radio Buttons and Checkboxes by Default
* Nest Many Elements within a Single div Element
* Declare the Doctype of an HTML Document
* Define the Head and Body of an HTML Document

### 重点学习

1. [HTML5新元素](http://www.runoob.com/html/html5-new-element.html)
2. 记忆各类元素及其常见属性。[速查手册](http://www.runoob.com/html/html-quicklist.html)



```html
<!DOCTYPE html>
<html>
    <head>
        <meta charset="utf-8">
        <title>CatPhoto</title>
    </head>
    <body>
        <h2>CatPhotoApp</h2>
        <main>
        <p>Click here to view more <a href="#">cat photos</a>.</p>
        
        <a href="#"><img src="https://bit.ly/fcc-relaxing-cat" alt="A cute orange cat lying on its back."></a>
        
        <p>Things cats love:</p>
        <ul>
            <li>cat nip</li>
            <li>laser pointers</li>
            <li>lasagna</li>
        </ul>
        <p>Top 3 things cats hate:</p>
        <ol>
            <li>flea treatment</li>
            <li>thunder</li>
            <li>other cats</li>
        </ol>
        
        <form action="/submit-cat-photo">
            <label><input type="radio" name="indoor-outdoor" checked> Indoor</label>
            <label><input type="radio" name="indoor-outdoor"> Outdoor</label><br>
            <label><input type="checkbox" name="personality" checked> Loving</label>
            <label><input type="checkbox" name="personality"> Lazy</label>
            <label><input type="checkbox" name="personality"> Energetic</label><br>
            <input type="text" placeholder="cat photo URL" required>
            <button type="submit">Submit</button>
        </form>
        </main>
    </body>
</html>
```

## Introduction to Basic CSS

Cascading Style Sheets (CSS) tell the browser how to display the text and other content that you write in HTML.

There are three main ways to apply CSS styling. You can apply inline styles directly to HTML elements with the style attribute. Alternatively, you can place CSS rules within style tags in an HTML document. Finally, you can write CSS rules in an external style sheet, then reference that file in the HTML document.

* Change the Color of Text
* Use CSS Selectors to Style Elements
* Use a CSS Class to Style an Element
* Style Multiple Elements with a CSS Class
* Change the Font Size of an Element
* Set the Font Family of an Element
* Import a Google Font
* Specify How Fonts Should Degrade
* Size Your Images
* Add Borders Around Your Elements
* Add Rounded Corners with border-radius
* Make Circular Images with a border-radius
* Give a Background Color to a div Element
* Set the id of an Element
* Use an id Attribute to Style an Element
* Adjust the Padding of an Element
* Adjust the Margin of an Element
* Add a Negative Margin to an Element
* Add Different Padding to Each Side of an Element
* Add Different Margins to Each Side of an Element
* Use Clockwise Notation to Specify the Padding of an Element
* Use Clockwise Notation to Specify the Margin of an Element
* Use Attribute Selectors to Style Elements
* Understand Absolute versus Relative Units
* Style the HTML Body Element
* Inherit Styles from the Body Element
* Prioritize One Style Over Another
* Override Styles in Subsequent CSS
* Override Class Declarations by Styling ID Attributes
* Override Class Declarations with Inline Styles
* Override All Other Styles by using Important
* Use Hex Code for Specific Colors
* Use Hex Code to Mix Colors
* Use Abbreviated Hex Code
* Use RGB values to Color Elements
* Use RGB to Mix Colors
* Use CSS Variables to change several elements at once
* Create a custom CSS Variable
* Use a custom CSS Variable
* Attach a Fallback value to a CSS Variable
* Cascading CSS variables
* Change a variable for a specific area
* Use a media query to change a variable


### 重点学习
1. [CSS选择器](http://www.runoob.com/cssref/css-selectors.html)
2. 记忆常用[CSS属性](http://www.runoob.com/cssref/css-reference.html)
3. 导入字体
4. 绝对单位和相对单位
5. 理解样式层叠
6. 掌握CSS颜色表示
7. 重点理解CSS变量
8. 掌握[媒体查询](http://www.runoob.com/css3/css3-mediaqueries.html)



```html

<!-- Use CSS Variables to change several elements at once -->
<style>
  :root {
    --penguin-size: 300px;
    --penguin-skin: gray;
    --penguin-belly: white;
    --penguin-beak: orange;
  }
  
  @media (max-width: 350px) {
    :root {
      
      /* add code below */
      --penguin-size: 200px;
      --penguin-skin: black;
      /* add code above */
      
    }
  }
  
  .penguin {
    position: relative;
    margin: auto;
    display: block;
    margin-top: 5%;
    width: var(--penguin-size, 300px);
    height: var(--penguin-size, 300px);
  }
  
  .right-cheek {
    top: 15%;
    left: 35%;
    background: var(--penguin-belly, white);
    width: 60%;
    height: 70%;
    border-radius: 70% 70% 60% 60%;
  }
  
  .left-cheek {
    top: 15%;
    left: 5%;
    background: var(--penguin-belly, white);
    width: 60%;
    height: 70%;
    border-radius: 70% 70% 60% 60%;
  }
  
  .belly {
    top: 60%;
    left: 2.5%;
    background: var(--penguin-belly, white);
    width: 95%;
    height: 100%;
    border-radius: 120% 120% 100% 100%;
  }
  
  .penguin-top {
    top: 10%;
    left: 25%;
    background: var(--penguin-skin, gray);
    width: 50%;
    height: 45%;
    border-radius: 70% 70% 60% 60%;
  }
  
  .penguin-bottom {
    top: 40%;
    left: 23.5%;
    background: var(--penguin-skin, gray);
    width: 53%;
    height: 45%;
    border-radius: 70% 70% 100% 100%;
  }
  
  .right-hand {
    top: 5%;
    left: 25%;
    background: var(--penguin-skin, black);
    width: 30%;
    height: 60%;
    border-radius: 30% 30% 120% 30%;
    transform: rotate(130deg);
    z-index: -1;
    animation-duration: 3s;
    animation-name: wave;
    animation-iteration-count: infinite;
    transform-origin:0% 0%;
    animation-timing-function: linear;
  }
  
  @keyframes wave {
      10% {
        transform: rotate(110deg);
      }
      20% {
        transform: rotate(130deg);
      }
      30% {
        transform: rotate(110deg);
      } 
      40% {
        transform: rotate(130deg);
      }  
    }
  
  .left-hand {
    top: 0%;
    left: 75%;
    background: var(--penguin-skin, gray);
    width: 30%;
    height: 60%;
    border-radius: 30% 30% 30% 120%;
    transform: rotate(-45deg);
    z-index: -1;
  }
  
  .right-feet {
    top: 85%;
    left: 60%;
    background: var(--penguin-beak, orange);
    width: 15%;
    height: 30%;
    border-radius: 50% 50% 50% 50%;
    transform: rotate(-80deg);
    z-index: -2222;
  }
  
  .left-feet {
    top: 85%;
    left: 25%;
    background: var(--penguin-beak, orange);
    width: 15%;
    height: 30%;
    border-radius: 50% 50% 50% 50%;
    transform: rotate(80deg);
    z-index: -2222;
  }
  
  .right-eye {
    top: 45%;
    left: 60%;
    background: black;
    width: 15%;
    height: 17%;
    border-radius: 50%;
  }
  
  .left-eye {
    top: 45%;
    left: 25%;
    background: black;
    width: 15%;
    height: 17%;
    border-radius: 50%;
  }
  
  .sparkle {
    top: 25%;
    left:-23%;
    background: white;
    width: 150%;
    height: 100%;
    border-radius: 50%;
  }
  
  .blush-right {
    top: 65%;
    left: 15%;
    background: pink;
    width: 15%;
    height: 10%;
    border-radius: 50%;
  }
  
  .blush-left {
    top: 65%;
    left: 70%;
    background: pink;
    width: 15%;
    height: 10%;
    border-radius: 50%;
  }
  
  .beak-top {
    top: 60%;
    left: 40%;
    background: var(--penguin-beak, orange);
    width: 20%;
    height: 10%;
    border-radius: 50%;
  }
  
  .beak-bottom {
    top: 65%;
    left: 42%;
    background: var(--penguin-beak, orange);
    width: 16%;
    height: 10%;
    border-radius: 50%;
  }
  
  body {
    background:#c6faf1;
  }
  
  .penguin * {
    position: absolute;
  }
</style>
<div class="penguin">
  <div class="penguin-bottom">
    <div class="right-hand"></div>
    <div class="left-hand"></div>
    <div class="right-feet"></div>
    <div class="left-feet"></div>
  </div>
  <div class="penguin-top">
    <div class="right-cheek"></div>
    <div class="left-cheek"></div>
    <div class="belly"></div>
    <div class="right-eye">
      <div class="sparkle"></div>
    </div>
    <div class="left-eye">
      <div class="sparkle"></div>
    </div>
    <div class="blush-right"></div>
    <div class="blush-left"></div>
    <div class="beak-top"></div>
    <div class="beak-bottom"></div>
  </div>
</div>
```

## Introduction to the Applied Visual Design Challenges

Visual Design in web development is a broad topic. It combines typography, color theory, graphics, animation, and page layout to help deliver a site's message. 

* Create Visual Balance Using the text-align Property
* Adjust the Width of an Element Using the width Property
* Adjust the Height of an Element Using the height Property
* Use the strong Tag to Make Text Bold
* Use the u Tag to Underline Text
* Use the em Tag to Italicize Text
* Use the del Tag to Strikethrough Text
* Create a Horizontal Line Using the hr Element
* Adjust the background-color Property of Text
* Adjust the Size of a Header Versus a Paragraph Tag
* Add a box-shadow to a Card-like Element
* Decrease the Opacity of an Element
* Use the text-transform Property to Make Text Uppercase
* Set the font-size for Multiple Heading Elements
* Set the font-weight for Multiple Heading Elements
* Set the font-size of Paragraph Text
* Set the line-height of Paragraphs
* Adjust the Hover State of an Anchor Tag
* Change an Element's Relative Position
* Move a Relatively Positioned Element with CSS Offsets
* Lock an Element to its Parent with Absolute Positioning
* Lock an Element to the Browser Window with Fixed Positioning
* Push Elements Left or Right with the float Property
* Change the Position of Overlapping Elements with the z-index  Property
* Center an Element Horizontally Using the margin Property
* Learn about Complementary Colors
* Learn about Tertiary Colors
* Adjust the Color of Various Elements to Complementary Colors
* Adjust the Hue of a Color
* Adjust the Tone of a Color
* Create a Gradual CSS Linear Gradient
* Use a CSS Linear Gradient to Create a Striped Element
* Create Texture by Adding a Subtle Pattern as a Background Image
* Use the CSS Transform scale Property to Change the Size of an Element
* Use the CSS Transform scale Property to Scale an Element on Hover
* Use the CSS Transform Property skewX to Skew an Element Along the X-Axis
* Use the CSS Transform Property skewY to Skew an Element Along the Y-Axis
* Create a Graphic Using CSS
* Create a More Complex Shape Using CSS and HTML
* Learn How the CSS @keyframes and animation Properties Work
* Use CSS Animation to Change the Hover State of a Button
* Modify Fill Mode of an Animation
* Create Movement Using CSS Animation
* Create Visual Direction by Fading an Element from Left to Right
* Animate Elements Continually Using an Infinite Animation Count
* Make a CSS Heartbeat using an Infinite Animation Count
* Animate Elements at Variable Rates
* Animate Multiple Elements at Variable Rates
* Change Animation Timing with Keywords
* Learn How Bezier Curves Work
* Use a Bezier Curve to Move a Graphic
* Make Motion More Natural Using a Bezier Curve

### 重点学习
1. 了解视觉设计相关知识，如原型，字体，排版布局，色彩，动画等
2. 掌握`text-align`，`background`，`box-shadow`
3. 掌握`position`，`float`
4. 掌握色轮,HSL
5. 掌握渐变`linear-gradient()`，`transform`
6. 理解CSS图画
7. 掌握CSS动画,理解Bezier Curves

```html
<!-- Make a CSS Heartbeat using an Infinite Animation Count -->

<style>
  .back {
    position: fixed;
    padding: 0;
    margin: 0;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    background: white;
    animation-name: backdiv;
    animation-duration: 1s; 
    animation-iteration-count: infinite;
  }

  .heart {
    position: absolute;
    margin: auto;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    background-color: pink;
    height: 50px;
    width: 50px;
    transform: rotate(-45deg);
    animation-name: beat;
    animation-duration: 1s;
    animation-iteration-count: infinite;
  }
  .heart:after {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: 0px;
    left: 25px;
  }
  .heart:before {
    background-color: pink;
    content: "";
    border-radius: 50%;
    position: absolute;
    width: 50px;
    height: 50px;
    top: -25px;
    left: 0px;
  }

  @keyframes backdiv {
    50% {
      background: #ffe6f2;
    }
  }

  @keyframes beat {
    0% {
      transform: scale(1) rotate(-45deg);
    }
    50% {
      transform: scale(0.6) rotate(-45deg);
    }
  }

</style>
<div class="back"></div>
<div class="heart"></div>
```

## Introduction to the Applied Accessibility Challenges

"Accessibility" generally means having web content and a user interface that can be understood, navigated, and interacted with by a broad audience. This includes people with visual, auditory, mobility, or cognitive disabilities.

1. have well-organized code that uses appropriate markup

2. ensure text alternatives exist for non-text and visual content

3. create an easily-navigated page that's keyboard-friendly

* Add a Text Alternative to Images for Visually Impaired Accessibility
* Know When Alt Text Should be Left Blank
* Use Headings to Show Hierarchical Relationships of Content
* Jump Straight to the Content Using the main Element
* Wrap Content in the article Element
* Make Screen Reader Navigation Easier with the header Landmark
* Make Screen Reader Navigation Easier with the nav Landmark
* Make Screen Reader Navigation Easier with the footer Landmark
* Improve Accessibility of Audio Content with the audio Element
* Improve Chart Accessibility with the figure Element
* Improve Form Field Accessibility with the label Element
* Wrap Radio Buttons in a fieldset Element for Better Accessibility
* Add an Accessible Date Picker
* Standardize Times with the HTML5 datetime Attribute
* Make Elements Only Visible to a Screen Reader by Using Custom CSS
* Improve Readability with High Contrast Text
* Avoid Colorblindness Issues by Using Sufficient Contrast
* Avoid Colorblindness Issues by Carefully Choosing Colors that Convey Information
* Give Links Meaning by Using Descriptive Link Text
* Make Links Navigatable with HTML Access Keys
* Use tabindex to Add Keyboard Focus to an Element
* Use tabindex to Specify the Order of Keyboard Focus for Several Elements

## Introduction to the Responsive Web Design Challenges

Responsive Web Design is an approach to designing web content that responds to the constraints of different devices. The page structure and CSS rules should be flexible to accommodate these differences. In general, design the page's CSS to your target audience. 

* Create a Media Query
* Make an Image Responsive
* Use a Retina Image for Higher Resolution Displays
* Make Typography Responsive

```css
// Make an Image Responsive
img {
  max-width: 100%;
  display: block;
  height: auto;
}
```

## Introduction to the CSS Flexbox Challenges

CSS3 introduced Flexible Boxes, or flexbox, to create page layouts for a dynamic UI. It is a layout mode that arranges elements in a predictable way for different screen sizes and browsers. 

* Use display: flex to Position Two Boxes
* Add Flex Superpowers to the Tweet Embed
* Use the flex-direction Property to Make a Row
* Apply the flex-direction Property to Create Rows in the Tweet Embed
* Use the flex-direction Property to Make a Column
* Apply the flex-direction Property to Create a Column in the Tweet Embed
* Align Elements Using the justify-content Property
* Use the justify-content Property in the Tweet Embed
* Align Elements Using the align-items Property
* Use the align-items Property in the Tweet Embed
* Use the flex-wrap Property to Wrap a Row or Column
* Use the flex-shrink Property to Shrink Items
* Use the flex-grow Property to Expand Items
* Use the flex-basis Property to Set the Initial Size of an Item
* Use the flex Shorthand Property
* Use the order Property to Rearrange Items
* Use the align-self Property

### 重点学习

1. 掌握`display: flex`，默认`flex-direction: row`，`flex-direction: column`
2. 掌握`justify-content`属性，值有`center,flex-start,flex-end,space-between,space-around`
3. 掌握`align-items`属性，值有`center,flex-start,flex-end,stretch,baseline`
4. 掌握`flex-wrap`属性，值有`nowrap,wrap,wrap-reverse`
5. 掌握`flex-shrink`和`flex-grow`属性，值是数字。掌握`flex-basis`属性，值是大小（px, em, %）。

```html
<style>
  #box-container {
    display: flex;
    height: 500px;
  }
  #box-1 {
    background-color: dodgerblue;
    width: 100%;
    height: 200px;
    flex-shrink: 1;
  }

  #box-2 {
    background-color: orangered;
    width: 100%;
    height: 200px;
    flex-shrink: 2;
  }
</style>

<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```

6. 掌握`flex`属性，默认是`flex: 0 1 auto;`,代表`flex-grow: 0;, flex-shrink: 1;,flex-basis: auto;`

```html
<style>
  #box-container {
    display: flex;
    height: 500px;
  }
  #box-1 {
    background-color: dodgerblue;
    flex: 2 2 150px;
    height: 200px;
  }

  #box-2 {
    background-color: orangered;
    flex: 1 1 150px;
    height: 200px;
  }
</style>

<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```

7. 掌握`order`排序属性，值是数字。

8. 掌握`align-self`对齐属性，值同`align-items`属性。

```html
<style>
  #box-container {
    display: flex;
    height: 500px;
  }
  #box-1 {
    background-color: dodgerblue;
    align-self: center;
    height: 200px;
    width: 200px;
  }

  #box-2 {
    background-color: orangered;
    align-self: flex-end;
    height: 200px;
    width: 200px;
  }
</style>

<div id="box-container">
  <div id="box-1"></div>
  <div id="box-2"></div>
</div>
```

## Introduction to the CSS Grid Challenges

CSS Grid helps you easily build complex web designs. It works by turning an HTML element into a grid container with rows and columns for you to place children elements where you want within the grid.

* Create Your First CSS Grid
* Add Columns with grid-template-columns
* Add Rows with grid-template-rows
* Use CSS Grid units to Change the Size of Columns and Rows
* Create a Column Gap Using grid-column-gap
* Create a Row Gap using grid-row-gap
* Add Gaps Faster with grid-gap
* Use grid-column to Control Spacing
* Use grid-row to Control Spacing
* Align an Item Horizontally using justify-self
* Align an Item Vertically using align-self
* Align All Items Horizontally using justify-items
* Align All Items Vertically using align-items
* Divide the Grid Into an Area Template
* Place Items in Grid Areas Using the grid-area Property
* Use grid-area Without Creating an Areas Template
* Reduce Repetition Using the repeat Function
* Limit Item Size Using the minmax Function
* Create Flexible Layouts Using auto-fill
* Create Flexible Layouts Using auto-fit
* Use Media Queries to Create Responsive Layouts
* Create Grids within Grids

```html
<!-- CSS Grid: Use Media Queries to Create Responsive Layouts -->

<style>
  .item1 {
    background: LightSkyBlue;
    grid-area: header;
  }
  
  .item2 {
    background: LightSalmon;
    grid-area: advert;
  }
  
  .item3 {
    background: PaleTurquoise;
    grid-area: content;
  }
  
  .item4 {
    background: lightpink;
    grid-area: footer;
  }
  
  .container {
    font-size: 1.5em;
    min-height: 300px;
    width: 100%;
    background: LightGray;
    display: grid;
    grid-template-columns: 1fr;
    grid-template-rows: 50px auto 1fr auto;
    grid-gap: 10px;
    grid-template-areas:
      "header"
      "advert"
      "content"
      "footer";
  }
  
  @media (min-width: 300px){
    .container{
      grid-template-columns: auto 1fr;
      grid-template-rows: auto 1fr auto;
      grid-template-areas:
        "advert header"
        "advert content"
        "advert footer";
    }
  }
  
  @media (min-width: 400px){
    .container{
      /* change the code below this line */
    
      grid-template-areas:
        "advert header"
        "advert content"
        "advert footer";
    
    /* change the code above this line */
    }
  }
</style>
  
<div class="container">
  <div class="item1">header</div>
  <div class="item2">advert</div>
  <div class="item3">content</div>
  <div class="item4">footer</div>
</div>
```

## Introduction to the Responsive Web Design Projects

 By working on projects you would have the opportunity of applying all the skills, principles and concepts you have learnt so far HTML, CSS, Visual Design, Accessibility, etc.

In this section you get the chance to:

* Build a Tribute Page
* Build a Survey Form
* Build a Product Landing Page
* Build a Technical Documentation Page
* Build a Personal Portfolio Webpage