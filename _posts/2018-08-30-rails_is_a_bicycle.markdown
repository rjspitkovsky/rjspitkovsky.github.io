---
layout: post
title:      "Rails is a bicycle"
date:       2018-08-30 16:17:15 +0000
permalink:  rails_is_a_bicycle
---


Since I've graduated the Flatiron School, I have been trying to keep myself fresh with my own independent projects. I have built things in React, HTML/CSS/JS, have been dipping my foot in the Python pond, and in Rails. I love Rails. The compartmentalized nature of the Model View Controller architecture comes naturally to me. Even though the latter part of the curriculum was living in JavaScript land, once I started building out a program in Ruby-on-Rails, initializing a proper environment came right back to me. (Like riding a bike, ahem)

```rails new [project name]``` is simple enough and gets you started, with a comprehensive Gemfile and you're own console sandbox along with other features that would be annoying as hell to set up every single time you wanted to start a new project. From there, I set up my migrations in the database--SQLite as the default is a great choice (though I need to work on expanding my database selections). After that I set up my models, which inherit from ApplicationRecord--the first things I do here are set up my relationships (has_many, belongs_to, has_many through, etc.) and my validations. Validations are so important to make sure your data is consistent and correct so do not skip on this. 

I set up my routes in my config file and I love the control I have in my url naming and the ease with which I can link to my controllers. Not to mention, I can nest my resources here for greater accuracy. For instance, if I want to link to the page for the 3rd book by a particular author my url would end with ```/author/1/books/3```. This leads me to building out my controllers, the middleman that brings the database/model logic to my views that will be displayed by the browser. If you are building out a program by the REST convention you've got 7 easy-to-remember methods to build out here-- index, new, create, show, edit, update, delete. 

Finally, you take the data that you collected in the controller, store it in an instance variable, and display it in the view page. The name convention is also very simple-- create a new folder in your views folder that is the name of your controller and then create a file in that folder that's the name of the action you're using, ex: ```new.html.erb```. That ```erb```, Embedded RuBy, means that you can mix your ruby with your html and the result is dynamically dynamite. 

Obviously there is so much more to Rails than what I've covered, but the setting up process is incredible. It is simple, easy to understand, and even after a little bit of time away from it, comes back to you and makes sense pretty much right away. Thank you DHH! 


