---
layout: post
title:      "The Importance of Validations"
date:       2018-09-30 15:52:35 +0000
permalink:  the_importance_of_validations
---


On a recent job interview, the topic turned to validations and why they are important. I thought the concept was worth exploring so after the interview I did a little refresh on the matter. Simply put, validations are a check against the data being saved into the database. They make sure that that data is formatted to your specifications so that bad data doesn't get in and throw an error or return a value you weren't expecting. 

If your model inherits from ActiveRecord::Base, that model will have access to the ```validates``` method. It takes two arguments, the attribute you are checking against and the parameters that will allow the data to save properly. If bad data is entered you will not see an error message; the database will remain unchanged. The data is validated at the point of attempted save into the database-- using #new will not set up any validation checks as that method doesn't save, but using #create will do the trick. You can check if your data is valid before attempting to save it to the database using #valid? 

You can validate any attribute that you have. Common ones include: ```presence: true``` which validates that there is data for that attribute--like how you cannot leave a password field blank when signing up to an app; ```length:``` which sets the appropriate amount of characters to be entered for a particular attribute; ```uniqueness: true``` which makes sure that the data entered for this particular object is unique amongst all the objects in the database. 

You can also write your own validation helper method in the body of the model. Say you want to exclude particular words from a database-- you would need to build a method that takes in the pending data, then checks to make sure that any banned word doesn't appear. If they don't then the data saves to the database; otherwise it won't. You may want to add error messages to this helper method to make it easier to figure out why the data was unsuccessfully saved. In this case you use ```validate {helper_method}``` instead of ```validates```. 

Validations are just an extra layer of security that protect your database from bad information. It is important to understant conceptually why they are important and to use them in your own projects, or else you may be in for a rude surprise. 
