SOURCE: https://github.com/rtoal/ple/blob/master/docs/reinforcement/js.md
@rtoal rtoal Even more JS reinforcement questions

JavaScript Reinforcement Practice
Here are a set of problems designed to help you reinforce and retain some useful JavaScript knowledge. If you are an Anki fan, consider adding some of these questions into a deck. 😀

Who created JavaScript and in what year?

What was JavaScript originally called?

Why was JavaScript created?

How do you write a line of text to the console?

How do you change the text of an element in a web browser document?

How do you access the third command line argument of a script, run on the command line, with node.js?

Name the 7 data types of JavaScript (as of ES2019). Name the 8th that is coming soon.

Does JavaScript have separate types for integers and floating point values? If not, how can you tell whether a number is an integer or not?

What are safe integers in JavaScript?

If x has the value NaN, what is the value of the expression x === NaN? Why? What is the correct way to determine if an expression has the value NaN?

How can you tell whether string s is a substring of string t?

What two things can you do with backtick-delimited strings you can’t do with strings delimited with apostrophes or quotation marks?

Why does "🤣".length have the value 2?

Give an example that shows the == operator is not transitive.

Why is 2 && 3 equal to 3, but 2 & 3 equal to 2?

Name all the falsy values in JavaScript.

How do you determine the type of an expression at runtime?

When should you use let and when should you use const?

What bad thing will happen if you forget to use let, const, or var when declaring an identifier?

What is the object literal { x, y } a shorthand for?

What is the difference between p.x and p[x]?

If x === 'y' then what is { x: 3, [x]: 5 } ?

Why is [1,12] < [1,3] true but [1,42] < [1,3] false?

How do you write an object to the console (beautifully formatted)?

Describe how a prototype-based language (like JavaScript) differs from a class-based language (like Java), in terms of thinking about collections of objects that share the same structure and behavior.

Properties defined directly within an object are called **\*\***\_\_\_\_**\*\*** properties. Properties of an object accessible on the object’s prototype chain are called **\*\***\_\_\_\_**\*\*** properties.

What do we mean when we say arrays are objects in JavaScript?

Describe how splice works.

What is the spread operator? Give an example of its use.

You might often see the expression a.slice(), for some array a. What does this expression do, exactly?

How does one best create an array of size 100 in which every element is 0? (Do not write a loop.)

Write an equivalent expression to a.concat(b), where a and b are arrays, using spreads.

a.push() mutates a. How do you do a non-mutating “push“?

What does unshift do? Does it mutate or not? What does it return?

What is the difference between value types and reference types?

Why do you think the JavaScript designer decided that objects should be reference types?

Since strings can be very large, you might think strings would be reference types in JavaScript. After all, they are reference types in Java. But in JavaScript, they are considered primitive (value) types. This might lead you to believe JavaScript is necessarily slow because strings are always copied on assignment. However, this is not the case! Why?

Write an IIFE that applies the (anonymous, arrow) function that squares its argument to the value 100.

In the function definition function f(x, y) { return [x, y]; }, what do we call x and y?

In the function call f(y, z), what do we call y and z?

A function is called higher-order if it does at least one of two things. What two things?

What do the array methods map, filter, every, some, find, and findIndex do?

Write the function function f(x = 3) { return x \* y } (where y is some global variable) without using a default parameter.

What is a rest parameter? Give an example.

Can a function definition have multiple rest parameters? Why or why not?

One could argue that all non-default parameters are really default parameters. Why?

In many languages, assignment has the form IDENTIFIER = EXPRESSION. In JavaScript, the left hand side is not just an identifier. What exactly is the left hand side called?

The old-fashioned to write a function that takes in an array and returns the sum of its first and third elements is: function f(a) {return a[0] + a[2];} Rewrite this in a modern fashion, where the function parameter is a pattern.

Write a function that takes in an object and returns the product of its x and y properties. If no argument is passed, return 1. Write the function using a pattern for its parameter. Supply defaults so the function body is simply return x \* y;.

Show how to declare the function that is called like this: push({onTheStack: s, theValue: v})? Use an object pattern in the parameter list.

What are global scope, function scope, and block scope?

How do let-bound and var-bound function-scope variables differ? (Make sure the phrase “temporal dead zone” appears in your answer.)

Write a function that takes in a number and returns a function that adds that number to its argument. Is the function you wrote higher-order? Why or why not? Does that function illustrate a closure? Why or why not? Does that function illustrate currying? Why or why not?

What is currying good for, anyway?

Is JavaScript statically-scoped or dynamically scoped?

Do JavaScript functions exhibit shallow binding or deep binding?

Given function\* f() {yield 1; yield 2; yield 3;}, what is wrong with writing for (let i of f) {console.log(i)}?

Why must (pretty much all reasonable) methods be non-arrow functions?

Why should callbacks generally be arrow functions?

What does the expression this refer to inside of a function called with the new operator?

Is this early-bound or late-bound?

For function f and object x, the expressions f.call(x, 1, 2) and f.apply(x, [1, 2]) produce the same result. Write the equivalent expression using bind.

JavaScript doesn’t have classes, but it does have the word class. But the keyword class does declare a function. How is this “function” defined? Give a short example.

What happens under the hood when you write class A extends B? In particular what does A.prototype look like in this case?

Why doesn’t Crockford like using this?

What is the primary disadvantage of the Crockford-classless style of avoiding this and prototypes?

How do you make a JavaScript object without a prototype?

When would you see a TypeError thrown? A RangeError? A SyntaxError? A ReferenceError?

What is callback hell?

What is an advantage of promises over callbacks?

What exactly is a promise?

What does the function async function five() { return 5; } actually return?

Given let f = async x => 1 and let g = async => 2 what do the expressions f() and g() return? Why? Why is the definition of g even acceptable?

What are the most common names given to the parameters of the Promise constructor? What are they for?

What is the difference between p.then(f, g) and p.then(f).catch(g) for a promise p?

Why do most API invocations, or operating system calls (like reading and writing files) take in callbacks or return promises?

Give the expression, in client-side JavaScript using fetch, that hits the (hypothetical) endpoint https://api.example.com/fortunes?limit=5 and, from its JSON response, places the first result in the DOM into the element with id fortune.

Does await actually wait (block) for anything? It not, what exactly does it do?

How does one “wait” for a whole bunch of async functions to all ”finish”?

What is the difference between an accessor property and a data property? (Your answer should include all of the attributes for each kind of property.)

How do you make a property read-only?

What is the difference between sealing and freezing an object?

How do you get the prototype of an object?

How do you set an object’s prototype after the object has already been created?

What is the difference between Object.keys and Object.getOwnPropertyNames?

How does Object.entries work?
