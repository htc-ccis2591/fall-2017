---
title: JS Fizz Buzz
summary: "Fizz Buzz is based on a children's game used to practice basic math, but is a common programming interview question. "
---

# {{ page.title }}
{{ page.summary }}

## Prerequisites
Make sure that you have completed the following prerequisites before beginning:

- [JavaScript Objects]({{ "/readings/js-objects.html" | prepend:site.baseurl }})  
- [JavaScript Document Object]({{ "/readings/js-dom.html" | prepend:site.baseurl }})
- [JavaScript Events]({{ "/readings/js-events.html" | prepend:site.baseurl }})

Most of the required code is based on basic JS syntax presented in Module 1, but we will use DOM methods to add our results to the web page.

## Game Play
To play the game, children will sit in a circle and count up from 1, but there are rules that cause words to be substituted for numbers. For example we might have a rule that says: if the number is evenly divisible by 3, then change it to Fizz.  As new rules are added, the game becomes more complex and challenging.

## Requirements
We will write code to simulate playing Fizz Buzz by having the computer count from 1 to some max number.  We will set the max to 30 to start, but should be able to easily change it.

There will also be rules to control when numbers are replaced with words.  To begin the rules are:

- If the number is evenly divisible by 3 change it to Fizz
- If the number is evenly divisible by 5 change it to Buzz

When multiple rules apply to a number, all words should be said on the same line.

If no rules apply, we just say the number.

## Getting Started
Before we can get started, we'll need to setup a basic HTML file that calls our JavaScript code.  We want to write our JavaScript in a separate file that we add to the HTML using a `script` element.  

First, create a folder for this web project and open the folder in Brackets.  Then create an index.html file with the following contents:

{% highlight html %}
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Fizz Buzz</title>
  <meta charset="utf-8" />
</head>
<body>
  <h1>Fizz Buzz</h1>
  <p>We will count from 1 to 30, using the following rules:</p>
  <ul>
    <li>If the number evenly divides by 3 replace it with "Fizz"</li>
    <li>If the number evenly divides by 5 replace it with "Buzz"</li>
    <li>If more than one rule applies, output all replacement words on the same line.</li>
  </ul>

  <h2>Let's Do It</h2>
  <p>Enter the number to count up to and then click "Go!"</p>
  <form>
    <label for="max">Max:</label>
    <input id="max" type="number" min="1" max="250">
    <input type="button" id="btn-count" value="Go!">
  </form>

  <div id="output"></div>

  <script src="fizz-buzz.js"></script>
</body>
</html>
{% endhighlight %}

Next create the JavaScript file fizz-buzz.js, which is referenced in the above HTML.  Make sure that both the HTML and JavaScript files are saved in the web project folder.

### First Iteration, Write to Console
To begin our JavaScript code, lets set up a counter and a loop to simulate counting to our max number.  Since we want to be able to easily change the max number, we should make a variable to hold that value.

{% highlight JavaScript %}
const maxCount = 30
{% endhighlight %}

Then we need to setup the loop counter and a loop to do the counting:
{% highlight JavaScript %}
let count = 0
while (count < maxCount) {
  count += 1;

}
{% endhighlight %}

It's easy to forget to change the counter in a while loop, so I try to do that as a first step in the setup.

Next we need to add the code for our rules.  

If a number is divisible by 3, we want to replace it with the word "Fizz".  We know that one number divides evenly by another if the remainder from the division is 0.  We can use the modulus operator to get the remainder from division.

Add the following code inside the while loop:
{% highlight JavaScript %}
if (count % 3 === 0) {
  console.log("Fizz");
} else {
  console.log(count);
}
{% endhighlight %}

Try running the code.  At this point, we should see our code count to 30 replacing any numbers that divide evenly by 3 with "Fizz".

This is a good start, but the if/else logic becomes complicated as additional rules are added.  Plus we need to be able to combine words when multiple rules apply.  The else isn't going to work well for that.

Instead, lets add a variable to hold the value we will say. Let's call it our "message". We can start with that being empty, then we can check each rule in turn using a basic if statement.  If the rule applies, we will add the word to the message. If the message is still empty after checking all the rules, then set the message to the count.

Change the code from above to:
{% highlight JavaScript %}
let message = "";
if (count % 3 === 0) {
  message += "Fizz";
}
if (message == ""){
  message = count;
}
console.log(message);
{% endhighlight %}

Now run the code.  The same thing should happen. However now we have a structure that is easy to extend with additional rules.  

Let's add the rule for "Buzz":
{% highlight JavaScript %}
let message = "";
if (count % 3 === 0) {
  message += "Fizz";
}
if (count % 5 === 0) {
  message += "Buzz";
}
if (message == ""){
  message = count;
}
console.log(message);
{% endhighlight %}

Now when be run the code we should see both rules work.  Numbers that are divisible by 3 such as 3, 6, 9, 12, etc should be replaced with "Fizz".  Numbers that are divisible by 5 such as 5, 10, 20, 25, etc. should be replaced with "Buzz", and numbers that are divisible by both, such as 15 and 30 should be replaced with "FizzBuzz".

We can make the message a little prettier by adding a space at the end of Fizz and Buzz to get "Fizz Buzz ".  The extra whitespaces are trimmed off by web browsers, which is handy.

Now we have working Fizz Buzz code, but we still need to get our max number to count to from the form and then write our output to the web page.

### Second Iteration, Write to Page
Notice in the HTML we added a section for output with a `div` that has an `id`.
{% highlight html %}
<div id="output"></div>
{% endhighlight %}

This makes it easy for us to target this `div` with the DOM `getElementById` method.

At the top of the JavaScript file, insert a line to get and save this element in a variable:

{% highlight JavaScript %}
const outputElement = document.getElementById("output");
{% endhighlight %}

To make our output nicer to read, and get a little more experience writing out HTML elements, let's put the output in a list or a `ul` HTML element.  To do this, we first need to create the `ul` element.
{% highlight JavaScript %}
const listTarget = document.createElement("ul");
{% endhighlight %}

Then we can append it as a child of the `div` or outputElement variable:
{% highlight JavaScript %}
outputElement.appendChild(listTarget);
{% endhighlight %}

Now that we have the list on the HTML page (you can use the Developer Tools Elements view to see this), we can change the `console.log()` to add a new list item to the DOM.

Again we'll start by making a new element. Comment out the `console.log()` and add this code below:
{% highlight JavaScript %}
const item = document.createElement("li");
{% endhighlight %}

HTML list items have text content vs element content, so we need to create a text node to hold our message text:
{% highlight JavaScript %}
const text = document.createTextNode(message);
{% endhighlight %}

Then we need to add the text node as a child of the `li` element:
{% highlight JavaScript %}
item.appendChild(text);
{% endhighlight %}

And finally we can add the `li` element as a child of the `ul` element:
{% highlight JavaScript %}
listTarget.appendChild(item);
{% endhighlight %}

Now when we load the page, we should see the output written to the page instead of the console.

### Third Iteration, Form Input
For out last iteration of this code, we'll use the form input to get the max number to count up to and then start the code when the "Go!" button is clicked.

First let's wrap all of our current code in a function that takes an input parameter for the max number to count up to:
{% highlight JavaScript %}
function fizzBuzzGame(maxCount) {

  // All of the earlier code goes in here

}
{% endhighlight %}

In our earlier code, we set the `maxCount = 30`.  We are now getting the maxCount as the input parameter to our function, so that line can be removed entirely from our previous code that we put in the loop.

Now that we have a function, we need to call it in order for it to run.  Let's set-up a click-handler on the "Go!" button to call the function and pass in the value of 30 that we were using before.  This will let us test the function before we worry about getting the input from the form.

Put this code either before or after the function definition.  It will work either place, so long as it is outside the fizzBuzzGame function we made above:
{% highlight JavaScript %}
const button = document.getElementById("btn-count");
button.addEventListener("click", function () {

  const max = 30;
  fizzBuzzGame(max);
});
{% endhighlight %}

Notice that we got the button using it's id attribute value.  Then we added the click event handler to it.  Inside the event handler function, we are setting the max to 30, then using that variable as the input to the fizzBuzzGame function.

Now when you test your page, no matter what you set the input value to, when you click "Go!" we will play Fizz Buzz counting to 30.

Last step then is to get the actual max value from the form field and use that to call our function.

Change the click handler to get the input control by id and then use it's `value` attribute to set the max:
{% highlight JavaScript %}
button.addEventListener("click", function () {
  const maxInput = document.getElementById("max");
  const max = maxInput.value;
  fizzBuzzGame(max);
});
{% endhighlight %}

Notice however that if we click "Go!" a second time we double the output.  To clean this up, we need to delete what was previously there.

To do this, we need to get our outputElement and then delete it's children.  Let's make another function to remove any elements children.  Let's start by defining the function with one input parameter, the element we want to remove the children from:
{% highlight JavaScript %}
function removeAllChildren(element) {

}
{% endhighlight %}

Then we can get the elements child elements using the `children` property:
{% highlight JavaScript %}
const children = element.children;
{% endhighlight %}

Then set up a for loop to get each child and remove it using the `removeChild()` method:
{% highlight JavaScript %}
for (let i = 0; i < children.length; i++) {
  let current = children[i];
  element.removeChild(current);
}
{% endhighlight %}

Now we can update our eventHandler method to get the output `div` and remove all of it's children before we call the fizzBuzzGame method to write (new) output:
{% highlight JavaScript %}
const outputElement = document.getElementById("output");
removeAllChildren(outputElement);
{% endhighlight %}


## Complete Solution
You can view the entire solution on GitHub: [module2-code](https://github.com/htc-ccis2591/module2-code)

You can also see and interact with the results on the web: [Module 2 Sample Code](https://htc-ccis2591.github.io/module2-code/)


## Tips to Remember
This exercise had two very distinct parts:

1) the programming logic for Fizz-Buzz
2) the DOM coding to write the output to the page

As we worked through the assignment, we handled each part separately. By breaking down the problem into two parts, the larger problem was easier to solve.

We were also able to test our code and output along the way.  It's very difficult to write all the code, then try to fix all the errors that might occur. It's much easier to write small amounts of code and test it, then once that is working write a little bit more.
