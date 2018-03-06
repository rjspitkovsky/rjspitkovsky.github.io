---
layout: post
title:      "CLI Data Gem Project "
date:       2018-03-06 21:59:55 +0000
permalink:  cli_data_gem_project
---


I have just completed the first big kahuna portfolio project for the Flatiron School. I started my journey through this project feeling great, then frustrated, then pretty good again, so in that respect I am developing quite nicely as a programmer. 

My project revolves around the New York Times Bestsellers List. I originally had a different idea of which website to scrape, and I made the mistake of setting up my project environment without really thinking, planning out how I wanted my code to work, and exactly what and how I was going to scrape. When I went ahead and realized that my original idea would be too complex, time-consuming and wouldn't best fulfill the requirements of the project I scraped that idea (pun intended), and started brainstorming new ideas. This part was the most frustrating. 

I felt like I needed to choose a topic that included objects with multiple attributes that can collaborate but it also needed to be from a website that was relatively easy to scrape because I did not want to get bogged down by the trial-and-error method of scraping text. The NYT Bestseller list fulfills both of those preferences. The HTML on that website is well-tagged so finding specific key text did not take too long. On top of that, it is filled with different attributes that can collaborate. 

Their are 5 categories or different lists on the website. Each of these categories has a name and *has many* books. Each book has a title, author, summary, and *belongs to* a category. I created a class for each of those objects. I created a third class, simply titled Scraper, whose job was to scrape sections for the category name, then instantiate an instance of a Category with @name = name. I then scraped all the books within each category, and instantiated an instance of a book with it's necessary attributes-- @title, @author, @summary, and @category. I then added the #add_book_to_category method which looks up the different category instances in Category.all and add the book when the Category.name == Book.category. 

Finally, I built the CLI class which deals with user interaction. The interface first lists the different categories by their name--- after the user chooses one of the categories, it lists the books in that category. You can then choose the title of the book you'd like a summary from, and if the summary titiliates you enough, you can choose to open the external source website in your browser and purchase the book. 

The key to this project was reviewing previous labs along with the different live programming videos that supplement the lab. Seeing it done helped me organize my thoughts when it was my turn to create an app. Secondly, taking the time to note (on paper) exactly what attributes I wanted each object to have, how the objects would collaborate, and how did I want the user interface to look like, BEFORE I even opened the project on my computer helped me significantly. I had a clear idea of what I wanted to do, what I wanted to scrape, and how I would go about passing the different information along. 

Considering this is the first app/gem I have ever built from start to finish without aid, I am proud of my work. My code can be found at: https://github.com/rjspitkovsky/nyt-bestsellers-cli-app. I can definitely go back to refactor the code as well as add new improvements but I feel very satisfied with how the CLI turned out. 
