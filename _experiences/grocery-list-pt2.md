---
title: Grocery List - Part 2
summary: "In this exercise we will update our grocery list web page to remember the items in the list. "
---

# {{ page.title }}
{{ page.summary }}

## Prerequisites
Make sure that you have completed the following prerequisites before beginning:

- [More on Events]({{ "/readings/js-events-deeper.html" | prepend:site.baseurl }})
- [Objects & JSON]({{ "/readings/json-intro.html" | prepend:site.baseurl }})  
- [Browser Storage]({{ "/readings/browser-storage.html" | prepend:site.baseurl }})

## Accept the assignment
Click the link below, then on the web page, click the green button to accept the assignment.

[Assignment: grocery-list]( https://classroom.github.com/a/TBvx_wrr )

Note that once you accept this assignment, you will continue working with the same repository on GitHub for later parts of the assignment and will not need to accept the assignment again.

## Requirements
Behavior:

- Click on items to remove them from the list
- Add Item button should:
  - hide the button
  - show the form
- Form submit should:
  - add a new item to the list
  - then hide the form
  - show the New Item button


## Starter Files
Before beginning, review the HTML & CSS files provided for you. Also note that there is an empty JavaScript file as well.  It is located in the `js` folder.  Note that the script tag that includes this file uses the folder name in the path.

{% highlight html %}
<script src="js/grocery-list.js"></script>
{% endhighlight %}

To show or hide elements, you can add or remove the `hide` style class from them. (Part of Bootstrap)



## Write good JavaScript code!

- Use functions to break down the functionality into small tasks
- Practice good coding standards with clear variable and function names, use $ for variables that will hold jQuery objects, use ES6 `let` and `const` instead of `var`
- Make sure your variables are well named.  Avoid abbreviations and use camelCase to make multi-word names readable.

## Final Testing
When you are done, push your files to GitHub, then make sure that your page displays and runs correctly on the GitHub website.  

Don't forget the Pull Request.  Put a screenshot of the open request in the assignment dropbox.
