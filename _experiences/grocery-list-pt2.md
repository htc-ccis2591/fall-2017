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
Continue working with the repository from the previous assignment.  You __DO NOT__ need to accept the assignment again.

[Grocery List: Part 1]( {{ "/experiences/grocery-list-pt1.html" | prepend:site.baseurl }} )

## Requirements
Behavior:

- Add a button to save all of the items in the to the local browser storage
- When the page loads, it should check the local browser storage for saved items and add them to the list.

To do this, you should go through all of the list items in the grocery list `ul`, pull out the text, and then stash it in an array. (What code structure would you need to go through all the items in a list?)

__Don't save the HTML elements.  Only save the text.__  

Then use the `localStorage` methods:
  - setItem()
  - getItem()
and the `JSON` methods:
  - stringify()
  - parse()
to read and write the array from the browser local storage.


## Write good JavaScript code!

- Use functions to break down the functionality into small tasks
- Practice good coding standards with clear variable and function names, use ES6 `let` and `const` instead of `var`
- Make sure your variables are well named.  Avoid abbreviations and use camelCase to make multi-word names readable.

## Final Testing
When you are done, push your files to GitHub, then make sure that your page displays and runs correctly on the GitHub website.  

Don't forget the Pull Request.  Put a screenshot of the open request in the assignment dropbox.
