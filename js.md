##JavaScript and the DOM

JavaScript in the browser has an API (application program interface) for accessing and editing the DOM (the document object model) of an HTML document. The DOM is a hierarchical tree representation of the structure of the HTML in a web page.

JavaScript can target specific elements on an HTML page and show, hide, style, edit and animate them. It can also listen for events emitted by an HTML page (e.g mouse-clicks) and invoke functions when an event occurs.

---

##JavaScript and the DOM

JavaScript gets a reference to elements with (for example)
```
document.getElementById()
```

The JQuery library provides easier ways to do this, but is not actually necessary.

---

##JavaScript and CSS

You can dynamically set CSS classes on elements with JavaScript.

Open up the 'jsfb-styling-css-with-js' in the 'js-for-beginners' folder and open `lesson.html` in your browser

---

##JavaScript and CSS

The same thing can be achieved with jQuery using less code, _but you have to import the jQuery library too!_

Open up the 'jsfb-styling-css-with-jquery' in the 'js-for-beginners' folder and open `lesson.html` in your browser

---

##JQuery

JQuery is a JavaScript library that does the following:
* Access parts of the HTML page
* Modify the appearance of the page
* Edit the page
* Respond to user interaction
* Add animation
* Retrieve data from a server using AJAX (Asynchronous JavaScript and XML)
* Simplify common JavaScript tasks

---

##JQuery

JQuery also provides the following useful features:
* uses CSS selector syntax
* supports extensions
* abstracts away browser quirks
* allows multiple actions to be defined in one line with chaining

---

##JQuery scrolling

Firstly lets create some `<a>` anchor tags that link to other parts of your same page. If you are linking to a spot on the same page, the format of the link will be similar to:
```
<a href="#my-anchor">Jump to contact details</a> //note the # (hash)!
```

Now set the anchor where the first `<a>` will link to. The anchor should be placed at the beginning of the line where you want to start reading after you jump:
```
<p><a name="my-anchor"></a>Hey you can contact me at blah@blah.sg</p>
```
or you can target the id of a `<div>`
```
<div id="my-anchor">
```

---

##JQuery scrolling

Now make sure `jQuery` is linked in the `<head>` of your page:
```
<script src="https://code.jquery.com/jquery-1.11.3.min.js"></script>
```

Create a file called `scrollLinks.js` and put it in the root of your current folder. Then create another `<script>` link in your `<head>`:
```
<script defer src="scrollLinks.js"></script>
```

---

##JQuery scrolling

Now copy and paste the following code into `scrollLinks.js`

```
$(document).ready(function(){
	$('a[href^="#"]').on('click',function (e) {
	    e.preventDefault();
	    var target = this.hash;
	    var $target = $(target);
	    $('html, body').stop().animate({
	        'scrollTop': $target.offset().top
	    }, 900, 'swing', function () {
	        window.location.hash = target;
	    });
	});
});
```

When you click on an `<a>` that links to another part of your page, the page should scroll to that position.

---

##NodeJS Express server example

`cd` to the 'hello-express-programmers' folder in your Terminal. We now need to install dependencies via the command line
```
npm i express --save
```
```
npm install
```

Now run the server with
```
npm start
```
