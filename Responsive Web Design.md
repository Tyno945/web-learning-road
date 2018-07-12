# Responsive Web Design

## Introduction to Basic HTML & HTML5

HTML, or HyperText Markup Language, is a markup language used to describe the structure of a web page. It uses a special syntax or notation to organize and give information about the page to the browser. Elements usually have opening and closing tags that surround and give meaning to content. For example, there are different tag options to place around text to show whether it is a heading, a paragraph, or a list.

```html
<!DOCTYPE html>
<html>
    <head>
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
* PassedAdjust the Width of an Element Using the width Property
* PassedAdjust the Height of an Element Using the height Property
* PassedUse the strong Tag to Make Text Bold
* PassedUse the u Tag to Underline Text
* PassedUse the em Tag to Italicize Text
* PassedUse the del Tag to Strikethrough Text
* PassedCreate a Horizontal Line Using the hr Element
* PassedAdjust the background-color Property of Text
* PassedAdjust the Size of a Header Versus a Paragraph Tag
* PassedAdd a box-shadow to a Card-like Element
* PassedDecrease the Opacity of an Element
* PassedUse the text-transform Property to Make Text Uppercase
* PassedSet the font-size for Multiple Heading Elements
* PassedSet the font-weight for Multiple Heading Elements
* PassedSet the font-size of Paragraph Text
* PassedSet the line-height of Paragraphs
* PassedAdjust the Hover State of an Anchor Tag
* PassedChange an Element's Relative Position
* PassedMove a Relatively Positioned Element with CSS Offsets
* PassedLock an Element to its Parent with Absolute Positioning
* PassedLock an Element to the Browser Window with Fixed Positioning
* PassedPush Elements Left or Right with the float Property
* PassedChange the Position of Overlapping Elements with the z-index * Property
* PassedCenter an Element Horizontally Using the margin Property
* PassedLearn about Complementary Colors
* PassedLearn about Tertiary Colors
* PassedAdjust the Color of Various Elements to Complementary Colors
* PassedAdjust the Hue of a Color
* PassedAdjust the Tone of a Color
* PassedCreate a Gradual CSS Linear Gradient
* PassedUse a CSS Linear Gradient to Create a Striped Element
* PassedCreate Texture by Adding a Subtle Pattern as a Background * Image
* PassedUse the CSS Transform scale Property to Change the Size of * an Element
* PassedUse the CSS Transform scale Property to Scale an Element on * Hover
* PassedUse the CSS Transform Property skewX to Skew an Element * Along the X-Axis
* PassedUse the CSS Transform Property skewY to Skew an Element * Along the Y-Axis
* PassedCreate a Graphic Using CSS
* PassedCreate a More Complex Shape Using CSS and HTML
* PassedLearn How the CSS @keyframes and animation Properties Work
* PassedUse CSS Animation to Change the Hover State of a Button
* PassedModify Fill Mode of an Animation
* PassedCreate Movement Using CSS Animation
* PassedCreate Visual Direction by Fading an Element from Left to * Right
* PassedAnimate Elements Continually Using an Infinite Animation * Count
* PassedMake a CSS Heartbeat using an Infinite Animation Count
* PassedAnimate Elements at Variable Rates
* PassedAnimate Multiple Elements at Variable Rates
* PassedChange Animation Timing with Keywords
* PassedLearn How Bezier Curves Work
* PassedUse a Bezier Curve to Move a Graphic
* PassedMake Motion More Natural Using a Bezier Curve

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
* PassedKnow When Alt Text Should be Left Blank
* PassedUse Headings to Show Hierarchical Relationships of Content
* PassedJump Straight to the Content Using the main Element
* PassedWrap Content in the article Element
* PassedMake Screen Reader Navigation Easier with the header Landmark
* PassedMake Screen Reader Navigation Easier with the nav Landmark
* PassedMake Screen Reader Navigation Easier with the footer Landmark
* PassedImprove Accessibility of Audio Content with the audio Element
* PassedImprove Chart Accessibility with the figure Element
* PassedImprove Form Field Accessibility with the label Element
* PassedWrap Radio Buttons in a fieldset Element for Better Accessibility
* PassedAdd an Accessible Date Picker
* PassedStandardize Times with the HTML5 datetime Attribute
* PassedMake Elements Only Visible to a Screen Reader by Using Custom CSS
* PassedImprove Readability with High Contrast Text
* PassedAvoid Colorblindness Issues by Using Sufficient Contrast
* PassedAvoid Colorblindness Issues by Carefully Choosing Colors that Convey Information
* PassedGive Links Meaning by Using Descriptive Link Text
* PassedMake Links Navigatable with HTML Access Keys
* PassedUse tabindex to Add Keyboard Focus to an Element
* PassedUse tabindex to Specify the Order of Keyboard Focus for Several Elements

## Introduction to the Responsive Web Design Challenges