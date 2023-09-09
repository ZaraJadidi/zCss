## What is CSS ?<br>

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

##### Class Selectors: Often we need to target only a subset of elements, without changing the others. This can be done using a class selector.We first need to add a class attribute to the elements we want to target. 
the class selector needs to start with a dot, followed by the class name that we gave to our element.<br>

##### Id: We can also create selectors based on the id attribute of elements.This is done by using the hash (#) symbol before the id value.You can have only one element with the same id on the page, while the class value can be used multiple times.<br>

##### Besed on location: We can also target elements based on their location.For example, there are two strong elements, one inside a paragraph and the other inside a list item.We can target only the one inside the list item by using the following rule:
in css file: li strong{..}<br>

### Styling Texts <br>

color : change color of the text. Besides color names, a color value can also be set using hex and rgb values.Colors are displayed in combinations of red, green, and blue light (RGB).Hex values are written using the hashtag symbol (#), followed by six hex characters, which define the components:




































