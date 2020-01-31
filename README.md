# Sprint Challenge: JavaScript Fundamentals

This challenge allows you to practice the concepts and techniques learned over the past week and apply them in a survey of problems. This Sprint explored JavaScript Fundamentals. During this Sprint, you studied variables, functions, object literals, arrays, this keyword, prototypes, and class syntax. In your challenge this week, you will demonstrate proficiency by completing a survey of JavaScript problems.

## Instructions

**Read these instructions carefully. Understand exactly what is expected _before_ starting this Sprint Challenge.**

This is an individual assessment. All work must be your own. Your challenge score is a measure of your ability to work independently using the material covered through this sprint. You need to demonstrate proficiency in the concepts and objectives introduced and practiced in preceding days.

You are not allowed to collaborate during the Sprint Challenge. However, you are encouraged to follow the twenty-minute rule and seek support from your TL and Instructor in your cohort help channel on Slack. Your work reflects your proficiency in JavaScript fundamentals.

You have three hours to complete this challenge. Plan your time accordingly.

## Commits

Commit your code regularly and meaningfully. This helps both you (in case you ever need to return to old code for any number of reasons) and your team lead.

## Description

You will notice there are several JavaScript files being brought into the index.html file.  Each of those files contain JavaScript problems you need to solve.  If you get stuck on something, skip over it and come back to it later.

In meeting the minimum viable product (MVP) specifications listed below, you should have a console full of correct responses to the problems given.

## Self-Study Questions

Demonstrate your understanding of this week's concepts by answering the following free-form questions.

Edit this document to include your answers after each question. Make sure to leave a blank line above and below your answer so it is clear and easy to read by your team lead

1. Describe the biggest difference between `.forEach` & `.map`.

`forEach` iterates through an array without returning anything, whereas `map` iterates through the array it was called on and returns a new array, with the same number of elements. This makes it so that other methods can be chained after a call to `map` but not after a call to `forEach` (because it doesn't return anything).

2. What is the difference between a function and a method?

A method is a kind of function, which is invoked as a property of an object. `this` in a method refers to the object preceding the `.`, so that a method can refer to the properties of the object that receives its function call. Functions in JavaScript are also objects with properties, but they are not implicitly bound to an object unless they are a property of that object.

3. What is closure?

Closure describes the way that a function "remembers" the environment in which it was defined, so that it has access to variables within its inner and outer lexical environments. In JavaScript, functions automatically create their own closure when they are created. For example:
```
function outer() {
    const foo = 42;
    return function inner() {
        return foo;
    }
}
const inner = outer();
console.log(inner()); // 42
```
The `inner` function has access to `foo` even though `foo` is otherwise inaccessible from outside of the `outer` function. Variables in a function's closure are referenced from a hidden environment property on the function's prototype.

4. Describe the four rules of the 'this' keyword.

a. Window/Global Object Binding

When invoked in the global scope, i.e., not bound to any other object, the `this` keyword refers to the `window` object in the browser and the `global` object in Node.

b. Implicit Binding

When calling a method on an object, `this` refers to the object preceding the dot before the method invocation. For example, when calling `foo.bar()` the value of `this` is `foo`. Arrow functions, however, are not implicitly bound, so if `foo.baz()` is an arrow function, `this` does not refer to `foo`.

c. New Binding

The `new` keyword creates and returns a new object from a constructor function, ignoring any value returned from the function body with the `return` keyword. `this` refers to the new object created from a constructor function. The new object is unique, existing in its own slot in memory.

d. Explicit Binding

The `call` and `apply` methods, when invoked on a function will explicitly bind the `this` parameter passed in as an argument, allowing us to override an object's implicitly bound `this` to any object.

5. Why do we need super() in an extended class?

When called within the constructor of an extended class, `super()` calls the constructor of its parent class, initializing `this` so that it inherits the properties and methods of the parent class. It must be called in order to access `this` and return from the constructor of an extended class.

## Project Set up

Follow these steps to set up and work on your project:

- [x] Create a forked copy of this project.
- [x] Add TL as collaborator on Github.
- [x] Clone your OWN version of Repo (Not Lambda's by mistake!).
- [x] Create a new Branch on the clone: git checkout -b `<firstName-lastName>`.
- [x] Create a pull request before you start working on the project requirements.  You will continuously push your updates throughout the project.
- [x] You are now ready to build this project with your preferred IDE
- [x] Implement the project on your Branch, committing changes regularly.
- [x] Push commits: git push origin `<firstName-lastName>`.

Follow these steps for completing your project:

- [x] Submit a Pull-Request to merge <firstName-lastName> Branch into master (student's  Repo).
- [x] Add your team lead as a Reviewer on the Pull-request
- [ ] TL then will count the HW as done by  merging the branch back into master.


## Minimum Viable Product

Your finished project must include all of the following requirements:

**Pro tip for this challenge: If something seems like it isn't working locally, copy and paste your code up to codepen and take another look at the console.**

## Task 1: Objects and Arrays
Test your knowledge of objects and arrays. 
* [x] Use the [objects-arrays.js](challenges/objects-arrays.js) link to get started.  Read the instructions carefully!

## Task 2: Functions
This challenge takes a look at callbacks and closures as well as scope. 
* [x] Use the [functions.js](challenges/functions.js) link to get started. Read the instructions carefully!

## Task 3: Prototypes
Create constructors, bind methods, and create cuboids in this prototypes challenge.
* [x] Use the [prototypes.js](challenges/prototypes.js) link to get started. Read the instructions carefully!

## Task 4: Classes
Once you have completed the prototypes challenge, it's time to convert all your hard work into classes.
* [x] Use the [classes.js](challenges/classes.js) link to get started. Read the instructions carefully!

In your solutions, it is essential that you follow best practices and produce clean and professional results. Schedule time to review, refine, and assess your work and perform basic professional polishing including spell-checking and grammar-checking on your work. It is better to submit a challenge that meets MVP than one that attempts too much and does not.

## Stretch Problems

There are a few stretch problems found throughout the files, don't work on them until you are finished with MVP requirements!
