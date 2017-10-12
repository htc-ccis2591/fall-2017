---
title: Grocery List Using jQuery
summary: "In this exercise we will rewrite the Grocery List project to use jQuery."
---

# {{ page.title }}
{{ page.summary }}

## Prerequisites
Make sure that you have completed the following prerequisites before beginning:

- [jQuery]({{ "/readings/jquery.html" | prepend:site.baseurl }})

## Accept the assignment
Click the link below, then on the web page, click the green button to accept the assignment.

[Assignment: js-grocerylist-jquery]( https://classroom.github.com/a/CJrcLLtQ)


## Requirements
We will keep the same behavior that we had originally in Part 1 of the assignment with base JavaScript:

- Click on items to remove them from the list
- Add Item button should:
  - hide the button
  - show the form
- Form submit should:
  - add a new item to the list
  - then hide the form
  - show the New Item button


## Starter Files
Before beginning, review the HTML & CSS files provided for you. There is an empty JavaScript file provided in the `js` folder. Both jQuery and this script file are linked at the bottom of the HTML file for you.

The jQuery file is also required by Bootstrap.  

{% highlight html %}
  <!-- jQuery (necessary for Bootstrap's JavaScript plugins) -->
  <script src="https://code.jquery.com/jquery-3.2.1.min.js"></script>
  <!-- Latest compiled and minified Bootstrap JavaScript -->
  <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js" integrity="sha384-Tc5IQib027qvyjSMfHjOMaLkfuWVxZxUPnCJA7l2mCWNIpG9mGCD8wGNIcPD7Txa" crossorigin="anonymous"></script>

  <!-- Grocery List JS which also uses jQuery! -->
  <script src="js/grocery-list.js"></script>
{% endhighlight %}


## Notes on show/hide
In the original assignment, we controlled the display of elements by adding or removing the `hide` style class (part of Bootstrap) from the element.

With jQuery, we have a few options on how to do this.  Since the elements are already hidden by having this class added to them in the HTML, it is best to continue to show/hide the elements using this class.  We can do this two ways:

1. Adding and removing the *entire* class attribute. This could be done with the [attr](http://api.jquery.com/attr/) method. This would work now because no other style classes are on these elements.  However this is not a good approach as it could cause problems later if other styles are added.
2. Adding and removing (toggling) the specific style class. This is a better approach for long term maintainability of the code. This is done using either:
 - the [addClass](http://api.jquery.com/addClass/) and [removeClass](http://api.jquery.com/removeClass/) methods
 - OR the [toggleClass](http://api.jquery.com/toggleClass/) method  


## Write good JavaScript code!

- Use functions to break down the functionality into small tasks
- Practice good coding standards with clear variable and function names, use $ for variables that will hold jQuery objects, use ES6 `let` and `const` instead of `var`
- Make sure your variables are well named.  Avoid abbreviations and use camelCase to make multi-word names readable.
- If you store jQuery objects in a variable, start the variable name with $ to indicate it is a jQuery object.


## Final Testing
When you are done, push your files to GitHub, then make sure that your page displays and runs correctly on the GitHub website.  

Don't forget the Pull Request.  Put a screenshot of the open request in the assignment dropbox.
