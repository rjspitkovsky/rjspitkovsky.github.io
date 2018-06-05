---
layout: post
title:      "Important Basics of JS: Variables, Scope, & Hoisting "
date:       2018-06-05 15:07:11 -0400
permalink:  important_basics_of_js_variables_scope_and_hoisting
---


As you go through the JavaScript curriculum, it can be very easy to get caught up in trying to understand the more complex components of the language and lose sight of the important basics that are the fundamentals to good JS coding. This post will talk about three of these fundamentals, because not having a good grasp on them is a very easy way to program an avoidable error in your code. The assignment of variables, the understanding of scope and the scope chain, and the concept of hoisting are all critical building blocks to understanding JS. Sometimes you need to review multiple times before getting them down and that is perfectly all right. 

**Variables**

The assignment of variables is important in JS because your method of assigning may have a major effect on the return values you may expect in your program. The original way to assign variables before ES5 was through the ```var``` keyword. However there were some holes with var that led to the creation of the ```let``` and ```const``` keywords. With ```var``` you can re-declare and re-assign a variable. Additionally, ```var``` variables will be available in the global scope even if it was defined within a block. That is not what you want because you may get unplanned values for your variables. ```let``` allows you to re-assign variables but not re-declare that variable. It is especially useful when iterating like: 
``` 
for(let i = 0; i < array.length; i++)
``` 
```let``` is also block-scoped so if you define a variable within a block it is not available on a global scope, which protects your variables from unwanted manipulation.

```const``` is the most secure way to assign a variable and the one that should be used most often. You cannot re-define or re-assign with ```const```. Unlike with ```var``` and ```let``` you must assign a variable when you declare the variable when using ```const```. This keyword is also block-scoped and will not leak out into the global scope when used within a block. 

The key takeaway here is to use ```const``` early and often, ```let``` when you know the value of the variable will change (like in iteration) and ```var```, generally never. Oh, and always use one of the above because not using a keyword automatically assigns the variable to the global scope regardless of where it is declared and that can mess with your program if that variable is used in other points in your code. 


**Scope**

Scope is extremely important to understand when going over JS. Scope is essentially, where certain information is available in your code. When you declare and assign a variable outside of a function or block, you are doing so in what is known as the global scope. 
```
const example = "Hello, world!"
``` 
This assignment is in the global scope and is available not only throughout the global scope but also the scope of anything declared within the global scope. This is know as the scope-chain. Functions have access to the variables declared within them AS WELL AS the variables declared in the global scope. As an example: 

```
const example= "Rich" 

function sayHelloRich() {
  const sentenceStart = "My name is " 
  return (sentenceStart + example)
}

sayHelloRich()
```

The function has access to both the sentenceStart variable declared within the function AND the example variable declared outside it but in the global scope. I like to think of a tree that has many branches. The branches are the functions (which themselves can branch off into functions) but they all lead back to the global scope which is the tree. 

Scope chains do not work backwards however. For example: 

```
const example= "Rich" 

function sayHelloRich() {
  const sentenceStart = "My name is " 
  return (sentenceStart + example)
}

sayHelloRich()

const newSentence = sentenceStart + example 

```
Will return a ```ReferenceError: sentenceStart is not defined``` because the global scope has no idea what sentenceStart refers to. It was only defined within the function. 


**Hoisting**

An even more complex concept to understand is that of hoisting. It is important to understand that the interpreter makes two passed through code when executing: a compilation phase, allocating memory to function and variable assignments and then an execution phase, actually running the code and firing off the methods with any assigned variables. If a variable is not assigned by the time the interpreter gets to the line of code in which it is invoked, you are gonna have some problems. A common hoisting example:

```
function hoisting() {
  console.log("My name is", name)
  var name = "Rich"
}

hoisting()
```
will return ```My name is undefined```. This is because when the interpreter reaches name it hasn't yet reached the definition of name. Using ```let``` or ```const``` will return an error. When a variable or function is hoisted it means that it's declaration has been moved to the top of its current scope and thus they can actually be invoked before they are defined. However, as seen in the example above, invoking a variable before it has been assigned will lead to many problems and unexpected outputs. That distinction between declaration and assignment is critical to understand and may be the difference between returning an error and smooth code. 

The best way to avoid issues with hoisting is by defining your variables and functions right at the top of your scope. They cannot be hoisted if they are already there at the top. Secondly, do not use ```var``` if you can help it. If you use ```let``` or ```const``` you at least return an error message that you can debug but using ```var``` as your variable declarer will return undefined instead of error messages. You may think your code is running correctly, until all of sudden you aren't getting the expected return values and you are left combing through your program trying to debug while not ripping your hair out. 

For me, I am a practice learner. I need to practice, practice and practice some more with these concepts but putting in the time to get a solid understanding of the basic things will go so very far in making you an exceptional programmer. This is true in general, but it also applies to the key concepts of variables, scoping, and hoisting. 
