# Anonymous Functions Readme

## Objectives

+ Explain what an anonymous function is and why it's useful
+ Call an anonymous function

## Intro

We know functions (like methods in Ruby) are used to bundle our code to be able to reuse again and again and again. So why take the time to define and store a function we never plan on reusing? It takes up memory, requires extra typing, and completely goes against the purpose of a function. Thankfully, JavaScript allows us to easily solve this problem by using an **anonymous function**. An anonymous function is one that is never defined and is planned on being used once. They allow us to execute a block of a code once. One and done.


## Usage

One of the most common usage's for anonymous functions is a callback function (function passed as a parameter to another function).

## Event Handler Callbacks

We know that functions can accept functions as parameters. We've seen this time and time again when setting up jQuery event handlers. The `on` function accepts a string of the event you would like to bind, and a function which is executed when the event is trigged. But that function we pass as a parameter, it was never defined anywhere previously. That function does not have a name.


```js
$('#submit').on('click', function(){
  alert("form submitted!");
});
```

The anonymous function (the callback function) in the example above simply creates an alert in the browser with the text `"form submitted!"`. This function is never executed on another part of the code. We only want it to fire when the submit button is clicked.

### setTimeout

The `setTimeout` function executes a code block after a specific amount of time has passed. This function accepts two parameters, a function and time in milliseconds.

```js
setTimeout(function(){ console.log("I waited 5 seconds to execute");}, 5000)
```

The `setTimeout` function accepts the anonymous function as the first parameter. This anonymous function prints `"I waited 5 seconds to execute"` to the console.

```js
function(){ console.log("I waited 5 seconds to execute");}
```


### Function Expression

We've seen function expressions already, but they can also be considered anonymous functions:

```js
var numberz = function() {
    return 6+3;
}

//anonymous function because the function the variable is storing doesn't have a name

var cats = function kitties() {
    return "meow meow pow pow";
}
// not an anonymous function because the function has the name kitties
```

Remember that variable declarations get hoisted to the top of their scope, but variable expressions do not. In the above example, `var numberz;` would get hoisted to the top of the scope, not the anonymous function it's storing. Therefore, at the top of the scope, the variable `numberz` is storing `undefined` and thus not taking up memory for the entire duration of the program.

## Postscript

You might be thinking that you've seen something like these anonymous functions before — and you'd be right. Anonymous function are _sort of_ like Ruby blocks in that they provide a handy way to process incoming data but can't be called outside of their immediate context. Pretty cool, eh?

## Resources

+ [JavaScript WE Blog](https://javascriptweblog.wordpress.com/2010/07/06/function-declarations-vs-function-expressions/)
+ [Thoughtbot Blog](https://robots.thoughtbot.com/back-to-basics-anonymous-functions-and-closures)

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/js-anonymous-functions-readme' title='Anonymous Functions Readme'>Anonymous Functions Readme</a> on Learn.co and start learning to code for free.</p>

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/js-anonymous-functions-readme'>Js Anonymous Functions</a> on Learn.co and start learning to code for free.</p>
