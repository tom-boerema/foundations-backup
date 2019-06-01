# JavaScript: the DOM and events

## Content 
This article helps students to 

1. Learn the basics of the HTML5 Document Object Model.
2. Learn how to get hold of elements on the page by element name, class name, or ID.
3. Learn a couple of simple methods for adding new elements or text nodes, for removing elements, and for replacing the content of an element.
4. Discover how to add a simple event handler to an HTML form to capture the submission of the form, then prevent the actual submission of that form.
5. Get a feel for manipulating HTML elements and capturing events.

## The Document Object Model (DOM)

When we are using JavaScript to manipulate HTML elements on a page by adding, moving, removing them or changing their style properties, we need a way to get hold of specific elements so we can do things with them.

Browsers provide a `document` JavaScript object with a large number of properties and methods to allow us to do exactly this. Actually, it's a "tree" of objects, with JS objects representing the head, body, title, paragraphs, etc. all connected up like a big tree. Like a family tree except each object, method, or property has only one parent.

At the head of this tree-the great-great-great-grandparent of all the rest, so to speak-the *original* ancestor- is the `window` object, and inside the `window` object is the `document` object, which represents our page.

You've seen this already when you open the Chrome Developer Tools console and type `window.` (don't forget the period after it) and wait a second, and the Chrome pops up a long list of properties, methods, and object that are the "children" of the `window` object.

For now, we're only going to worry about the `document` child. You can leave off the `window` part and just try `document.`:

<figure>
  <img src="/resources/images/js-dom-document-dropdown.png" alt="Document dropdown in Dev Tools"><br>
  <figcaption>
    <p><strong>Figure 1:</strong> What's inside the <code>document</code> object.</p>
  </figcaption>
</figure>

If we limit ourselves to just the page, we can imagine the `document` object like this (but much more complicated, right?):

<figure>
  <img src="/resources/images/js-dom-html-dom.jpg" alt="HTML5 DOM tree"><br>
  <figcaption>
    <p><strong>Figure 2:</strong> A simplified view of the <code>document</code> object.</p>
  </figcaption>
</figure>

OK, if you promise not to faint, we'll show you a bit more of the DOM. Here's a very simplified version of the `window` object:

<figure>
  <img src="/resources/images/js-dom-full-dom.png" alt="Full DOM tree"><br>
  <figcaption>
    <p><strong>Figure 3:</strong> A simplified view of the <code>window</code> object.</p>
  </figcaption>
</figure>

See what we mean? It gets complicated quickly!

The good news is that you only need to worry about a small part of this. Please don't try to learn or memorize the whole thing! That would be like memorizing every feature in Microsoft Word. It might get you into the Guinness Book of World Records-with bragging rights-but it will only delay your progress of becoming a web developer. Pick your battles!

So let's use only what we really need, and we'll learn more as we need it. That way we use what we learn immediately. Which means that we get the job done quickly (your boss will like that), and we remember what we learned because we practiced it immediately.

That said, if you just can't help yourself, there's a [W3Schools HTML DOM tutorial](http://www.w3schools.com/js/js_htmldom.asp) you can check out. Be aware, however, that the HTML DOM is not the only document object model out there, so make sure it's the HTML DOM you're working on.

### Getting our hands on HTML elements

So how can we get hold of an HTML element on the page so that we can manipulate it in our code.

Well, the three most common ways are by tag name (element name, such as `p` or `div`), by class name, or by ID. The first two return an *array* of elements (technically, a [nodelist](https://developer.mozilla.org/en/docs/Web/API/NodeList)) because there can be more than one `p` element or more than one element with `class="form-group"`. But when we find an element by its ID, we get back a single element (node) because ID attribute values have to be unique on a page.

One good way then to make things easy to grab is by giving them unique IDs. We don't want to use those IDs for CSS. For CSS, because of specificity, we should generally use classes. But with scripts, it's just the reverse. Finding an element by ID is much faster than finding a list of elements by tag name or class name and then having to loop through them to find the one we really want.

Of course, if you want to manipulate multiple elements on a page, then giving them all the same class and finding them by that class is the best way. So think about what it is that you're trying to do and you'll quickly see which approach is best for that specific circumstance.

Let's start with a basic page that looks like this:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Test</title>
  </head>
  <body>
    <div id="app">
      <header>
        <h1>My test page</h1>
      </header>
      <main>
        <p>
          That said, if you just can't help yourself, there's a
          <a id="w3schools-tutorial" href="http://www.w3schools.com/js/js_htmldom.asp">
            W3Schools HTML DOM tutorial
          </a>
          you can check out.
        </p>
        <p>
          Be aware, however, that the
          <span class="dom">HTML DOM</span>
          is not the only document object model out there, so make sure it's the
          <span class="dom">HTML DOM</span>
          that you're
          <a href="http://bit.ly/1MEVufu">looking for</a>.
        </p>
      </main>
  </body>
</html>
```

OK, so let's say we want to get hold of that `<h1>` element. How can we do it?

Well, we can use the `document.querySelector()` method. We can use the element name to do so, so we'll grab it with `document.querySelector('h1')`. Try it and it works!

What if we want to grab our paragraphs. Let's try `document.querySelector('p')`. And it works, too, but wait a minute! I only see one paragraph here. Where's the other one?

Well the `querySelector` method returns only the *first* matching element. If I want to return and array of all matching elements, then I have to use the `querySelectorAll` method.

Check it out:

<figure>
  <img src="/resources/images/js-dom-query-selector-all.png" alt="querySelectorAll"><br>
  <figcaption>
    <p><strong>Figure 4:</strong> Using <code>querySelector</code> and <code>querySelectorAll</code>.</p>
  </figcaption>
</figure>

We can also find elements by class name and by ID using `.` and `#`, respectively, or by combining these methods:

<figure>
  <img src="/resources/images/js-dom-query-by-id-and-class.png" alt="Querying by ID and class"><br>
  <figcaption>
    <p><strong>Figure 5:</strong> You can query by element name, class name, ID, or combination.</p>
  </figcaption>
</figure>

### OK, now what do we do with the elements we've got?

Well, how about if we replace the text of an element? Suppose we wanted to replace the "HTML DOM" in the two `<span>` elements with "HTML5 Document Object Model". We can use the `innerHTML` attribute of the element to both get and set the inner HTML (in this case, just text):

<figure>
  <img src="/resources/images/js-dom-innerhtml-get-set.png" alt="Getting and setting innerHTML"><br>
  <figcaption>
    <p><strong>Figure 6:</strong> You can get or set the `innerHTML` of an element.</p>
  </figcaption>
</figure>

But what happened here? We only set the first one? We want to do both. Well, let's reload the page and start over. Maybe if we use `querySelectorAll`?

<figure>
  <img src="/resources/images/js-dom-nodelist-not-array.png" alt="A nodelist is not an array"><br>
  <figcaption>
    <p><strong>Figure 7:</strong> Grave disappointments in DOM-land.</p>
  </figcaption>
</figure>

Huh? What's going on here? We used `forEach` with arrays before, right? Why isn't it working here?

Well, it turns out that `.querySelectorAll` returns a special data type, the "NodeList" that *looks* like an `Array`, but isn't. So the methods we'd expect to find on an array aren't available. We haven't got our friend `ramda` here either, so we're going to have to revert to the old fashioned methods.

One method that works is the old JavaScript `for` loop. You might not have seen this yet. If not, take a moment to look at this [W3Schools tutorial](http://www.w3schools.com/js/js_loop_for.asp) to see how it works.

So we could try this:

```js
var spans = document.querySelectorAll('.dom')
for (var i = 0; i < spans.length; i++) {
  spans[i].innerHTML = 'HTML5 Document Object Model'
}
```

That works:

<figure>
  <img src="/resources/images/js-dom-for-loop.png" alt="Using a for loop"><br>
  <figcaption>
    <p><strong>Figure 8:</strong> Using a for loop to loop through nodes in a nodelist.</p>
  </figcaption>
</figure>

There are also some tricks to convert the nodelist to an array. This one grabs the Array object (the one we use to make arrays), takes its `slice` method (which creates arrays from slices of other arrays), and calls it, passing in the nodelist. Effectively, this takes the whole nodelist and dumps it into an array. If this seems mystifying to you, don't worry. It's a neat trick you can put in your toolkit and worry about figuring out how it works later. We have to save some mystery for later, right?

```js
var spans = Array.prototype.slice.call(document.querySelectorAll('.dom'))
spans.forEach(function (span) { span.innerHTML = 'HTML5 Document Object Model' })
```

And it works!

<figure>
  <img src="/resources/images/js-dom-array-slice-nodelist.png" alt="Converting nodelist to an array"><br>
  <figcaption>
    <p><strong>Figure 9:</strong> Convert to array and we can use `forEach` to loop.</p>
  </figcaption>
</figure>

We can also set attributes using the [`setAttribute`](http://www.w3schools.com/jsref/met_element_setattribute.asp) method on an element. This includes the `style` attribute, though usually we'll want to set class names instead:

<figure>
  <img src="/resources/images/js-dom-set-style-attribute.png" alt="Setting the style attribute"><br>
  <figcaption>
    <p><strong>Figure 10:</strong> We can use the style attribute to style elements with JS.</p>
  </figcaption>
</figure>

Time to do Deliverable #1! Have some fun. Refer back to the code above as necessary to see what to do, or check out the various tutorials on W3Schools mentioned. You can also find plenty of material on MDN, of course.

## Events
We want our web pages and applications to be interactive, right? To accomplish this goal, we need to have some way of recognizing when a user interacts with our page.

The simplest form of interaction is to request a new page. Users can do this by clicking on links (or focus on them and pressing the Enter key) or by entering a URL in the browser's address bar and hitting the Enter key. But that's a pretty coarsely-grained mode of interaction! We can only do whole page loads on every click?

Obviously, we need to be able to capture other clicks, keystrokes, mouse moves, and more. What about when the user resizes the window? That might be good to know. Or when she drags and drops an item. Or he right clicks on an item.

Each of these occurrences is an "event". We can have a click event, or a hover event (when the user "hovers" the mouse pointer over an item), or a keypress event, or even a form submission event or page reload event.

The way we handle events is by attaching an "event handler" to the object we want to keep track of, and providing that event handler with a "callback" function that we want it to use when the event occurs.

So, essentially, we can say to the browser, "When the user clicks on this button, we want you to call this function and give it an 'event object' with lots of information about the event that occurred." Luckily, we don't have to be that verbose about it.

Let's add a button to our page. We'll give it an ID so it's easy to grab hold of it in the DOM:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Test</title>
  </head>
  <body>
    <div id="app">
      <header>
        <h1>My event test page</h1>
      </header>
      <main>
        <button id="way-cool-button">Click me!</button>
      </main>
  </body>
</html>
```

Now let's add an event handler to the button and we'll pass it a function to call when the button is clicked. In this instance, we'll just ask it to log the event object that gets passed to the callback to the console, so we can do it all in one line:

```js
document.querySelector('#way-cool-button').onclick = function (event) {
  console.log(event)
}
```

And it works! Here I clicked three times. You can click on the little triangle to see what's in an event object. Wow! There's a lot of stuff in there. Some of that might even be useful.

<figure>
  <img src="/resources/images/js-dom-click-me.png" alt="Onclick event handler"><br>
  <figcaption>
    <p><strong>Figure 11:</strong> Handling the button `onclick` event.</p>
  </figcaption>
</figure>

This method works, but it has the limitation of allowing only one event to be added and only one callback (for the button, that is). There is a more up-to-date if slightly more complex way:

```js
document.querySelector('#way-cool-button').addEventListener(
  'click',
  function (event) { console.log(event) },
  false
)
```

(Don't worry about what the `false` does. It's complicated. We'll figure it out when we need it.)

It works:

<figure>
  <img src="/resources/images/js-dom-add-event-listener.png" alt="Using addEventListener"><br>
  <figcaption>
    <p><strong>Figure 12:</strong> The <code>addEventListener</code> method is the better way.</p>
  </figcaption>
</figure>

W3Schools has a long list of [DOM events](http://www.w3schools.com/jsref/dom_obj_event.asp). Like kids in a candy store! Let's play.

Once you've played around a bit yourself, maybe we want to try something a bit more difficult. What if we wanted to capture keystrokes in a text field and output them immediately to a `<div>` below the text field. You've probably seen this before, right?

First, let's modify our page:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Test</title>
  </head>
  <body>
    <div id="app">
      <header>
        <h1>My keystroke test page</h1>
      </header>
      <main>
        <p>
          <input id="keystroker">
        </p>
        <p id="outputter"></p>
      </main>
  </body>
</html>
```

Now we can grab our input and attach an event handler to it to capture keystrokes. We can capture the stroke on the way down (`keydown`), the way up (`keyup`), or both (`keypress`). We want to check the innerHTML *after* it has been updated with the new value, so we'll use `keyup`.

With each `keyup` event, we'll update the paragraph below the input so that its content is the value of the input:

```js
var input = document.querySelector('#keystroker')
var output = document.querySelector('#outputter')
var updater = function (e) { output.innerHTML = input.value }

input.addEventListener('keyup', updater, false)
```

Not too difficult, right? We grab the `<input>` element as `input`. We grab the `<p>` element as `output`. Then we create an `updater` function that ignores the input `e` and just pastes the value of the `<input>` element as the innerHTML of the `<p>` element.

Then all that's left to do is to add an event listener to listen for `keyup` events on the input and run the `updater` function to update the output:

<figure>
  <img src="/resources/images/js-dom-keyup.png" alt="Using keyup to update the page"><br>
  <figcaption>
    <p><strong>Figure 13:</strong> The <code>keyup</code> event lets us capture keystrokes.</p>
  </figcaption>
</figure>

### Form submission

OK, one last thing. What if we want to capture a form submission and handle it on the front end *instead* of submitting it to the server?

Let's add a simple form to our page:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Test</title>
  </head>
  <body>
    <div id="app">
      <header>
        <h1>My form submission test page</h1>
      </header>
      <main>
        <form id="catch-it">
          <input id="some-text">
          <input type="submit">
        </form>
        <p id="outputter"></p>
      </main>
  </body>
</html>
```

And here's our code. It's pretty self-explanatory. But what is that `preventDefault()` bit?

Well, the normal default action when we submit a form is to do a POST request to the server and reload the page with the response. But we want to *prevent* page reload, so we want to prevent the default action. Conveniently, the `e` event object comes with a method called `preventDefault()` that does precisely that. It's like we planned it!

```js
var form = document.querySelector('#catch-me')
var input = document.querySelector('#some-text')
var output = document.querySelector('#outputter')
var updater = function (e) {
  e.preventDefault()
  output.innerHTML = 'Submitting form with "' + input.value + '"'
}

form.addEventListener('submit', updater, false)
```

Does it work? You bet:

<figure>
  <img src="/resources/images/js-dom-catching-form-submit.png" alt="Catching form submission"><br>
  <figcaption>
    <p><strong>Figure 13:</strong> Using the `submit` event to capture form submission.</p>
  </figcaption>
</figure>

OK, that's enough for this section. You've learned some very powerful tools. Post questions or blocks on Slack so your cohort and online community can help you.


## Glossary

<dl>
  <dt>callback</dt>
  <dd>
    In computer programming, a callback is a piece of executable code that is passed as an argument to other code, which is expected to call back (execute) the argument at some convenient time. The invocation may be immediate as in a synchronous callback, or it might happen at later time as in an asynchronous callback.
  </dd>
  <dt>document object model</dt>
  <dd>
    The Document Object Model (DOM) is a cross-platform and language-independent convention for representing and interacting with objects in HTML, XHTML, and XML documents.[1] The nodes of every document are organized in a tree structure, called the DOM tree. Objects in the DOM tree may be addressed and manipulated by using methods on the objects. The public interface of a DOM is specified in its application programming interface (API).
  </dd>
  <dd>
    The history of the Document Object Model is intertwined with the history of the "browser wars" of the late 1990s between Netscape Navigator and Microsoft Internet Explorer, as well as with that of JavaScript and JScript, the first scripting languages to be widely implemented in the layout engines of web browsers.
  </dd>
  <dt>event</dt>
  <dd>
    An action or occurrence detected by a program. Events can be user actions, such as clicking a mouse button or pressing a key, or system occurrences, such as running out of memory. Most modern applications, particularly those that run in Macintosh and Windows environments, are said to be event-driven, because they are designed to respond to events. (Webopedia)
  </dd>
  <dt>event handler</dt>
  <dd>
    A function or method containing program statements that are executed in response to an event. An event handler typically is a software routine that processes actions such as keystrokes and mouse movements. With Web sites, event handlers make Web content dynamic. JavaScript is a common method of scripting event handlers for Web content. (Webopedia)
  </dd>
</dl>

