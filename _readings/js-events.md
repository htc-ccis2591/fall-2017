---
title: JavaScript Events
summary: "This reading provides an introduction to events and event handling in JavaScript."
---

# {{ page.title }}
{{ page.summary }}.

## Working with Events
[Chapter 14 of Eloquent JavaScript](http://eloquentjavascript.net/14_event.html) introduces events and how to work with them using JavaScript. We will go deeper into events, and the material in this chapter, in the next module. For now, you really just need to know how to add a click handler as shown below.

Events are the key to interactivity on the web and through computer science and programming. While web events are generally triggered by a person interacting with our page, you might also imagine that a new row being added to a database might trigger an event that would cause some database code to run.  

### Event Handlers
In JavaScript we work with events by using __event handler__ functions. An event handler is just a function that is linked to an event. In JavaScript this is done by using the object's `addEventListener` method. They can also be removed by using the `removeEventListener` method.

These event handlers are setup to be triggered when a particular __event__ occurs. In JavaScript, events are also objects, and we can determine the type of event by checking the event object's `type` property.  

The most common type of event we will be working with is the click event.

{% highlight JavaScript %}
let button = document.getElementById("myButton");
  button.addEventListener("click", function() {
    console.log("Button clicked.");
  });
{% endhighlight %}
