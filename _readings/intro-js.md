---
title: Introduction to JavaScript
summary: "An introduction to basic JavaScript syntax."
---

# {{ page.title }}
We're going to run through basic syntax very quickly, as it is assumed that you already have the basics of programming down from learning some other language. We'll be learning syntax for variables, functions, arrays, and basic programming constructs for branching or conditional statements and iteration (or looping). Basically everything you would cover in a first programming course, we're going to learn the JS (JavaScript) syntax for that this week.

Don't worry if you need to refer back to the web, examples, or your notes for a bit on the exact syntax as the more you do it, the more you'll remember it. However it is important that you understand what all this all means. I'll expect you to use these things (functions in particular) without being told specifically to do it.

## Adding JavaScript to a Web Page
Let's start with how to add JavaScript to a basic web page.  This is done using the `<script>` HTML tag.  This tag can be used to embed JavaScript code directly into the page or it can reference a separate JavaScript file.

Embedding JavaScript directly into the page:

{% highlight html %}
  <script>
    console.log("Hello World");
  </script>
{% endhighlight %}

Referencing JavaScript in a separate file:

{% highlight html %}
  <script src="script.js"></script>
{% endhighlight %}

When using multiple JavaScript files, the order of your script tags is important if you have dependencies between them.  Any libraries that are used by your own script need to be added __before__ your script in order for the library code to be available to your script.


## Variables & Values
JavaScript is not a strictly typed language. This means that you do not need to specify the type of a variable when you define it, and that a variable can hold any value. The same variable can hold numbers, strings, or even objects. This is similar to python, for example, but different from Java or C#.
