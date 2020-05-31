SOURCE: https://github.com/rtoal/ple/blob/master/docs/reinforcement/js.md
@rtoal rtoal Even more JS reinforcement questions

JavaScript Reinforcement Practice
Here are a set of problems designed to help you reinforce and retain some useful JavaScript knowledge. If you are an Anki fan, consider adding some of these questions into a deck. 😀

1. Who created JavaScript and in what year?
   Brendan Eich, Netscape 1995

2. What was JavaScript originally called?
   Mocha / LiveScript

3. Why was JavaScript created?
   Client-side web scripting. Java was not suitable for this task

4. 96+833How do you write a line of text to the console?
   console.log("Hello, world")

5. How do you change the text of an element in a web browser document?
   Document.text / Document.write / document.body.textContent = "Hello, world.";

6. How do you access the third command line argument of a script, run on the command line, with node.js?
   process.argv(2)

7. Name the 7 data types of JavaScript (as of ES2019). Name the 8th that is coming soon.
   Undefined, Null, Boolean, Number, String, Symbol, Object / Bigint

8. Does JavaScript have separate types for integers and floating point values? If not, how can you tell whether a number is an integer or not?
   no / 'typeof x'

9. What are safe integers in JavaScript?
   In the range (−253, 253) (excluding the lower and upper bounds), JavaScript integers are safe: there is a one-to-one mapping between mathematical integers and their representations in JavaScript

10. If x has the value NaN, what is the value of the expression x === NaN? Why? What is the correct way to determine if an expression has the value NaN?
    undefined / x.isNaN()

11. How can you tell whether string s is a substring of string t?
    s.includes(t) / s.substr(t, len)

12. What two things can you do with backtick-delimited strings you can’t do with strings delimited with apostrophes or quotation marks?
    span lines and support string interpolation

13. Why does "🤣".length have the value 2?
    unicode character length

14. Give an example that shows the == operator is not transitive.
    == sucks
    null == undefined is true, but null === undefined is false. That is but one of the reasons why == sucks.
    Need another reason? == is NOT transitive! "16" == 16 and 16 == "0x10" but "0x10" != "16".

15. Why is 2 && 3 equal to 3, but 2 & 3 equal to 2?
    && = short-circuit logical and
    & = bitwise and

16. Name all the falsy values in JavaScript.
    undefined, null, nan, 0, "", false

17. How do you determine the type of an expression at runtime?
    .typeof

18. When should you use let and when should you use const?
    Use const when the value bound to the name should not and must not change; use let otherwise

19. What bad thing will happen if you forget to use let, const, or var when declaring an identifier?
    The identifier is never initialized or if it was initialized somewhere else in the program, it will be assigned by nearest scope.

20. What is the object literal { x, y } a shorthand for?
    Access and creation of object properties

21. What is the difference between p.x and p[x]?
    Create and access the properties with square bracket notation, or, if the key is a string of simple-enough characters, with dot-notation.

22. If x === 'y' then what is { x: 3, [x]: 5 } ?
    TODO

23. Why is [1,12] < [1,3] true but [1,42] < [1,3] false?
    TODO

24. How do you write an object to the console (beautifully formatted)?
    console.log(JSON.stringify(object, undefined, number)

25. Describe how a prototype-based language (like JavaScript) differs from a class-based language (like Java), in terms of thinking about collections of objects that share the same structure and behavior.
    Class Inheritance: A class is like a blueprint — a description of the object to be created. Classes inherit from classes and create subclass relationships: hierarchical class taxonomies.
    JavaScript’s class inheritance uses the prototype chain to wire the child `Constructor.prototype` to the parent `Constructor.prototype` for delegation. Usually, the `super()` constructor is also called. Those steps form single-ancestor parent/child hierarchies and create the tightest coupling available in OO design.
    Prototypal Inheritance: A prototype is a working object instance. Objects inherit directly from other objects.

26. Properties defined directly within an object are called **\*\***\_\_\_\_**\*\*** properties. Properties of an object accessible on the object’s prototype chain are called **\*\***\_\_\_\_**\*\*** properties.
    TODO

27. What do we mean when we say arrays are objects in JavaScript?
    An 'array' is not a primitive type in js. it is an object with multiple defined properties in it's prototype chain.

28. Describe how splice works.
    array.splice(start[, deleteCount[, item1[, item2[, ...]]]])
    method changes the contents of an array by removing or replacing existing elements and/or adding new elements in place.

29. What is the spread operator? Give an example of its use.
    ...x / const e = [5, ...b, -10] /allows an iterable to expand in places where 0+ arguments are expected. It is mostly used in variable array where there is more than 1 values are expected.It allows us the privilege to obtain a list of parameters from an array. Syntax of Spread operator is same as Rest parameter but it works completely opposite of it.

30. You might often see the expression a.slice(), for some array a. What does this expression do, exactly?
    method .sliceO() returns a shallow copy of a portion of an array into a new array object selected from begin to end (end not included) where begin and end represent the index of items in that array. The original array will not be modified.

31. How does one best create an array of size 100 in which every element is 0? (Do not write a loop.)
    let a = new Array(100)
    a.fill(0)

32. Write an equivalent expression to a.concat(b), where a and b are arrays, using spreads.
    let a = [...b]

33. a.push() mutates a. How do you do a non-mutating “push“?
    a.concat();

34. What does unshift do? Does it mutate or not? What does it return?
    The unshift() method adds new items to the beginning of an array, and returns the new length.

35. What is the difference between value types and reference types?
    reference value: the value stored in the variable is also copied into the location of the new variable.

    reference types: meaning object values are references. Objects have properties which are key-value pairs. Keys can be strings, numbers, or symbols

36. Why do you think the JavaScript designer decided that objects should be reference types?
    Objects have properties which are key-value pairs. Keys can be strings, numbers, or symbols. Create and access the properties with square bracket notation, or, if the key is a string of simple-enough characters, with dot-notation. You can even delete properties.

37. Since strings can be very large, you might think strings would be reference types in JavaScript. After all, they are reference types in Java. But in JavaScript, they are considered primitive (value) types. This might lead you to believe JavaScript is necessarily slow because strings are always copied on assignment. However, this is not the case! Why?
    TODO

38. Write an IIFE that applies the (anonymous, arrow) function that squares its argument to the value 100.
    const nextSquare = (() => {
    return this.pow(2);
    })();

39. In the function definition function f(x, y) { return [x, y]; }, what do we call x and y?
    TODO
40. In the function call f(y, z), what do we call y and z?
    TODO

41. A function is called higher-order if it does at least one of two things. What two things?
    TODO

42. What do the array methods map, filter, every, some, find, and findIndex do?
    map: creates a new array with the results of calling a provided function on every element in the calling array.
    filter: creates a new array with all elements that pass the test implemented by the provided function.
    every: tests whether all elements in the array pass the test implemented by the provided function. It returns a Boolean value.
    some: tests whether at least one element in the array passes the test implemented by the provided function. It returns a Boolean value.
    find: returns the value of the first element in the provided array that satisfies the provided testing function.
    findindex:returns the index of the first element in the array that satisfies the provided testing function. Otherwise, it returns -1, indicating that no element passed the test.

43. Write the function function f(x = 3) { return x \* y } (where y is some global variable) without using a default parameter.
    let y = 1;
    function f(x) { return x\*y}

44. What is a rest parameter? Give an example.
    function f(x, ...y) { return [x, y]; }

45. Can a function definition have multiple rest parameters? Why or why not?
    No, they must be at the end to define all extra arguments passed in

46. One could argue that all non-default parameters are really default parameters. Why?
    They are assigned as undefined.

47. In many languages, assignment has the form IDENTIFIER = EXPRESSION. In JavaScript, the left hand side is not just an identifier. What exactly is the left hand side called?
    LeftHandSideExpression / Reference

48. The old-fashioned to write a function that takes in an array and returns the sum of its first and third elements is: function f(a) {return a[0] + a[2];} Rewrite this in a modern fashion, where the function parameter is a pattern.
    TODO

49. Write a function that takes in an object and returns the product of its x and y properties. If no argument is passed, return 1. Write the function using a pattern for its parameter. Supply defaults so the function body is simply return x \* y;.
    TODO

50. Show how to declare the function that is called like this: push({onTheStack: s, theValue: v})? Use an object pattern in the parameter list.
    TODO

51. What are global scope, function scope, and block scope?
    Variables declared with var are local to the innermost enclosing function. When declared with const or let, they are local to the innermost enclosing block.
    global - variable declared outside a func

52. How do let-bound and var-bound function-scope variables differ? (Make sure the phrase “temporal dead zone” appears in your answer.)
    Using a let or const variable in its scope but before the declaration (i.e., within the temporal dead zone) throws a ReferenceError. Doing that with a var variable just gives you undefined.
    // Here’s a major ramification of function scope versus block scope:
    let a = [];
    for (var i = 0; i < 10; i++) {
    a[i] = () => i;
    }
    a[3](); // 10, GRRRRR
    for (let i = 0; i < 10; i++) {
    a[i] = () => i;
    }
    a[3](); // 3, YES I EXPECTED THAT

53. Write a function that takes in a number and returns a function that adds that number to its argument. Is the function you wrote higher-order? Why or why not? Does that function illustrate a closure? Why or why not? Does that function illustrate currying? Why or why not?
    TODO

54. What is currying good for, anyway?
    Currying lets you create a new function out of an existing function by fixing some parameters. It is a special case of lexical closure where the anonymous function is just a trivial wrapper which passes some captured arguments to another function

55. Is JavaScript statically-scoped or dynamically scoped?
    Variables are statically scoped in JavaScript

56. Do JavaScript functions exhibit shallow binding or deep binding?
    shallow

57. Given function\* f() {yield 1; yield 2; yield 3;}, what is wrong with writing for (let i of f) {console.log(i)}?
    f() is a generator and will only execute each time it is called. The for loop is redundant.

58. Why must (pretty much all reasonable) methods be non-arrow functions?
    TODO

59. Why should callbacks generally be arrow functions?
    TODO

60. What does the expression this refer to inside of a function called with the new operator?
    The expression 'this' will refer to the property of the new operator

61. Is this early-bound or late-bound?
    early-bound (runtime)

62. For function f and object x, the expressions f.call(x, 1, 2) and f.apply(x, [1, 2]) produce the same result. Write the equivalent expression using bind.
    TODO

63. JavaScript doesn’t have classes, but it does have the word class. But the keyword class does declare a function. How is this “function” defined? Give a short example.
    TODO

64. What happens under the hood when you write class A extends B? In particular what does A.prototype look like in this case?
    TODO

65. Why doesn’t Crockford like using this?
    TODO

66. What is the primary disadvantage of the Crockford-classless style of avoiding this and prototypes?
    TODO

67. How do you make a JavaScript object without a prototype?
    var dictionary = { destructor: "A destructive element" }; function getDefinition(word) { return dictionary[word]; }

68. When would you see a TypeError thrown? A RangeError? A SyntaxError? A ReferenceError?
    TODO

69. What is callback hell?
    Asynchronous JavaScript, or JavaScript that uses callbacks, is hard to get right intuitively. A lot of code ends up looking like this:
    fs.readdir(source, function (err, files) { if (err) { console.log('Error finding files: ' + err) } else { files.forEach(function (filename, fileIndex) { console.log(filename) gm(source + filename).size(function (err, values) { if (err) { console.log('Error identifying file size: ' + err) } else { console.log(filename + ' : ' + values) aspect = (values.width / values.height) widths.forEach(function (width, widthIndex) { height = Math.round(width / aspect) console.log('resizing ' + filename + 'to ' + height + 'x' + height) this.resize(width, height).write(dest + 'w' + width + '\_' + filename, function(err) { if (err) console.log('Error writing file: ' + err) }) }.bind(this)) } }) }) } })

70. What is an advantage of promises over callbacks?
    They are composable, so when you have lots of async operations, things are going to look much cleaner.

71. What exactly is a promise?
    myFunction(args).then(callback);
    A promise is an object representing a value which may or may not be ready yet, or may never be ready. It may be in one of three states:
    PendingFulfilledRejected

72. What does the function async function five() { return 5; } actually return?
    undefined

73. Given let f = async x => 1 and let g = async => 2 what do the expressions f() and g() return? Why? Why is the definition of g even acceptable?
    undefined

74. What are the most common names given to the parameters of the Promise constructor? What are they for?
    resolve, reject
    TODO

75. What is the difference between p.then(f, g) and p.then(f).catch(g) for a promise p?
    TODO

76. Why do most API invocations, or operating system calls (like reading and writing files) take in callbacks or return promises?
    TODO

77. Give the expression, in client-side JavaScript using fetch, that hits the (hypothetical) endpoint https://api.example.com/fortunes?limit=5 and, from its JSON response, places the first result in the DOM into the element with id fortune.
    TODO

78. Does await actually wait (block) for anything? It not, what exactly does it do?
    TODO

79. How does one “wait” for a whole bunch of async functions to all ”finish”?
    TODO

80. What is the difference between an accessor property and a data property? (Your answer should include all of the attributes for each kind of property.)
    TODO

81. How do you make a property read-only?
    TODO

82. What is the difference between sealing and freezing an object?
    TODO

83. How do you get the prototype of an object?
    TODO

84. How do you set an object’s prototype after the object has already been created?
    TODO

85. What is the difference between Object.keys and Object.getOwnPropertyNames?
    TODO

86. How does Object.entries work?
    TODO
