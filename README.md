# What is CSS ?<br>

CSS allows you to define styles for web pages.It can be used to style text, change colors, font size, etc., as well as create layout - for example, create columns, sidebars, navigation menus, etc.<br>


CSS stands for Cascading Style Sheets.<br>

CSS uses rules to style elements.

A rule is a group of style declarations.

An example rule could define all paragraphs to be red and large.<br>

There are a number of ways we can apply CSS rules to our elements.

#### Inline:<br>

The first way is to define the style declarations right on the element we target, using the style attribute.We can have multiple declarations in the style rule.The declarations are separated using a semicolon.<br>

#### Outline:<br>

It is common practice to define the CSS rules in a separate document and link it with the HTML.

CSS allows you to target elements using selectors, which allows you to target specific elements and apply the same style to them.
The style rules are defined in a CSS file using selectors.<br>

### Selectors<br>

u can use the target element with {} in css file.Each style declaration in a rule ends with a semicolon.  We can target multiple selectors at once, by separating the selectors with a comma.<br>

#### Class Selectors:<br>
Often we need to target only a subset of elements, without changing the others. This can be done using a class selector.We first need to add a class attribute to the elements we want to target. 
the class selector needs to start with a dot, followed by the class name that we gave to our element.<br>

#### Id:<br>
We can also create selectors based on the id attribute of elements.This is done by using the hash (#) symbol before the id value.You can have only one element with the same id on the page, while the class value can be used multiple times.<br>

#### Besed on location:<br>
We can also target elements based on their location.For example, there are two strong elements, one inside a paragraph and the other inside a list item.We can target only the one inside the list item by using the following rule:
in css file: li strong{..}<br>

### Styling Texts <br>

#### color :<br>
change color of the text. Besides color names, a color value can also be set using hex and rgb values.Colors are displayed in combinations of red, green, and blue light (RGB).Hex values are written using the hashtag symbol (#), followed by six hex characters, which define the components.<br>

#### font-size :<br>
The font-size property is used to set the size of the text.It can take values using pixels (px). The em size unit is another way to set the size of the text.By default, 1em = 16px. <br>

#### Font-family :<br>
You can change the font of the text using the font-family property.There are only a certain number of fonts that are generally available across all systems. These are called web safe fonts and include: Arial, Courier New, Georgia, Times New Roman, Trebuchet MS, Verdana.It's a common practice to define multiple fonts in the font-family property, so that if the first one is not available on for the user, the browser will try the next one like :<br>
.intro {
  font-family: Arial, "Helvetica Neue", Helvetica, sans-serif;
}<br>

If the browser does not support the font Arial, it tries the next font (Helvetica Neue, then Helvetica). If the browser doesn't have any of them, it will try the generic sans-serif.
If the font name consists of multiple words, it has to be in quotes.<br>

#### Font-style :<br>
The font-style property is used to make text italic:<br>
.intro {
  font-style: italic;
}<br>

#### font-weight :<br>
The font-weight property is used to make the text bold.You can also define the font weight with a number from 100 (thin) to 900 (thick). 400 is the same as normal, and 700 is the same as bold.<br>

#### text-transform :<br>
allows you to transform text with the following values:<br>

uppercase: Transforms the text to capitals.<br>

lowercase: Transforms the text to lower case.<br>

capitalize: Transforms all words to have the first letter capitalized.<br>

.intro {<br>
  text-transform: uppercase;
}<br>

#### text-decoration :<br>
supports the following values: <br>

none: removes any decoration.<br>

underline: underlines the text.<br>

overline: gives the text an overline.<br>

line-through: puts a strikethrough over the text.<br>

.intro {<br>
  text-decoration: underline;
}<br>
.outro {<br>
  text-decoration: line-through;
}<br>

#### text-shadow :<br>
allows you to set a shadow for the text.<br>
h1 {<br>

  text-shadow: 3px 2px 3px red;
} <br>
The first value is the horizontal offset of the shadow.<br>

The second value - the vertical offset.<br>

The third value is the blur radius: a higher value means the shadow is dispersed more widely.<br>

The last one is the color of the shadow.<br>

You can add multiple shadows, by separating them with a comma.<br>

#### Text Alignment :<br>

The text-align property is used to control how text is aligned within its container. The supported values are: left, right, center, justify.

#### Line Height : <br>
sets the height of each line of text.The recommended line height is 1.5 - 2 (double spaced.).__>> The line-height value 2 indicates that its double the height of the font .  <br>

#### Letter & Word Spacing : <br>

The letter-spacing and word-spacing properties allow you to set the spacing between letters and words in your text. <br>


## Box_Model <br>

HTML elements appear as boxes. The box model defines how the different parts of the box -  margin, border, padding, and content, work together to create the box.The content box is the area where the content is displayed.<br>

The padding box is the white space around the content.<br>

The border box comes after the padding.<br>

The margin box is the last one and defines the space between this box and other elements.<br>

The Standard Box Model : In the standard box model, the height and width attributes define the size of the content box.

Any padding and border is then added to that width and height to get the total size of the box.

For example, the total width of the box with paddings will be the sum of width plus padding left and padding right.The margin is not counted towards the actual size of the box, it is the space outside the box.

### Margin :<br>
The margin is the space around your box.

We can control all margins of an element at once using the margin property, in the following order: top, right, bottom, and left.<br>


The margins can be provided using separate properties.__>> margin_top,margin_right,margin_bottom,margin_left

### Padding :<br>
The padding is the area between the border and the content. It is defined similar to the margin.


### BOX_SIZE <br>

Similar to using HTML attributes, the width and height can be given using CSS, with the width and height properties.They can take both pixel and percentage values. <br>

Similar to the width, we can also define the height of the elements.<br>

Alternative Box Model :<br>
It can be inconvenient to calculate the actual size of the box, because of the padding and border widths being added to it.

For this reason, CSS provides an alternative box model where the given width is taken by the box and includes the padding and border.

The model is turned on using box-sizing: border-box:<br>
p {<br>
  margin: 5px 10px 5px 10px;<br>
  padding: 4px 7px 4px 7px;<br>
  width: 200px;<br>
  box-sizing: border-box;<br>
  border: 3px solid black;<br>
}<br>
Now, the paragraph box has the width 200px, irrespective of the padding and border widths.Without the box-sizing property it would have the width: 200+7+3+7+3 = 220px.<br>

### Border :<br>
The border property allows you to set the border style for the elements.


The property takes 3 values:

- the width in pixels,

- the border style,

- the border color.<br>
If not defined, the border is not visible.<br>

Border Styles :<br>
The border style can take one of the following values:<br>

dotted, dashed, solid, double, groove, ridge, inset, outset.<br>
Similar to paddings and margins, the border supports separate properties to set the border for each side, e.g.: border-top, border-bottom, etc.Each side of the border can have its own style.<br>

#### Border Radius <br>
The border-radius property allows you to round the corners of elements.A single value provided uses that value for all 4 corners. You can also set the border radius for each corner separately, by separating them with spaces.The radius applies to the whole element, even if it has no border set.

### Background <br>
<br>
 Background-color :<br>
 <br>
 This property sets the background color for an element.You can set the color using color names, hex values and rgb.<br>
 <br>

Background Image : <br>
<br>
You can also set an image as the background of an element, using the background-image property.It has the following syntax:<br>
.box {<br>
  background-image: url('sl-logo.png');<br>
  height:150px;<br>
  padding: 10px;<br>
}<br>
The image address has to be put in quotes and enclosed by the url() attribute.A small image is, by default, tiled to fill the box.In case the image is larger than the element, it is not scaled down by default and we will see only the part that fits in the box.<br>

background-repeat : <br>
<br>
This  property can control how the image is tiled (or repeated) in the box.It can take the following values:

no-repeat: does not tile the image.

repeat-x: repeat horizontally.

repeat-y: repeat vertically.

repeat: repeat in both directions (default value).<br>
<br>
background-position: <br>
<br>
This property sets the position in which the background image appears. It uses a coordinate system in which the top-left corner of the box is at position (0,0).As its value, it can take both pixel/percentage units and keywords (top, left, right, bottom, center).The default background-position value is (0,0): the top-left corner.<br>
<br>

background-size : <br>
<br>
The background-size property allows you to define how the image should fit inside the box.It has two possible values:

cover: The image will completely cover the box, while maintaining its aspect ratio. 

contain: The image will fit inside the box completely.

<br>

### Styling Lists 

<br>

By default, unordered list items are marked with round bullets, while ordered lists are numbered.<br>

 list-style-type : <br>
 <br>
 llows you to change the markers to circle, square, decimal, disc, lower-alpha, lower-roman, etc.<br>


 list-style-position : <br>
 <br>
 specifies the position of the bullets: inside or outside.The default value is outside.


list-style-image : <br>
<br>
can be used to specify an image to be used as the list item marker.However, this property does not allow you to control the position and size of the image.If you want to use an image as the marker, it's better to set the list-style-type to none and add a background image to the list items with the marker image, positioning it to the left.<br>

list-style <br>
<br>
The list-style property is a shorthand for setting list-style-type, list-style-image and list-style-position, all in one declaration.<br>
<br>

### Styling Links 
<br>
A link is by default blue in color and underlined. We can style links with CSS properties (e.g., color, font-family, background, etc.). <br>

In addition, links can be styled differently, depending on what state they are in. The following selectors are available:

a:link - defines the style for normal unvisited links.

a:visited - defines the style for visited links.

a:active - a link becomes active once you click on it.

a:hover - a link is hovered when the mouse is over it.

These are called pseudo selectors.

a:hover {


  background-color: yellow;

  
}

 text-decoration :



 By default, all links are underlined.We can remove the underline using the text-decoration property.

                                       
                                       
## Styling Tables <br>

An HTML table doesn't look appealing by default.

border-collapse : <br>

The table cells have spacing between them by default, making double borders appear. The border-collapse property sets the borders to collapse into one, making the table look a lot better.

border-collapse: collapse

We can also provide some padding to the cells, to give the content some space to "breathe"


nth-child() : 

allows you to select specific rows and style them.


```
tr:nth-child(3) {
    background-color: #b0d1e4;
}
```
<br>

The nth-child selector allows you to also define rules for the rows, instead of providing the number.

For example, we can style the odd and even rows separately, giving them different background colors:

```
tr:nth-child(even) {
  background-color: #b0d1e4;
}
tr:nth-child(odd) {
  background-color: #6aabd1;
}
```
<br>

### Styling Forms <br>
<br>
We can add styling to the text fields and labels by selecting them using their name.

We can target the input elements by their type using the following syntax:

```
input[type='text'] {
  border: 1px solid green;
  width: 100%;
  padding: 5px;
}
```
<br>
We can also style the text inside the text fields, just like any other text.Just like link states, we can use the :hover pseudo selector to style the button, when it is hovered:

```
input[type='button']:hover {
  background-color: gray;
}
```
<br>

## Display 
<br>
<br>
block : The block elements span the entire width of their parent and start from a new line. __>> p, article, sec tion <br>

inline : The inline elements are placed inside block elements and act similar to their content, sitting on the same line.  __>> b, a <br>

flex : It is used to arrange elements in rows and columns. It will make the articles inside it act as flex items and arrange in columns. By default, the flex items take equal space.We can control what proportion of space flex items take up compared to the other items using the flex property. <br>


```
.special {
  flex: 2;
} 
```
<br>
make equal columns from the div elements, which are wrapped in a main element. <br>

```
main{
display:flex;
}
div{
flex:1;
}
```
<br>
 to make a real site layout:

 HTML :
 <br>
 ```
<header>My Header</header>
<main>
    <section class="content">Main Section</section>
    <section class="side">Side Section</section>
</main>
<footer>My Footer</footer>
```
<br>
 CSS :

 ```
header {
    background-color: #77adda;
    text-align: center;
    padding: 20px;
}
footer {
    background-color: black;
    color: white;
    text-align: center;
    padding: 10px;
}
.content {
    background-color: #2ca152;
    color: white;
    padding: 20px;
    height: 200px;
    flex: 3;
}
.side {
    background-color: #e6e6a5;
    padding: 20px;
    flex: 1;
}
main {
    display: flex;
}
```
<br>

### Positioning
<br>
<br>

To fine-tune the position of elements on the page, the position property can be used. There are a number of different values the position property supports, changing the way the element is positioned.By default, all elements have the position:static, which is the normal flow.
<br>
<br>
Static :<br>
<br>
By default, all elements have the position:static.
<br>
<br>
Relative :<br>
<br>
the element is positioned relative to its normal position.The properties top, right, bottom, and left can be used to specify how the element will be shifted.The content of relatively positioned elements can be moved and overlap other elements, but the reserved space for the element is still preserved in the normal flow.
<br>
<br>
Absolute : <br>
<br>
An absolutely positioned element is removed from the normal flow of the page. This is useful, for example, to create popup boxes, control menus, panels, etc.
<br>
<br>
Fixed : <br>
<br>
Fixed positioning makes the element stick to a part of the visible area, which means it always stays in the same place even if the page is scrolled.<br>
<br>

  Float :
<br>
<br>
allows you to float an element inside a container. The supported values are left and right. You can float any other element with the same technique.
<br>
<br>
z-index :
<br>
<br>
When elements are positioned outside the normal flow, they can overlap other elements. The z-index property specifies the stack order of an element (which element should be placed in front of, or behind, the others).
<br>
<br>
<br>
<br>
An absolutely positioned element's position is relative to its 🔰first positioned parent element🔰. If the element doesn't have any positioned parent elements, then its position will be relative to the initial containing block, which is usually the viewport or the body element. The position of the first positioned parent element is determined by the closest ancestor element that has a position value of relative, absolute, fixed, or sticky.
<br>
<br>
<br>
### CSS Transforms 
<br>
<br>
CSS transforms allow you to translate, rotate, scale, and skew elements.A transformation is an effect that lets an element change shape, size, and position.
<br>
<br>
Rotate :
<br>
The rotate() method rotates an element clockwise or counter-clockwise, according to a given degree. Negative value will result in a counterclockwise rotation. 
transform: rotate(- 45deg);
<br>
<br>
transform-origin :
<br>
The transform-origin property allows you to change the position of transformed elements. 
<br>
<br>
translate() :
<br>
The translate() method moves an element from its current position (according to the parameters given for the x-axis and the y-axis). __> transform: translate(100px, 200px);===>>>the div element is moved 100px to the right and 50px down.
<br>
<br>
Positive values will push an element down and to the right of its default position, while negative values will pull an element up and to the left of its default position.An element can also be moved by setting the margins or by positioning the element, although translate is a better choice for animating elements.<br>
<br>
<br>
skew() :
<br>
The skew() method skews an element along the x-axis and the y-axis by the given angles.
<br>
<br>
scale() :
<br>
The scale() method increases or decreases the size of an element, according to the parameters given for the width and height. 1 stands for the original size, 2 for twice the original size, and so on. 
<br>
<br>
Multiple Transforms :
<br>
Multiple transforms can be used at once. Applying multiple transforms to an element is simple; just separate them using spaces.

```
transform: rotate(45deg) translate(100px);

```
<br>
<br>
<br>
 CSS Transitions 
<br>
<br>
<br>
CSS transitions allow you to change from one property value to another over a given duration.Transition effects can be applied to a wide variety of CSS properties, including background-color, width, height, opacity, and many more.

```
div {
   width: 50px;
   height: 50px;
   background: #32CD32;
   transition: width 3s;
}
div:hover {
   width: 250px;
}
```
<br>
In the example , the div element has width and height of 50px, with a green background. We specified a transition effect for the width property, with a duration of 3 seconds.If you hover over the div element, it will start to change its width.When the cursor is moused out of the element, it will gradually change back to its original style.
<br>
<br>
<br>
transition-timing-function :
<br>
<br>
The transition-timing-function property specifies the speed curve of the transition effect.

It can have the following values:
<br>
<br>
ease - the animation starts slowly, then accelerates quickly.

ease-in - starts slowly, then accelerates, and stops abruptly.

ease-out - starts quickly, but decelerates to a stop.

ease-in-out - similar to ease, but with more subtle acceleration and deceleration.

linear - constant speed throughout the animation; often best for color or opacity changes.
<br>
<br>
If no timing function is specified, the default value is ease.
<br>
<br>
<br>
The transition timing function can also be specified in the transition property, like this:

```
transition: width 3s ease-in;
```
<br>
<br>
<br>
We can add a transition on a transform property!Let's make our div rotate when the its hovered:

```
div {
   ...
   transition: transform 1s ease-in-out; 
}
div:hover {
   transform: rotate(90deg);
}
```
<br>
We specify the transform to rotate the div by 90 degrees, and then declare the transition on our transform property.
<br>
<br>
<br>
 A transition can be applied on a transform.
<br>
<br>
<br>
<br>
## CSS Animations 
CSS transitions are generally best for simple from-to movements, while CSS animations are for more complex series of movements.With animations, you can change as many CSS properties as you want to, as many times you want to.An animation is defined using keyframes which hold the styles the element will have at certain times.
<br>
<br>
Keyframes 
<br>
Keyframes are defined using the @keyframes keyword, followed by a name of the animation.

```
@keyframes colorchange {
   [b]0%[/b]  {background-color: red;}
   [b]50%[/b]  {background-color: yellow;}
   [b]70%[/b]  {background-color: blue;}
   [b]100%[/b] {background-color: green;}
}
```
<br>
The example animation will change the background color of an element three times: when the animation is 50% complete, 70% complete, and when the animation is 100% complete.colorchange is the name of the animation. You can choose any name for your animation.

As an alternative to using percentages, you can use from and to keywords, where:

from is a starting offset of 0%

to is an ending offset of 100%.
<br>
To get an animation to work, you must bind the animation to an element.

In the example below, the animation is set for the div element and lasts three seconds:

```
div {
...
   animation-name: colorchange;
   animation-duration: 3s;
}
@keyframes colorchange {
   0% {background-color: red;}
   50% {background-color: green;}
   100% {background-color: blue;}
}
```
<br>
<br>
The animation-name property specifies the animation to be used for the element.

The animation-duration property specifies the duration of the selected animation.
<br>
<br>

There are a number of properties we can set for the animation.

The animation-timing-function:
<br>
specifies the speed curve of an animation. It can have the following values:

ease - specifies an animation with a slow start, then fast, then end slowly (this is default)

linear - specifies an animation with the same speed from start to end

ease-in - specifies an animation with a slow start

ease-out - specifies an animation with a slow end

ease-in-out - specifies an animation with a slow start and end.
<br>
<br>
<br>
animation-delay:
<br>
defines the delay before an animation starts.The animation-delay and animation-duration values can be defined in seconds (s) or milliseconds (ms).
<br>
<br>
<br>
animation-iteration-count:
<br>
determines the number of times an animation repeats. To make the animation repeat forever, just use the s value.
<br>
<br>
<br>
animation-direction:
<br>
indicates how the keyframe should be applied.

The values can be set as:

normal - the default value, which means it plays forward from 0 % to 100%. 

reverse - plays the keyframe in an opposite direction from 100 % to 0%

alternate -  the animation first runs forward, then backward, then forward.

alternate-reverse - the animation first runs backward, then forward, then backward.
<br>
<br>
<br>
A single animation property can be used to achieve the same result as the above code:

```
div {
   animation-name: colorchange;
   animation-duration: 3s;
   animation-timing-function: ease-in;
   animation-delay: 1s;
   animation-iteration-count: infinite;
   animation-direction: reverse;
}
```
<br>
It is the same with:
<br>

```
div { 
   animation: colorchange 3s ease-in 1s infinite reverse;
}
```
<br>


















































                                       








  


  






 





















 







































