---
title: Moonflower's Coffee Part 2
summary: "In this exercise we will create a web page from embedded JSON data. "
---

# {{ page.title }}
{{ page.summary }}


## Accept the assignment
Click the link below, then on the web page, click the green button to accept the assignment.

[Assignment: js-moonflowers]( https://classroom.github.com/a/NagdYc2F )

Note that once you accept this assignment, you will continue working with the same repository on GitHub for later parts of the assignment and will not need to accept the assignment again.


### Menu Information
The JS file has JSON for the menu information to be presented on the page. You will need to use the data from that object to build an HTML menu to add to the menu section.  

When adding the table, remove the default text that is initially present in the menu section. You will build HTML with a heading and menu table for each category of menu items.

The beverage item table should be first, followed by the bakery items, and the other items should be last.  

The tables should be laid out as follows:

H3 Heading (“Beverage”, “Bakery”, or “Other Products”)
Item 1 name | Price | Image
Item 2 name | Price | Sorry, no image.
Item 3 name | Price | Image

Of there is an image file, add an appropriate HTML image tag with the src and alt text.  However, the image property may not be present in the JSON for some items. In this case, that table cell should contain italicized text saying “Sorry, no image.”

Remember that you can make HTML tables as follows:
<table>
    <caption>Basic Table</caption>
    <tr>
        <td>Row 1, Column 1</td><td>Row 1, Column 2</td><td>Row 1, Column 3</td>
    </tr>
    <tr>
        <td>Row 2, Column 1</td><td>Row 2, Column 2</td><td>Row 2, Column 3</td>
    </tr>
    <tr>
        <td>Row 3, Column 1</td><td>Row 3, Column 2</td><td>Row 3, Column 3</td>
    </tr>
</table>


## Write good JavaScript code!

- Use functions to break down the functionality into small tasks
- Practice good coding standards with clear variable and function names, use $ for variables that will hold jQuery objects, use ES6 `let` and `const` instead of `var`
- Make sure your variables are well named.  Avoid abbreviations and use camelCase to make multi-word names readable.

## Final Testing
When you are done, push your files to GitHub, then make sure that your page displays and runs correctly on the GitHub website.  

Don't forget the Pull Request.  Put a screenshot of the open request in the assignment dropbox.
