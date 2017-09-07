---
title: JavaScript Document Object
summary: "An introduction to the JavaScript document object and methods for working with the DOM."
---

# {{ page.title }}
{{ page.summary }}.

## JavaScript & the Browser
[Chapter 12 of Eloquent JavaScript](http://eloquentjavascript.net/12_browser.html) provides some general background and history on the internet, browsers, HTML and JavaScript.  While this information is more conceptual, it is helpful in understand why things work the way they do. Somethings in the JS world make much more sense with an understanding of its history.


## Document Object
[Chapter 13 of Eloquent JavaScript](http://eloquentjavascript.net/12_browser.html) introduces the Document Object Model or DOM. The overall structure of HTML and the DOM should already be familiar to you, and you should have a solid understanding of parent-child and sibling relationships between HTML elements. This will be necessary as we begin to work with the DOM using JavaScript.

## DOM Methods
More information and examples of using these methods can be found in the reading, but the best way to understand them is to work with them.  Make a simple page and experiment.

### Methods to get elements
The following method will always return a single element, identified by its `id` attribute:

- getElementById(idName)

Remember in a valid HTML document, the value of the `id` attribute must be unique to a page. This will return the first element found with that id value, even if it is not the *only* one.

The following methods will always return a set of elements:

- getElementsByTagName(tagName)
- getElementsByClassName(className)
- querySelectorAll(cssSelector)

When working with a set of elements, you will either need to get a specific single element or use a loop to work with each one in turn.

### Methods to navigate the DOM
Once you have identified a particular element, it is often helpful to be able to move around and access other elements nearby.  The following methods allow us to use a specific element to access its parent, children and sibling elements.

These method return either elements or text/whitespace nodes:

- parentNode()
- firstChild()
- lastChild()
- nextSibling()
- previousSibling()
- childNodes()

When working with these methods, it is important to check the result type. You can check the property `nodeType` to see if the type is an element or text.  You can also use the `nodeValue` property to get or set the value. The value is dependent upon the `nodeType`. For a TextNode, the value will be the text content.  For an ElementNode, the value is a NodeList of the element's children.

Sometimes it is helpful to avoid the text and only work with elements. The following methods only return an element:

- parentElement()
- firstElementChild()
- lastElementChild()
- nextElementSibling()
- previousElementSibling()
- children()

### Working with Attributes
When dealing with HTML elements from the DOM, it is often necessary to work with their attributes.  The following properties and methods allow us to get and set attribute values.

Properties:

- className
- id

Methods:

- hasAttribute(attrName)
- getAttribute(attrName) - returns attribute value
- setAttribute(attrValue)
- removeAttribute(attrName)

### Modifying the DOM
One of the most useful aspects of JavaScript today is its ability to make updates to the content of an HTML page. This allows the web to behave more dynamically, giving us information like the current weather, stock prices, and availability of items and their prices in online market places. Much of the value in the Web today is its ability to give us current information, and JavaScript is often the technology that makes this possible.

The following methods allow us to create new elements and text to add to the DOM:

- createElement(elementName)
- createTextNode(textString)

Once we have created a new element or text node, we can add it to the DOM as a child of another element using the `appendChild` method. We can also remove an existing element or text node by using the `removeChild` method.
