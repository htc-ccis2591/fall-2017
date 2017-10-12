---
title: Moonflower's Coffee with jQuery
summary: "In this exercise we will rewrite Moonflower's Coffe using jQuery and JSON data stored in separate files."
---

# {{ page.title }}
{{ page.summary }}


## Accept the assignment
Click the link below, then on the web page, click the green button to accept the assignment.

[Assignment: js-moonflowers-jquery]( https://classroom.github.com/a/UpEZq0hk )


## Requirements
In this exercise we will rewrite the existing behavior of the Moonflower's Coffee page (both parts 1 and 2) to be done using jQuery.

### Menu Information
The menu.json file contains the JSON for the menu information that will be presented on the menu section of the page.  This information will be broken up into a heading and table for type of content: Beverage, Bakery, & Other. Before adding the tables, remove the default text that is initially present in the menu section.

Each menu category will have:
- an H3 heading (“Beverage”, “Bakery”, or “Other Products”)
- a table of menu items, showing the name, price & image (if present)

The beverage item table should be first, followed by the bakery items, and the other items should be last.  

The tables should be laid out similar to the following example:
<table class="table table-bordered" style="width:60%">
    <tr>
        <th>Item</th><th>Price</th><th>Image</th>
    </tr>
    <tr>
        <td>Item 1 name</td><td>Price</td><td>(image)</td>
    </tr>
    <tr>
        <td>Item 2 name</td><td>Price</td><td>Sorry, no image.</td>
    </tr>
    <tr>
        <td>Item 3 name</td><td>Price</td><td>(image)</td>
    </tr>
</table>

If there is an image file, add an appropriate HTML image tag with the correct src and alt attributes. Use "Image of {item name}." for the alt text.  If the image property is not be present in the JSON for that item, then that table cell should contain italicized text saying “Sorry, no image.”

Remember that you can make HTML tables as follows:
```
<table>
    <tr>
        <th>Heading 1</th><th>Heading 2</th><th>Heading 3</th>
    </tr>
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
```

### Locations Information
The locations.json file contains the JSON to be presented on the locations section of the page. This includes, staff, hours and weekly specials. Use the data from that object to build the HTML as described below.

The Locations section will consist of a heading for each location followed by a list of the weekly hours and information on its staff members.  This data should be added to the "locations" section.  Before adding the headings for each location, remove the default text.

The HTML for each location should be created as follows:
<pre>
HTML5 Article with class="location"
   H3 Heading for Location Name
   H4 Weekly Hours
   Unordered List of hours data with list item for each day/time

   H4 Staff Members
   Div with class="staff row" (One div for each staff member at that location)
      Div with class="col-sm-8"
         H5 Staff Member Name
         Paragraph - Staff Member Text
      Div with class="col-sm-4"
         Staff Member Image with class="img-responsive" (for alt text, use "Picture of {staff member name}")
</pre>


## Write good JavaScript code!

- Use functions to break down the functionality into small tasks
- Practice good coding standards with clear variable and function names
- Use ES6 `let` and `const` instead of `var`
- Use ES6 template literals instead of string concatenation
- Make sure your variables are well named.  Avoid abbreviations, and use camelCase to make multi-word names readable.
- If you store jQuery objects in a variable, start the variable name with $ to indicate it is a jQuery object.


## Final Testing
When you are done, push your files to GitHub, then make sure that your page displays and runs correctly on the GitHub website.  

The site should look something like the following:

{% include img-medium.html url="/assets/images/jquery/moonflowers-jq-menu.png"
            alt="Image of completed page showing menu section." %}
{% include img-medium.html url="/assets/images/jquery/moonflowers-jq-locations.png"  
            alt="Image of completed page showing locations section." %}

Don't forget the Pull Request.  Put a screenshot of the open request in the assignment dropbox.
