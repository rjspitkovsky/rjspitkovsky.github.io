---
layout: post
title:      "OO Ruby Obstacles Part I"
date:       2018-02-27 02:32:34 +0000
permalink:  oo_ruby_obstacles_part_i
---


As I near the end of the Object Oriented Ruby portion of the curriculum, I am faced with a number of increasingly complex and challenging labs. While I stare at my screen for hours-turned-to-days I am reflecting on the section as a whole-- what did I find easy? What concepts took me longer to grasp? I believe this kind of introspection is important because understanding your weaknesses and working on them is a great way to be a well-rounded programmer(or a well-rounded anything, really). This blog post is Part I of a two-part reflection on OO Ruby: The happy part (a/k/a the things I found easier to pick up). Part II, coming shortly, will be the frustrating part( a/k/a the concepts that trouble(d) me greatly).  

**Class Methods/Variables && Instance Methods/Variables**

Classes are a blueprint and a factory. You can define a thing and then create that thing based on your specifications. And that thing can do whatever you tell it to do. Like a well-trained baby. There is a single baby instance and there is the royal we of babies-- all the babies that have ever existed and can do the same thing. 
Each of those categories have relevant variables and methods. 

A class variable, is a variable that stores information for all the babies ever created (when the stork came). They are denoted by double-ats, like @@, as in @@all. We can call class methods on this variable, like self.all, which should return whatever resides in @@all (usually the instances of the class). We can say self.reset, which should clear the contents of @@all. It is important to understand that you are dealing with the universal concept of a babies, when talking about class methods and variables (In our baby example, at least).

However each individual baby is an instance of a baby. They have their own individual attributes, like a name or a birthyear. We create instance variables with a single-at, like @, as in @name. We write setter and getter methods so we can access these instance variables. We can write out methods that can only work on an individual instance of a baby. It can be tough dealing with so much information within a class to distinguish what methods should be used for instances of an object and which methods are for the class itself. 

**Self**

The next concept, which is closely related to class/instance methods is the concept of self. Self means two things-- the class itSELF or the instance itSELF. It all depends on where you are placing the self-- in an instance method, self will mean the instance of the object while in a class method, it will mean the class. It is super easy to make a mistake and use self incorrectly. If you do the return value will cause an error in your code because methods are scope limited-- for example, an instance method can't really understand the concept of the class as a whole. This is just another example of practice makes perfect--- after implementing self over and over in my labs I picked up conceptually what self meant and when was the appropriate time to use the different self keywords. 

**Scraping**

I was a bit concerned about scraping before diving into the lessons on it. Pulling information out of a webpage and then manipulating that information seemed complicated. It certainly wasn't easy but I was pleasantly surprised at how I was able to understand the information fairly quickly. Scraping is a matter of patience--finding the correct element identifiers in code that you need for your program is a trial and error type of task. But as programmers we live in a world full of errors that we try to turn green, so we should not be afraid of them. 

Scraping leads into metaprogramming, which provides so much opportunity-- writing code that writes code itself can tackle and manipulate so much information-- it's a really powerful tool that I am excited to get proficient at and use. I suppose that is the whole appeal of Object Oriented Ruby in the first place-- the power and flexibility you have with information. You can manipulate so much data with ease. After this section, I understood completely why Ruby is the first major language taught in Flatiron. It is so powerful with such simple, straightforward syntax. 



In my next post I will talk about concepts that took me much longer to understand, and that I will still need to go back and review to excel. The fact that I don't get everything perfect right away doesn't discourage me at all because that is a normal part of learning something (particularly when you are immersing yourself completely in new subjects). 
