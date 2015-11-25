##HTML Tags Review



---




##HTML Syntax

![HTML Syntax](GA/FEWD_Curriculum/img/unit_1/tags.png)

* creates structured documents from page 'parts' (headings, paragraphs, lists, links, footer etc)
* is written in the form of HTML elements consisting of _tags_
* elements either have opening and closing tags: ```<p></p>```
* or are 'empty', they have no closing tag: ```<img>```



---



##HTML Syntax

![HTML Syntax](GA/FEWD_Curriculum/img/unit_1/tags_attributes.png)

HTML tags can also have _attributes_ which are properties written inside the first (opening) tag:

```<img src="smiley.gif" height="42" width="42">```



---



##Main Tags

```<html></html>``` the root container tag for the whole document (web page)

```<head></head>``` the container tag for metadata and links to external files (e.g .css files)

```<body></body>``` contains all the visible structure and content of the web page, _nested_ inside



---



##Content Tags

Heading Elements

```<h1>```Largest Heading```</h1>```

```<h2>``` . . . ```</h2>```

```<h3>``` . . . ```</h3>```

```<h4>``` . . .```</h4>```

```<h5>``` . . . ```</h5>```

```<h6>```Smallest Heading```</h6>```



---



##Content Tags

Text Elements

```<p>```This is a paragraph```</p>```

```<code>```This is some computer code```</code>```

```<span>```For styling words inside a container tag```</span>```



---



##Content Tags

Unordered list
```<ul></ul>```



---



##Content Tags

Unordered list item

```<li>```First item```</li>```

```<li>```Next item```</li>```



---



##Content Tags

links

 ```<a href="Link">```First item```</a>```



---



##Content Tags

```<div></div>```

This is a very widely used generic container tag. It is a rectangular element which can be styled with margins, padding, borders, background-colors, width, height etc. Like many other elements it has block-level display which means it starts on a new line of the page.

`<div>`s can be nested in other `<div>`s


---



##Images

```<img src="smiley.gif" height="42" width="42">```

The `img` tag requires a `src` attribute, which tells the browser where to find the image.



---



##Images

How would you write the src?

![](GA/FEWD_Curriculum/img/unit_1/folder_structure.png)

*	There are different approaches to specifying an image location



---

##Images

*	Inside ```webroot```, a relative path could be used:

####```<img src="images/logo.png">```

---

##Images
Relative Path

![Parent Folder Structure](GA/FEWD_Curriculum/img/unit_1/folder_structure_parentDirectory.png)

* Given this folder structure the same image would be ```<img src="../images/logo.png">```
* ```../``` means to go up a directory, and can be used repeatedly: `../../` would go up two directories.


---

##Images

Absolute Path

```<img src="/images/logo.png">```

Absolute URLs start with a `/`, which implies the `root` directory of your web site.

Note:

Absolute URLs start with a `/`, so if we imagine that our `webroot` directory was stored on a server such that the `webroot/index.html` file is accessible at `http://example.com/index.html`, then placing the logo image could be done from any html page with: ```<img src="/images/logo.png">```

The benefit here is that this same ```src``` path works on any html page, no matter what its location, so the same ```img``` tag can be used on both the ```webroot/index.html``` page and the ```webroot/about/index.html``` page.

The downside is that the path only works if the project is stored to a proper location for serving.


---


##Images
Full URL

		<img src="https://ga-core.s3.amazonaws.com/production/uploads/program/default_image/397/thumb_User-Experience-Sketching.jpg">

Note:
For linking to images, make sure that you have permission to use the image in this way. Even then, it is often better to host a copy of the same image, rather than link to another server, because it reduces dependency.


---

##Images

alt attribute

	<img src="puppy.jpg" alt="My cute puppy">

Note:

A piece of text to be used in lieu of the image when the image is unavailable

Using `alt` attributes has the added benefit of giving search engines more linguistic context about the image as it is used on your page.

Reasons an image may not load:

*	There was a connection error, the browser didn't download the image.

*	The file was not found, perhaps because the image got moved elsewhere and the page wasn't updated yet to reflect the change.

*	The user is running a text-based browser such as an older phone with a WAP-style browser, or a non-graphical browser like lynx.

*	The user is using a screen reader because she has low vision, which will read the `alt` text aloud or present it through a braille reader.



---



##HTML vs HTML5

HTML5 is HTML with a few additions
The Doctype tells you if the page is HTML5 ready.


```<!DOCTYPE html>```


##HTML HISTORY

![HTML History](GA/FEWD_Curriculum/img/unit_1/Timeline_of_web_technologies.jpg)

Note:
image retrieved from http://www.onbile.com/info/wp-content/uploads/2013/09/Timeline-of-web-technologies-639x168.jpg on October 1, 2013.


---


##HTML5

* brings many improvements and new features to web pages
* many features of HTML5 have been built to run on low-powered devices such as smartphones and tablets
* introduces the new ```<video>```, ```<audio>``` and ```<canvas>``` tags
* introduces many new structural document tags, e.g. ```<main>```, ```<section>```, ```<article>```, ```<header>```, ```<footer>```, ```<aside>```, ```<nav>``` and ```<figure>``` - these are like ```<div>``` but with a semantic styleable name.
