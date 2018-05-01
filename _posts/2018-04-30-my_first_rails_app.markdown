---
layout: post
title:      "My First Rails App"
date:       2018-05-01 03:16:00 +0000
permalink:  my_first_rails_app
---


Like each of the previous two portfolio projects, this one marked the hardest point of the course thus far. Each section is a new summit I have to climb as I near the top of the FlatIron School Mountain. This project once again taught me the importance of organization. Unlike my Sinatra project, the Rails app is just too large to write out front-to-back before actually coding. I decided to compartmentalize: separate the project into major parts and then drill down from there as opposed to trying to solve the whole jigsaw puzzle at once. 

I spent time working on my models, migrations, and their relationships. I spent time going over my routes, nested resources, and controller actions. I spent time going over my views and what information I want to manipulate from the database to present to the user. I made sure to get things working before refactoring--making use of helpers and partials. Once I got the architecture down, I moved on to what I considered to be the harder requirements: Class models and Omniauth. Again, after I incorporated those features into my app, I refactored. I am sure, there is more refactoring to be done but I am still pleased with my results. 

Oh, one more thing before I get into the details of my app: Troubleshooting. So very important. Learning how to search the extensive library of the internet to solve your coding problems is a crucial skill to becoming a successful programmer. I took a deep breath, didn't get frustrated because I knew the answer would be found if I spend enough time looking for it, and then I eventually found the information I was looking for and kept it moving. Do not be afraid to admit you don't know something!

My app, called Explorers Unite!, is a travel lifestyle site where Users can post reviews of trips that they've taken. They can see other User's reviews and their recommendations. They have the option to filter trips by a particular timeframe (which is how I fulfilled the class method requirement) and filter by particular country and see each trip to that country. My app has three models, a User which has many trips and has many countries through trips; a Country which has many trips and has many users through trips, and a Trip which belongs to a user and a country. The nested resource requirement is fulfilled through seeing the trips of each user (i.e. users/:user_id/trips/:id). Users can choose to sign in through Facebook which fulfills the 3rd party sign in requirement. 

It takes a lot to complete a major project, especially your first of its kind. You need to be patient and organized. You need to review the curriculum and the videos reviews provided. You can't get down on yourself when you get stuck. I know I have so much more room to grow and improve but I am still creating apps that fulfill the requirements and more importantly, I feel like I am understanding HOW exactly my code works. Moving onward and upward!
