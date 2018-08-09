---
layout: post
title:      "Stacks & Queues "
date:       2018-08-09 16:22:32 +0000
permalink:  stacks_and_queues
---


As I am preparing for the technical interviews coming my way, one of the key fundamental concepts I've been reviewing is data structures.  Knowing different data structures, when they should be used, and the different ways to return the desired data from them is critical in programming. I understand that this is something asked often during the interview process so I've decided to make studying this a top priority. 

Stacks & Queues did not really come up through the Flatiron curriculum which is why it's especially important to go over them after you've completed the course. I'm going to briefly go over Stacks & Queues mostly for my own review, but if you have no idea what I am talking about yet, hopefully you'll get a slightly better understanding or introduction on important concepts. 

# Stacks 
A stack is a data structure that you can think of as a stack of plates from the dishwasher. You take the first plate and put (push) it into the cupboard. You take the second plate and do the same thing until all the plates are stacked on top of one another in the cupboard. When you want to put food on a plate, the only plate you can access is the last plate you pushed on to the stack. This demonstrates the concept of LIFO (last in, first out) and it is a major component of what makes a stack a stack. Manipulating a stack requires much more specificity than a normal array so they are harder to tamper with and have your data behave against your programming wishes.

The major operations that a stack can support are: pushing an item onto a stack; popping the top item from the stack and displaying the entire stack (pip). 

# Queues
The same strict manipulations that make a stack a simple and attractive data structure to use also apply to queues. If you are walk up to a line to enter a club you wait in that line until the people in front of you are let in. Then when you are at the front of the line it is your turn to make small talk with the bouncer while he deeply examines a crappy picture from years ago and--- sorry, where was I? Anyway, a line is an example of the concept of FIFO (first in, first out). The data in your queue is examined based on the first data that was placed there. Data elements are still placed at the end of the line but they are not the first to be examined like it would be in a stack. Like pushing into a stack, you can enqueue an item into a queue. Dequeuing an item is to remove that item from the front of the queue. 



Handling data should be on the Mt. Rushmore of responsibilities that a programmer has to write an efficient, abstract program. Stacks and Queues are two data structures that help handle your data in a particular way--LIFO or FIFO. There is always more to study and review but I think it is important to know that not everything is stored in an array or a hash. There are many more ways to store and access data and they can be more efficient and suit the needs of your program better than the basic data structures we went over in the Flatiron curriculum. Happy learning!
