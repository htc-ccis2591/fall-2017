---
title: Moonflower's Coffee Part 1
summary: "In this exercise we will create a web page from embedded JSON data. "
---

# {{ page.title }}
{{ page.summary }}


## Accept the assignment
Click the link below, then on the web page, click the green button to accept the assignment.

[Assignment: js-moonflowers]( https://classroom.github.com/a/NagdYc2F )

Note that once you accept this assignment, you will continue working with the same repository on GitHub for later parts of the assignment and will not need to accept the assignment again.

### Locations Information
The JS file has JSON for the locations information to be presented on the page. This includes, staff, hours and weekly specials. You will need to use the data from that object to build the HTML as described below.

The Locations section will consist of a heading for each location followed by a list of the weekly hours and information on its staff members.  This data should be added to the “locations” section.  Before adding the headings for each location, remove the default text.

The HTML for each location should be created as follows:

HTML5 Article with class="location"
   H3 Heading for Location Name
   H4 Weekly Hours
   List of hours data

   H4 Staff Members
   Div with class="staff row" (One div for each staff member at that location)
      Div with class="col-sm-8"
         H5 Staff Member Name
         Paragraph - Staff Member Text
      Div with class="col-sm-4"

Staff Member Image with class="img-responsive", use "Picture of {staff member name}" as the alt text.


## Write good JavaScript code!

- Use functions to break down the functionality into small tasks
- Practice good coding standards with clear variable and function names, use $ for variables that will hold jQuery objects, use ES6 `let` and `const` instead of `var`
- Make sure your variables are well named.  Avoid abbreviations and use camelCase to make multi-word names readable.

## Final Testing
When you are done, push your files to GitHub, then make sure that your page displays and runs correctly on the GitHub website.  

Don't forget the Pull Request.  Put a screenshot of the open request in the assignment dropbox.
