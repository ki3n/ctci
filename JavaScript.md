JavaScript Questions:

How do you determine the context of the keyword this in JavaScript? How can you change the context of &this?
this in Javascript always refers to the 'owner' of the function that is being executed.
If no explicit owner is defined, then the top most owner, the window object, is referenced.
So if I did
function someKindOfFunction() {
   this.style = 'foo';
}
element.onclick = someKindOfFunction;
this would refer to the element object. But be careful, a lot of people make this mistake
<element onclick="someKindOfFunction()">
In the latter case, you merely reference the function, not hand it over to the element. Therefor, this will refer to the window object.

What is “Closure” in javascript?
Closures are frequently used in JavaScript for object data privacy, in event handlers and callback functions, and in partial applications, currying, and other functional programming patterns.
A closure is the combination of a function bundled together (enclosed) with references to its surrounding state (the lexical environment). In other words, a closure gives you access to an outer function’s scope from an inner function. In JavaScript, closures are created every time a function is created, at function creation time.

What is a “Callback” function in JavaScript?
A callback function, also known as a higher-order function, is a function that is passed to another function (let’s call this other function “otherFunction”) as a parameter, and the callback function is called (or executed) inside the otherFunction. A callback function is essentially a pattern (an established solution to a common problem), and therefore, the use of a callback function is also known as a callback pattern.

What is the difference between == (double equal sign) and === (triple equal sign)?
The identity (===) operator behaves identically to the equality (==) operator except no type conversion is done, and the types must be the same to be considered equal.