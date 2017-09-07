---
title: JavaScript Objects
summary: "General information on understanding and working with JavaScript objects."
---

# {{ page.title }}
{{ page.summary }}.

## JavaScript & the Browser
[Chapter 6 of Eloquent JavaScript](http://eloquentjavascript.net/06_object.html) provides some general background and history on objects and methods - the backbone of any Object Oriented programming language. However it also introduces a somewhat unique twist on OO found in JavaScript, prototypes. A __prototype__ is a fallback basis for a JavaScript object's properties & methods. It behaves in someways like inheritance, but unlike a base or parent class, a prototype is a working object instance.  

You can read more about prototypes and inheritance in this article: [Master the JavaScript Interview: What’s the Difference Between Class & Prototypal Inheritance?](https://medium.com/javascript-scene/master-the-javascript-interview-what-s-the-difference-between-class-prototypal-inheritance-e4cd0a7562e9)


## Document Object
In the [GitHub: JS Hello World]({{ "/experiences/intro-hello-world.html" | prepend:site.baseurl }}) assignment, we saw that we could write to a web page using:
{% highlight js %}
document.write("Hello World");
{% endhighlight %}

This illustrates the common *object dot method* syntax used by JavaScript (and many other Object Oriented language) to call methods on an object.

However, we also learned that this was not a very good way to write to the page. It doesn't allow us to be very specific about what part of the page we want to write to.  In the next reading, we'll learn how to access and modify specific parts of a web page using the JavaScript document object.
