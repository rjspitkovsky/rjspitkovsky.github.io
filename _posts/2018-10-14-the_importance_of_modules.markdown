---
layout: post
title:      "The Importance of Modules!"
date:       2018-10-14 22:15:43 +0000
permalink:  the_importance_of_modules
---


An important tool used to create code that is easier to understand and architecturally sound is a module. Modules are like classes in that they are a factory for certain methods you want to write. Unlike classes you cannot instantiate a module to create a new object. Module.new() is not a thing. However, let's say you are working with multiple different objects that you want to provide some shared functionality for. Rather than repeating yourself by writing the same method in every class you can create a Module and then have the classes inherit that module. Now, if down the road in the development of your application you want to change the functionality of the classes you can just change the code in the module as opposed to in each class. Saves time and is cleaner.

## Include vs. Extend

Classes can have all sorts of methods written for it--some are written for an individual object of a class and some are written for the class itself. Like Class.all() traditionally returns all of the instances of the class. That is known as a class method. Modules can have both instance methods and class methods. When your class inherits from a model you can use one of two keywords: Include or Extend. For methods inherited from a Module via Include, the Class will assume it is an instance method. If you try to call a class method on one of these inherited instance methods you will get an error. The converse, is Extend. The Extend keyword implies a class method-- calling it on an instance of a Class will return an error. 


Modules may not be necessary in getting the functionality you seek but they are an important tool. They consolidate your code so that your Classes aren't cluttered and that your programming intentions are clear. Make sure to use the proper keyword when inheriting--- Include for instance methods, Extend for class methods. That could be a really easy way to get an error. Important to think about code readability after you've got it working and Modules can help. 
