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



 





















 







































