---
title: More on Events
summary: "This reading provides a deeper dive into events and event handling in JavaScript."
---

# {{ page.title }}
{{ page.summary }}.

## Working with Events
[Chapter 14 of Eloquent JavaScript](http://eloquentjavascript.net/14_event.html) examines events, the different event types, and how to work with them using JavaScript.

Events are the key to interactivity on the web and through computer science and programming. While web events are generally triggered by a person interacting with our page, you might also imagine that a new row being added to a database might trigger an event that would cause some database code to run.  

### Event Object
In JavaScript __event handler__ functions get passed an argument (or parameter), the __event object__. This object contains details about the event itself. For example the type of event is always identified by the event object's `type` property, which holds a string such as "click" or "keydown".

Different types of events will also have different properties set to give additional information. For example with the "mousedown" (triggered by a mouse-click) event you can tell which button on the mouse was pressed by examining the `which` property on the event object.  With a "keydown" or "keyup" event, checking the `keycode` property allows you to know which key was pressed or released, while the `charCode` property gives the Unicode character code value of that key.

### Event Propagation
The DOM structure itself also affects JavaScript events.  When we register an event handler on an element that has children, the parent will receive some event notifications on events that occur on children and deeper descendant elements.  This means if both the parent and the child have an event handler registered, by default both will be triggered.  The most specific one (the child's handler) will run first and then the event will *propagate* outward until it reaches the parent. We can use the `target` property found on most events to identify the source node or element where the event originated.

### Default Behaviors
Many events are associated with default actions. For example, clicking a link triggers navigation to the link's target. We can prevent this default behavior from occurring by registering an event handler that calls the `preventDefault()` method on the event object.

Since this changes behavior that someone visiting your web page might be expect, you should be cautious and considerate about when you do this. Imagine visiting a web page where nothing happened when you clicked any buttons or links.  You'd be frustrated, right?  Remember, with great power comes great responsibility.

However it is rather common to `preventDefault()` in the click handlers for form submission buttons when JavaScript is used to do form validation.  We'll look at this more
