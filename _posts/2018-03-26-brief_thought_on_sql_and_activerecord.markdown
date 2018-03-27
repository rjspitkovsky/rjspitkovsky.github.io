---
layout: post
title:      "Brief Thought on SQL and ActiveRecord "
date:       2018-03-27 02:45:52 +0000
permalink:  brief_thought_on_sql_and_activerecord
---


After working my way through Object Oriented Ruby and the CLI Data Gem Project I was more than relieved to start the next section, SQL. It was refreshing to be learning a new topic as opposed to the review and meticulous debugging of the labwork I performed in the preceding weeks. 

SQL (I spent a while calling it S.Q.L. instead of sequel) is a language that manages databases. The applications that we build and the world around us is chock full of data so we need to store and manipulate it and that's where SQL comes in. I love SQL. The language is very logical and syntactically sweet. A common SQL query is: SELECT column_name FROM table_name WHERE some_conditions... It just makes sense. 

More importantly, SQL sets you up with the data managing building blocks that lead you into Dynamic ORMs and ActiveRecord. The one word that I kept thinking about when going through these sections is: POWER. These frameworks are so much more powerful than anything we were dealing with before going through the basic building blocks of OO Ruby. If your class inherits from ActiveRecord::Base, you have access to different methods that can associate objects via datbases (databii?). You can create has_many, and belongs_to associations to further connect classes and tables. My eyes were seriously opened by the different things you can do with these tools. And really, those are just building blocks for the real abstract, high level stuff that we will be doing with Sinatra and Rails and all the other stuff my brain can't comprehend just yet. 

In conclusion, the straightforward syntax of SQL and the power of the ActiveRecord inherited classes make this new section of the curriculum extremely interesting and exciting to go through. The amount of fun I have researching and playing around with the code is only exponentially increasing. 
