---
layout: post
title:      "CSS Grid Intro "
date:       2018-09-16 14:31:58 +0000
permalink:  css_grid_intro
---


There are many different ways to incorporate CSS into your project. One of them is CSS Grid, which I have been getting more comfortable at. Styling is super important-- you can write some really excellent front-end code but it is hard to separate logic from looks. The aesthetic of a page can sometimes be more important for user experience than the content of it so practicing your styling is something worth doing. 

CSS Grid is pretty self-explanatory-- you style your elements in a grid like manner. If you have a container Div, with a ```display: grid;``` then you can add ```grid-template-columns``` attribute to create columns. The number of arguments you provide will equal the number of columns there will be. If you give the container ```grid-template-columns: 50px 50px;``` you will have two equal sized columns of 50 pixels. Likewise, ```grid-template-rows: 50px 50px``` will do the same thing but create two equal sized horizontal rows instead of columns. 

Now that we can create columns and rows we can manipulate them to our specific needs. The columns or rows do not have to be uniformly sized so there is a lot of room to play with. The items within the spaces of our grids can be manipulated on individually as well. You can align an item horizontally within a specific grid box with ```justify-self``` and align all items with ```justify-items```. Similarly you can align an item vertically within a specific grid box with ```align-self``` and align all items with ```align-items```.  

There are shorthanded ways to get a desired output with shorthand code. You can use the ```repeat()``` function or the ```auto-fill``` and ```auto-fit``` keywords to fit a grid to the page. The best way to get familiar with CSS grid and its capabilities is by practicing. Go make a parent container div, some children divs, and play around. This is just the earliest beginnings of what someone can do with thoughtful styling. 
