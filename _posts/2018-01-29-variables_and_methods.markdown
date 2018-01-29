---
layout: post
title:      "Variables and Methods "
date:       2018-01-29 18:16:39 +0000
permalink:  variables_and_methods
---


After a few posts regarding my initial thoughts and feelings about the start of my journey through the FlatIron curriculum, I think it is important (and necessary) to actually talk about code and things that are challenging me. 

A concept that took me a little while to comprehend was the relationship of variables and methods in Ruby. As most of us know, a variable is a word that is a placeholder for other information. It is represented by an equal sign(=). An example of a variable would be: name = "Rich", with the word on the left hand side of the equal sign being the variable and the word on the right hand side being the value of that variable. We can change the value of the variable at any time (name = "Richard"). 

In Ruby, variables are essential. However, if we define a variable outside of a method, that variable is useless inside of that method. That is, unless we specifically call the variable as an argument to the method. If I used my above variable, name, inside of a method without redefining it or calling it in as an argument, I will get an error message. The interpreter does not recognize name, even if I had just defined it. 

The inverse relationship is true as well: If I define name = "Richard" inside of my method, then after I have finished defining that method and try to call for the name variable, I will get another error message. Once again, the interpreter doesn't recognize the variable. I like to think of it as a bubble-- variables aren't recognized within a method when defined outside of one, nor are they recognized outside a method when defined within them. Again, the exception is if you specifically use the variable in an argument for the method. 

This concept caused me a bit of a hiccup early on. Through practice I learned to be more diligent about when I define my variable. The relationships between variables and methods is a close one because we often need variables in our method definitions to give changing values(the name of a user) a static value(the word 'name'). Because of that close relationship, it is important to keep your variable definitions in order. And of course, do not freak out after an error message. It could be as simple as moving a variable definition inside or outside of a method.  
