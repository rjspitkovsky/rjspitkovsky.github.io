---
layout: post
title:      "Inner/Outer Joins"
date:       2018-09-23 16:02:51 +0000
permalink:  inner_outer_joins
---


Recently I was at a networking event talking to a very friendly person working at a major banking organization about some of the work he was doing. As we touched on back-end development, he quickly gave me a pop quiz: What is an inner join and an outer join? I had already talked about going over SQL and database queries as part of the Flatiron School curriculum so I had better get this right -- or else I'd feel like I'd lose credibility as a prospective employee down the road. 

Fortunately, I answered the question correctly despite the pressure I felt. The rest of the conversation went very positively and I was invited to connect with him; my goal of expanding my network with great people at cool companies was gaining steam. 

So what is the answer? What are inner joins and outer joins? 

##Inner Joins 
Imagine having two (or more) tables of information in your database. These tables are connected by a particular column present in both, maybe an ID number for a name. An inner join will allow you to create a new table with data that is a match between your tables. If you consider a venn diagram, and inner join would be the intersection of the two circles. 

##Outer Joins 
Like an inner join, an Outer Join creates a new table from the data of other tables used in the query. There are three types of Outer Joins: the most inclusive one is a Full Outer Join. This will return a table of all the records between the tables used. In the venn diagram analogy, this would be the entire diagram (both circles and the intersection). 

The Left Outer Join will return the entire Left table (circle) and the intersection of your tables wherever there is a match. 
The Right Outer Join will return the entire Right table (circle) and the intersection of your tables wherever there is a match. 

Join tables are extremely important for managing your data. They link different tables of information and condense what you may need in a single table that can be easily read and dissected by a program. If you are working with any back-end system, you will probably need to play with your data and thus it is important to remember the basics of inner and outer joins. Also, you never know when you might get put on the spot. 
