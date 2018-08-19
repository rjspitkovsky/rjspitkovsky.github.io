---
layout: post
title:      "Time C(O)mplexity"
date:       2018-08-19 23:57:21 +0000
permalink:  time_c_o_mplexity
---


Time complexity is one of the most important computer science concepts to understand and try to apply when building out your own programs. As I am gaining experience I am not just trying to build something that works but am trying to write programs that consider time complexity and the benefits of efficiency. 

But what exactly is time complexity? Very simply, it is the analysis of an algorithm based on how fast it takes to run, with the size of the input to the algorithm being a huge factor in that calculation. 

Why the heck is any of this important? The algorithms that we write in functions can sometimes be simple--but they can also be complex and they may involve handling an incredibly huge amount of data. You want to implement the most efficient way to return the information you seek-- the faster your function does this, the faster your entire program will run. The speed at which your program runs may be a determining factor in whether or not a user is satisfied. So, you definitely want to keep efficiency in mind when you're coding. 

Big O notation is used to express efficiency. The reason we use O is because the Order of the function is a mathematical term to refer to the functions growth rate (how fast the function runs when its input grows). Anyway, the point is that we use the big O. A function that removes the first element of an array and returns it ```array.shift``` , is O(1), or constant time, because the function does not need to go through the entire array, it just acts on the first element. 

Consider this. Let's say you had an array of integers and we wanted to return an array that squares the integers. [1,2,3] => [1,4,9]. We could write it like this:
```array.map{|i| i ** 2}```
This function is in linear time, O(n), where n is the size of the array. As the array grows so does the time it takes to complete the function because each element needs to be acted on. 

Another example is when you have a large sorted array of integers and you have a target integer you are trying to find. One method you can use is to find the middle integer, and determine if the target integer is higher or lower than that value. You can then remove the side the target value isn't in. Then repeat the process by finding the middle integer between the first integer and the middle, which is now the top (assuming the target integer is less than the middle integer of the array), and then making the comparison again. Eventually you will find your target integer by these comparison checks. This type of function is in logarithmic time, or O(log n), where n is the size of the array. 

Again, time complexity is not the simplest concept to tackle but it is crucial in learning to build lean and efficient programs, which is one of the major components of being a great programmer. As I continue writing programs, I will first try to get the functionality I am looking for, and after doiing so, I will try to determine if there is a more efficient way to get that same functionality. And if there is, I'll implement that way. That is my path to progressing as a programmer who applies the idea of time complexity. 

