---
title: jQuery
summary: "Using jQuery to build and work with the DOM."
---

# {{ page.title }}
{{ page.summary }}

## What is jQuery?
jQuery is an awesome, widely-used library to work with the DOM in a more friendly and consistent cross-browser manner. The way that we work with the DOM in jQuery is a lot more friendly than what we learned with base JavaScript only. For example it allows you to create an element with child elements or text in a single step!

## Getting jQuery
To add jQuery to your page, add a script tag for the current version of the (full not slim) jQuery core minified file from the [jQuery MaxCDN](https://code.jquery.com/).

{% highlight html %}
<script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
{% endhighlight %}

## Using jQuery
The best source on jQuery is their own [jQuery API Documentation](http://api.jquery.com/).

Much of the work is done by the [jQuery function](http://api.jquery.com/jQuery/).  And yes, jQuery is both the name of the library and the name of the core function in the library. You do a lot of work with the jQuery function.

This function is used for three things:

1. Setting a callback for when the DOM has loaded in the browser by passing in a function
2. Selecting elements from the DOM by passing in a selector
3. Creating new elements (to later add to the DOM) by passing in an HTML string

## Other important functions
There are also a series of other functions that act on a jQuery object.  A [jQuery object]()http://api.jquery.com/Types/#jQuery is returned from the jQuery function when you pass in a selector or an HTML string.

We will focus on jQuery methods for:

- [DOM manipulation](http://api.jquery.com/category/manipulation/)
	- [attr](http://api.jquery.com/attr/)
	- [addClass](http://api.jquery.com/addClass/), [removeClass](http://api.jquery.com/removeClass/), [toggleClass](http://api.jquery.com/toggleClass/)
	- [val](http://api.jquery.com/val/)
	- [text](http://api.jquery.com/text/)
	- [append](http://api.jquery.com/append/)
	- [remove](http://api.jquery.com/remove/)
- [Events](http://api.jquery.com/category/events/)
	- [on](http://api.jquery.com/on/)
	- [focus](http://api.jquery.com/focus/)
- [Visual Effects](http://api.jquery.com/category/effects/)
  - [toggle](http://api.jquery.com/toggle/) - show/hide

## Ajax with jQuery
Ajax is a way to make HTTP requests for data that allow you to make	updates to a part of your HTML page without needing to reload the entire page. We didn't look at this with base JavaScript as the way to do it has varied across browsers.  With jQuery, they handle that for us within the library, making the code more straightforward.

- [Ajax](http://api.jquery.com/category/ajax/)
  - [getJSON](http://api.jquery.com/jQuery.getJSON/)

Remember the code inside the function passed to getJSON is only called if the Ajax request is successful. Chain on appropriate *promise* methods for `fail` and/or `always` to handle errors.

{% highlight JavaScript %}
$.getJSON( "myData.json", function() {
  console.log( "Request was successful!" );
})
.fail(function() {
  console.log( "Request failed." );
})
.always(function() {
  console.log( "Put any code that should always happen - success or failure - here." );
});
{% endhighlight %}

Additional notes on Ajax:
 - Browser security restricts, most "Ajax" requests are subject to the [same origin policy](https://en.wikipedia.org/wiki/Same-origin_policy). This means that requests can not get data from a different domain/subdomain or protocol.
 - JSONP requests are not subject to the same origin policy restrictions and a sometimes used to work around this policy.
