---
layout: post
title:      "My Sinatra Portfolio Project "
date:       2018-04-04 00:18:27 +0000
permalink:  my_sinatra_portfolio_project
---


* After completing my second portfolio project my main takeaway for a successful program is practice and preparation. The Flatiron School does a fantastic job at providing us step-by-step labs that prepare us for handling the requirements of this project. After completing numerous labs like Playlister, NYC, and Fwitter, you understand not just HOW the program is designed but WHY. Then when it comes time to write your own application, the numerous reps you've done over the past weeks come in handy. Migrations, models with ActiveRecord associations, controller routes, and erb view pages are all concepts that I needed to go over a few times to gain a deeper understanding, but putting in the work then served me well when the time came to write my final project. 

The other type of preparation I found crucial was old fashioned pen-on-paper notes that I took before I even began typing my code. I stubed out exactly how the different sections of my code was going to look. How the migrations were going to relate to my models; how those models related to the controllers, and how the controllers were going to interact with the views directory. You may think that its a waste of time to code twice but I disagree. I was able to refer to my notes to help keep me organized and on track when typing it out in my text editor and as I was going through my code the second time I was able to do some refactoring. I definitely believe taking the time to sketch out the code helped save me time and headache in the long run. 

So what is my program all about? I wrote a CarViewer web app. The idea was that you can browse cars posted for sale, and post a car of your own for sale. There are two models, a User and a Car. The user has_many cars (for sale) and a car belongs_to a user. The user class requires validation of a username, email and password. If someone tries to create an account without all three of those fields, the user will be directed to a /failure page and will have to try creating an account again. Once logged in, a user can browse the list of all posted cars on /cars. They can select an individual car and view it's details. If the user is viewing a car that they themselves posted, they have the ability to edit or delete that car. I used the conditional `if current_user.id == @car.user_id` to ensure that only the car owner can manipulate a particular car. Users also have the ability to view user pages and see the cars posted by a particular user. 

The app is extremely rudimental in design but I do think that it is a satisfactory CRUD program. Users can create, read, update, and delete their cars. I am proud of the final result and am thrilled with my work process which I believe was effective in helping me finish the project in a timely manner. 
