<!-- .slide: style="text-align: left;"> -->  

##CSS Review

---


##CSS

* is a styling (stylesheet) language used for describing the presentation of an HTML document
* it separates document content from document presentation, including control of layout, colors, and fonts
* it makes the page much easier to edit and update, and improves accessibility
* multiple HTML pages can share the same formatting by writing the CSS in a separate .css file and linking to it from your HTML page


---


##CSS Syntax

![](GA/FEWD_Curriculum/img/unit_1/css_syntax.png)

---


##CSS

Where does CSS go?

* Inline with the `style` attribute

```
<h1 style="color: red;">Hello World</h1>
```

* In the `head`

```
<head>
 <style>h1 {color: red;}</style>
</head>
```

* In a separate file (best option)

```
<head>
	<link rel="stylesheet" type="text/css" href="path/to/some.css">
</head>
```


Note:
CSS should go in a separate file. We're going to start by placing them in the head for convenience and to learn the syntax. We'll show inline styles at the end, just to demonstrate.


---

##CSS

Using a separate CSS file

It is best practice to put CSS in its own file and link to it from the `<head>`.

```<link rel="stylesheet" href="style.css">```

Note:
"The `link` tag needs two attributes: `rel="stylesheet"` and an `href` attribute.

The `href` attribute value works very similarly to linking to an image, or to another page.


---

##CSS Break Down

```
p {
	color: red;
	font-weight: bold;
}
```
---

##CSS Break Down

This whole thing is called a **rule**.

The `p` is called a **selector**, and it's followed by a set of **declarations** in a **declaration block**.

---

##CSS Break Down

The **selector**, `p` in this case, specifies what parts of the HTML document should be styled by the declaration. This selector will style all `p` elements on the page.

---

##CSS Break Down

The **declaration block** here is:

```
{
	color: red;
	font-weight: bold;
}
```

**Declarations** go inside curly braces.

Every declaration is a **property** followed by a **value**, separated by a colon, ending in a semicolon.

---


##Cascading Style Sheets (CSS)
###Colors

Colors can be specified in CSS in a variety of ways:

* keyword (e.g. `red` or `blanchedalmond`)
* hex codes (e.g. `#FF0000`)
* `rgb(0,0,0)`
* `rgba(255, 255, 255, 0.8)`
* `hsl(0, 100%, 50%)`
* `hsla(0, 100%, 50%, 0.8)`

Today we'll use keywords : <http://www.w3schools.com/html/html_colornames.asp>


---

##CSS Selectors

if you want to directly style all elements of a certain type (e.g all `<p>` tags) they you style `p`

```
p {color: red;}
```

if you want to apply styles to individual elements then use '#' (hash/id) selectors. This selects one  element on your page with an unique id attribute

```
#my-id {color: green }
```

if you want to apply styles to groups of elements then use '.' (dot/class) selectors. These select elements which have a corresponding class attribute.
```
.my-class {color: blue }
```

---

##CSS Selectors

There are many other selectors and each has a different level of importance. This means it can either be overwritten by, or can overwrite another style.

See: <http://code.tutsplus.com/tutorials/the-30-css-selectors-you-must-memorize--net-16048>


---

##CSS Selectors Exercise

In the `blank` folder of the downloaded working files, do the following:

Copy this code into `lesson.css`

```
#my-id { color: green; background-color: white; }
.my-class { color: blue; background-color: yellow; }
```

Copy this code into `lesson.html`

```
<p id="my-id">There should only be one of me.</p>
<p class="my-class">There can be many of me.</p>
<p class="my-class">There can be many of me.</p>
<p>This text has <span class="my-class">a styled bit</span> inside</p>
```

---

##CSS Style Properties

There are many CSS styling properties. Some can be applied to all types of tags, others only work on certain tags.

* `color`: sets the color of text
* `background-color`: sets the color of the background rectangular area, including the padding
* `width`: sets the width of the element in different units
* `height`: sets the height of the element in different units
* `font-family`: sets the text font
* `font-weight`: sets the text font weight - e.g. `bold` or can be a numeric value

---

##CSS Style Properties

These properties relate the to the `box model` and positioning

* `margin`: sets the outer transparent rectangular border of an element as part of the box model
* `border`: sets the visible rectangular border style of the element as part of the box model
* `padding`: sets the inner transparent rectangular border of an element as part of the box model
* `display`: sets the layout of the element in the 'flow of the page'


Note:
Explain the box model again in Chrome dev tools

---

##CSS Box Model

The CSS box model is essentially a box that wraps around every HTML element. It consists of: margins, borders, padding, and the actual content.

In terms of visibility, `margin` area is transparent, `padding` area inherits background-color, `border` has its own style and color properties.

You can see a representation of the box model for an element in Chrome dev tools (Cmd + Alt + I), in the 'Elements' tab.

---

##CSS Style Properties

`margin`, `border` and `padding` have individual properties for each side of the rectangle.
* **margin-top, margin-left, margin-bottom, margin-right**
* **border-top, border-left, border-bottom, border-right**
* **padding-top, padding-left, padding-bottom, padding-right**

These values can also be set with shorthand:
* `margin: top right bottom left`; (clockwise)
* `margin: top-and-bottom left-and-right`;

---

##CSS Style Properties - borders

Border has its own style and color properties:
* `border-width` (number px)
* `border-style` (string)
* `border-color` (string or hex value)

It is commonly set as border: width style color;

```border: 4px dashed red;```

---

##CSS Style Properties - borders

Border style properties: `none` (low priority), `hidden` (high priority), `dotted`, `dashed`, `solid`, `double`, `groove`, `ridge`, `inset`, `outset`

Don't forget `border-radius`

`border-radius:50%;` makes a square into a circle

---

##CSS and `<div>` Exercise

Remembering that a `<div>` can be styled and nested inside another `<div>`, try and do the following:
* create a circle inside a square
* create the Singaporean flag (without the stars)

Your code should look something like:
```
<div class="parent-class">
	<div class="child-class"></div>
</div>
```

The demo is here, but have a go without looking first
<http://codepen.io/wilkom/pen/OyrPzV>

Work in the `blank` folder of the downloaded working files

Note:
Tell students to copy, rename and clear the blank folder for each exercise

---

##CSS Positioning

You can also position `<div>`s (or other HTML tags) with exact values using the `position` property and `top`, `left`, `bottom`, right properties.

`position` has the following values:
* `static`: default positioning in the document flow
* `absolute`: positioned relative to its first non-static ancestor element
* `fixed`: positioned relative to the browser window
* `relative`: positioned relative to it's normal default position

---

##CSS Positioning Exercise

Go to this link:
<http://codepen.io/wilkom/pen/xwmPeL>

You can see the top and left properties set on the different classes that are applied to the `<div>`s.

---

##CSS Overflow of an element

What happens when we put some content into a container and the content is bigger than the container? This can happen particularly when you want to put some text inside a container of a fixed size, but the text requires more space than the container has available.

Open up the folder named `overflow-text` and open the `lesson.html` file in your browser

---

##CSS Overflow of an element

For this we used the `overflow` property in the container. It has the following values:

* `visible`: (default) the content will ‘break out’ and be visible
* `hidden`: any overflowing content will be hidden
* `scroll`: the content is clipped and scroll bars will always be available
* `auto`: the content is clipped and scroll bars should be available
* `initial`: default value
* `inherit`: inherits from parent container

---

##CSS Overflowing nested images

Open up the folder named `nested-image` and open the `lesson.html` file in your browser

See if you can get the image to scale down be 'sitting inside' the parent `circle`. Hint there is a class you can use in the `lesson.css`.

Note:
Show different ways of applying the img style

---

##CSS Flow of an element in the page layout

The display property affects how an element is positioned in the 'flow' of the page.  

`display` has the following values:

* `block`: means the element 'moves down' the page
* `inline`: means the element 'moves across' the page
* `inline-block`: means the element is inline and the inside of this element is block
* `flex`: this is a big new thing that makes layouts easier

---

##CSS Flexbox

Flexbox is a new way of laying out the flow of elements in a web page.

It is a definite improvement in layout techniques for web pages. A good link explaining Flexbox is here:

<https://css-tricks.com/snippets/css/a-guide-to-flexbox/>

It is now fairly well supported in browsers (going back to IE9 using prefixing), and so should be used in front-end web development going forward.


---

##CSS Page Layout pre-Flexbox

Open up the folder named `web-page-float-layout` and open the `lesson.html` file in your browser

Before Flexbox the most common way of doing a page layout involved `floats`. The `float` property in CSS was originally intended for making content 'float alongside' other content. It ended up also being used to float containers alongside each other (e.g. sidebars in a web page).

---

##CSS Floats

* You can 'float' elements to the left or right of a parent container.
* Floats are often used for page layouts  - for example to have a sidebar
* You need to use the `clear` property in the style of the element that comes after the container of the floated elements. This stops the float continuing in the rest of the page. By convention a style for clearing a float is commonly called a `clearfix`.

---

##CSS Float layout styles

```
.sidebar{
   float:left;
}
```

```
.clearfix{
   clear:left;
}
```

---

##CSS Clearing Floats

You need to clear `floats` for different reasons - whether you are still inside the container of your floated elements or back up on the same level as the container.

In both cases a `clear` will fix things, but because things are different inside and outside the container there are also other  approaches to clear-fixing. Basically floated items in a container will cause the container to collapse so this will affect subsequent elements at the container level, as well as elements in the container.

See <http://www.sitepoint.com/clearing-floats-overview-different-clearfix-methods/>

---

##CSS HTML5 Tags layout

Open up the folder named `web-page-h5` and open the `lesson.html` file in your browser.

This page layout does not use `floats` but doesn't use Flexbox either. It is a single column layout with a 'sticky footer'.

It uses HTML5 semantic tags which can be styled directly.

---

##CSS Flexbox layout

Flexbox's algorithm works on the basic principles of elements flowing (vertically or horizontally), wrapping, and expanding or shrinking according to different page sizes (e.g for a laptop screen vs a tablet screen vs a mobile phone screen).

Open up the following working files in the browser and play around with resizing the window:
* flexbox/holy-grail-layout/index.html
* flexbox/flexible-column-layout-with-rows/index.html

---

##CSS Flexbox vertical centering

Another old problem that Flexbox solves easily is vertically centering text. Previous ways of doing this involved hackery or limitations (e.g. content could only be on one line).

Go to this link to see examples of vertically centered text:

<http://codepen.io/wilkom/pen/NGeyNg>

---

##CSS fonts

In our web pages we can use the system fonts that come with most operating systems, like Times, Arial and Helvetica.

But what if we want to use a really cool font, and embed it so that anyone who visited our web page would see that font. Enter the CSS3 font embedding syntax.
```
@font-face { font-family: MyFont; src: url('path/to/MyFont.ttf'); }
```

Now go and download some cool free fonts and put them in your project folder:
<http://www.dafont.com/>

Use the `font-family: MyFont;` property to apply that font to a given tag

---

##CSS3 transitions

CSS3 which is the latest well supported version of CSS gives you the ability to add transition animations to your HTML elements. We use the `transition` property.

We can add some transitions to specific properties so that they change smoothly over time. One place we can do this is when an `a:hover` style is applied to an `<a>` anchor tag.

```
-webkit-transition: background-color 2s;
transition: background-color 2s;
```
<https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Transitions/Using_CSS_transitions>
