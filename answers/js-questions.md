# JS Questions

#### Explain event delegation

When an event is fired from an element, the event will be bubbled up to its
parent nodes. However, the original element where the event occurs, called
'target', stays the same in the event object. Using the `target` property, we
can always keep tracking which element actually causes an event captured by
its parent, and it can help use reduce the number of event handlers as we
sometimes don't need to add event listeners for every element.

#### Explain how `this` works in JavaScript

*The answere is from https://javascriptissexy.com/understand-javascripts-this-with-clarity-and-master-it/*<br>
'this' is used inside a function (let’s say function A) and it contains the value of the object that invokes function A. We need this to access methods and properties of the object that invokes function A, especially since we don’t always know the name of the invoking object, and sometimes there is no name to use to refer to the invoking object. Indeed, this is really just a shortcut reference for the “antecedent object”—the invoking object.

#### Explain how prototypal inheritance works

*The answere is from https://goo.gl/3L94qS* <br>
The core idea of Prototypal Inheritance is that an object can point to another object and inherit all its properties. The main purpose is to allow multiple instances of an object to share common properties, hence, the Singleton Pattern.

#### What do you think of AMD vs CommonJS?

*The answere is from https://auth0.com/blog/javascript-module-systems-showdown/* <br>
CommonJS is a project that aims to define a series of specifications to help in the development of server-side JavaScript applications. One of the areas the CommonJS team attempts to address are modules. Node.js developers originally intended to follow the CommonJS specification but later decided against it. <br>
AMD was born out of a group of developers that were displeased with the direction adopted by CommonJS. In fact, AMD was split from CommonJS early in its development. The main difference between AMD and CommonJS lies in its support for asynchronous module loading. <br>
"The main difference between AMD and CommonJS lies in its support for asynchronous module loading."<br>


#### Explain why the following doesn't work as an IIFE: `function foo(){ }();`.

*Not answered yet*

###### What needs to be changed to properly make it an IIFE?

```js
(function foo() { })(); // or
(function foo() { }());
```

#### What's the difference between a variable that is: `null`, `undefined` or undeclared?
###### How would you go about checking for any of these states?

*Not answered yet*

#### What is a closure, and how/why would you use one?

*Not answered yet*

#### What's a typical use case for anonymous functions?

*Not answered yet*

#### How do you organize your code? (module pattern, classical inheritance?)

*Not answered yet*

#### What's the difference between host objects and native objects?

- Host objects: what an environment(browser, Node.js, etc) provides
- Native objects: what JavaScript provides


#### Difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`?

*The answer is from https://www.quora.com/In-Javascript-what-is-the-difference-between-function-Person-var-person-Person-var-person-new-Person*

#### What's the difference between `.call` and `.apply`?

*The answer is from https://stackoverflow.com/questions/1986896/what-is-the-difference-between-call-and-apply*

#### Explain `Function.prototype.bind`.

*The answer is from https://stackoverflow.com/questions/7282158/function-prototype-bind*

#### When would you use `document.write()`?

When someone gives me one million dollar for doing it.

#### What's the difference between feature detection, feature inference, and using the UA string?

- Feature detection: directly check if a feature is implemented

```js
if (Promise) {
  let a = Promise.resolve('hello');
}
```

- Feature inference: infer if a feature is implemented by checking other properties

```js
if (MozSmsMessage) {
  // guess it must be Firefox...
}
```

- UA string: UA stands for UserAgent, which a browser natively exposes to
  scripts and HTTP header

```js
console.log(navigator.userAgent); // "Mozilla/5.0 (Macintosh; ..."
```

#### Explain AJAX in as much detail as possible.

*Not answered yet*

#### Explain how JSONP works (and how it's not really AJAX).

A JSONP response contains a callback function usually written in JavaScript,
and when the response is flushed, the callback will be launched. It's more like
script tag injection, rather than AJAX.

#### Have you ever used JavaScript templating?

Yes.

###### If so, what libraries have you used?

Handlebars, Mustache, etc.

#### Explain "hoisting".

*Not answered yet*

#### Describe event bubbling.

It's when an event is bubbled into container elements, in the higher level of a
DOM tree.

#### What's the difference between an "attribute" and a "property"?

- Attribute: specified in HTML, always in the form of string
- Property: specified in DOM object, can have any type of JavaScript

#### Why is extending built-in JavaScript objects not a good idea?

*Not answered yet*

#### Difference between document load event and document ready event?

- document ready: when a HTML document is loaded and rendered
- document load: when a HTML document and assets in the document are all loaded
  and rendered

#### What is the difference between `==` and `===`?

*The answer is from https://www.codecademy.com/en/forum_questions/558ea4f5e39efed371000508*

#### Explain the same-origin policy with regards to JavaScript.

Same-origin means having same host, port and protocol(HTTP or HTTPS). If a
script in the different origin should be accessed, we can consider using CORS.

#### Make this work:
```javascript
duplicate([1,2,3,4,5]); // [1,2,3,4,5,1,2,3,4,5]
```

```js
let duplicate = (arr) => arr.concat(arr);
```

#### Why is it called a Ternary expression, what does the word "Ternary" indicate?

*Not answered yet*

#### What is `"use strict";`? what are the advantages and disadvantages to using it?

Advantages

- Cannot assign a value to an undefined global variable
- Fire TypeError for not-allowed assignments
- `this` in a normal function refers to `undefined`, instead of `global`

In short, it secures JavaScript.

Disadvantage

- When using global strict mode and concatenating the script with other scripts
  not using strict mode, the other scripts can be broken.

#### Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`

*Not answered yet*

#### Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it?

*Not answered yet*

#### Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those?

*Not answered yet*

#### Explain what a single page app is and how to make one SEO-friendly.

*Not answered yet*

#### What is the extent of your experience with Promises and/or their polyfills?

*Not answered yet*

#### What are the pros and cons of using Promises instead of callbacks?

*Not answered yet*

#### What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript?

*Not answered yet*

#### What tools and techniques do you use debugging JavaScript code?

*The answer is from https://developers.google.com/web/tools/chrome-devtools/javascript/*

#### What language constructions do you use for iterating over object properties and array items?

*Not answered yet*

#### Explain the difference between mutable and immutable objects.
###### What is an example of an immutable object in JavaScript?
###### What are the pros and cons of immutability?
###### How can you achieve immutability in your own code?

*Not answered yet*

#### Explain the difference between synchronous and asynchronous functions.

*The answer is from https://goo.gl/9RTnjx*<br>
Synchronous vs. Asynchronous Execution
The difference between synchronous and asynchronous execution may seem a bit confusing at first. Program execution in most high-level languages is usually very straightforward. Your program starts at the first line of source code and each line of code executed sequentially thereafter. Easy enough.
Synchronous program execution is somewhat similar to the above. Your program is executed line by line, one line at a time. Each time a function is called, program execution waits until that function returns before continuing to the next line of code.
This method of execution can have undesirable ramifications. Suppose a function is called to start a time consuming process. What if you want to stop the lengthy process? With synchronous execution, your program is “stuck,” waiting for the process to end, with no way out.
Asynchronous execution avoids this bottleneck. You are essentially saying, “I know this function call is going to take a great deal of time, but my program doesn’t want to wait around while it executes.”
Using asynchronous execution, the TakePicture() function returns immediately and shows the message. Although the two-minute process is not complete, your program can continue to execute. In this manner, your program could set the notCancelledByUser variable to FALSE to cancel the picture. It can also poll or ask the TakePicture() function when the exposure is completed, or if an error occurred during the process.<br>
#### What is event loop?
###### What is the difference between call stack and task queue?

*Not answered yet*

