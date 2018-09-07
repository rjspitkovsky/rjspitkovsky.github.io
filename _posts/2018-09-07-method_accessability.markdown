---
layout: post
title:      "Method Accessability"
date:       2018-09-07 15:08:16 +0000
permalink:  method_accessability
---


When working in Object-Oriented languages like Ruby, building out classes is a major component of building out functional code. One important factor to consider when creating a new class is the accessability of your methods within the class. Figuring out where your methods go in terms of accessability not only reduces the chances of unwanted manipulation of an object but also is a good design practice. Other programmers looking at your code will have a better understanding of the expectations of the code and how it works. There are three types of method accessability levels: Public, Private, and Protected. 

## Public 
Public methods are the default in Ruby. Any method you write will automatically be deemed a public one and can be accessed outside of the scope of the object. Any ```attr_accessor``` that you use on an attribute when instantiating an instance of your object is a type of public method. You can be dealing with an instance of an object in a different class and still be able to call a public method on that instance. 

## Private 
Private methods have the tightest scope in Ruby. They are used exclusively within the object they are defined in. They need the ```private``` keyword before them to inform the interpreter that they have a higher level of accessability. The design principle is that a consumer of an object does not need to know every detail about how an object functions. If there was a #make_eggs(3) method on a Chef class the return value may be a string, ```"You now have 3 eggs. Enjoy!```. But there is more that goes into making the eggs that the Chef class does not want you to see or be able to manipulate. Only the instance of the Chef that is making the eggs should have access to all the methods, like #fetch_eggs, #crack_eggs, #whisk_eggs, that are required to get to the final return value. 

## Protected 
Protected methods are less common but still important. They are methods that also cannot be used outside of the scope of the class but can be accessed by other instances of the same class. They are a bit of a half-way between public and private methods. Let's say that our Chef who had the #make_eggs(3) method called on it needed the help of a different Chef who was performing the helper methods, #fetch_eggs, #crack_eggs, #whisk_eggs. The method that communicates between the two Chef objects could be a protected method. It isn't something that should be accessable and acted on from outside the Object, like a public method, but since it involves communicating between two different instances of the same object type it can't be as strict as a private method. Protected methods are a nice inbetween that gives your object good security and good design. 

Method accessability may seem like a non-important concept in the grand scheme of writing out a large program but the success is in the details. Public, Private, Protected methods are an important component of creating clean code that is easy to understand and hard to manipulate outside of what is needed for proper functionality. This is part of the building blocks for writing good code and it is definitely worth a refresher every now and again. 
