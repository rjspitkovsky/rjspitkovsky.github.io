---
layout: post
title:      "OO Ruby Obstacles Part II "
date:       2018-03-19 16:18:58 +0000
permalink:  oo_ruby_obstacles_part_ii
---


I am gladly through the Object Oriented Ruby portion of the curriculum and have moved towards Sinatra, through SQL and ORMs and ActiveRecord. But it is important to reflect and report on what concepts challenged me through the OO section. 

**Object Collaboration**

The concept of objects collaborating and how they collaborate did not come naturally to me. There are three general types of collaboration that we went over: *Belongs to*, *has many*, and *has many through*. 

Belongs to, like a song belonging to an artist or a book belonging to an author can be achieved by simply setting and getting an instance variable in the Song or Book class you create. You add an attr_accessor for the value it belongs to, like :artist or :author, and an instance of an object will now have those attributes that you can add to (in an initialize method for instance).

Has many, the converse, is when an Author has many books or an Artist has many songs. Those are represented by an instance variable set to an empty array. You can then add an instance of a Book or a Song to those arrays. It is the responsibility of the Book or Song (children) class to add themselves to the parent instance that has many of them. 

Has many through, is a next level orientation. A genre has many authors through books, or has many artists through songs. A child class can have multiple parents. You'll have to create a method, iterating through each of the values in the @@all variable of the other parent class to set the genre value to itSELF. 

Slowly but surely, with patience, time, and a lot of review, these concepts became clearer to me. Do not be upset if these complex relationships are confusing to you at first. 

**Metaprograming and the Send Method**

While the curriculum does a great job at explaining slowly and in detail what Metaprogramming is, how the Send method works, and how to use it, I still needed to review that section multiple times before being comfortable with it. Code that writes code for you can be an extremely powerful tool. You do not even need to know what the attributes you're adding to your class are going to be when creating a class. You can get around typing out setter code (@name = name, for instance) via the send method. The send method, `send(("#{key}="), value)` will, if you pass it a hash of attributes, assign the key as the variable and the value as the value of that variable. This process is called mass assignment. You can quickly and easily assign values to all the attribute variables that your class has, without necessarily knowing what the values and variables are. This helps the creation of classes and instantiation of objects so that you can get to the higher level methods quicker. Again, now that I have put in the work to understand this concept, I recognize its value and am excited to be able to use this tool. It was however, another exercise in not getting frustrated, being patient with the material, and continuing to grind until you get it. 

Now that I feel like a have a firm grasp on OO Ruby my venture into SQL, ORM, and ActiveRecord has gone fairly smoothly. I am understanding the concepts and am happy with my progression. More thoughts on these topics to come... 
