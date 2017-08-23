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

Variables and types are covered in [Chapter 1 of Eloquent JavaScript](http://eloquentjavascript.net/01_values.html), but this information is a little outdated.  There is the old way to make variables using `var` and this has one set of JavaScript scoping rules & there is the new ES6 way which uses `let` and `const` and has different scoping rules.  

The ES6 way is *much* friendlier and more intuitive for developers used to other languages. Read the information on ES6 in [Section 4.1 of Exploring ES6](http://exploringjs.com/es6/ch_core-features.html#sec_from-var-to-const).

I will expect you to understand both the old syntax and the new, as currently many programs existing will not be using the new ES6 syntax.  However I will expect you to write code using the ES6 syntax.

## Additional JS Syntax
Basic programming structures are covered in [Chapter 2 of Eloquent JavaScript](http://eloquentjavascript.net/02_program_structure.html).

Basic functions are covered in [Chapter 3 of Eloquent JavaScript](http://eloquentjavascript.net/03_functions.html).

Basic objects and arrays are covered in [Chapter 4 of Eloquent JavaScript](http://eloquentjavascript.net/04_data.html). I will expect you to already have knowledge of arrays, but we will cover objects more in the next module.
