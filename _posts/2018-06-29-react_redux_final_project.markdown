---
layout: post
title:      "React/Redux Final Project "
date:       2018-06-29 23:21:23 +0000
permalink:  react_redux_final_project
---


Time flies when you're having fun, doesn't it? I can't believe that I am about to submit my final project for the Flatiron School. It has been a huge success and my confidence in my ability to program is definitely high right now. This project, even more than the others, made me feel like no matter what the issue is that I'm dealing with in my code, I WILL eventually find the solution. I will debug, and search error messages, and examine my code line by line, and eventually I wil get the functionality that I desire. I've come a long way from the initial feelings of hopelessness when I didn't immediately understand why my code wasn't working. 

My app is called Sports Predictions! It is a place to post your predictions about sporting events yet to occur. When they are proven right, they can be marked as such; if they are proven wrong they are also marked (but those ashamed of truly terrible predictions can delete those). The app complies with CRUD-- you can create a prediction, read all or a single prediction, update a prediction and delete a prediction. 

I used react-router to set myself up with multiple routes, with RESTful architecture and then added routes so that predictions can be filtered by whether they were correct or (hilariously) wrong. I set up my rails backend by creating a database, creating routes with an '/api' scope and creating a controller that will render the requested information in a JSON format. 

My front-end is initialized with the store, which has a rootReducer--that reducer uses combineReducer with my predictionsReducer. The predictionsReducer has two cases for the action.type: 'LOADING_PREDICTIONS' clears the state and 'FETCH_PREDICTIONS' adds the predictions to the state. The predictions that are being added (all, correct, or wrong) is determined by the component that is calling the dispatch action. That way the logic is removed from my reducer, and my action is also abstracted. 

After I've called the 'FETCH_PREDICTIONS' action, my state is filled with predictions-- I then use mapStateToProps to allow my components access to those predictions, and I iterate through the array of predictions and place each prediction in a Prediction component. The Prediction component is a stateless functional component that renders the content, sport, and status of each prediction along with the applicable buttons for the prediction. If a prediction's status is undetermined, buttons to update it to correct or wrong are displayed; if a prediction is wrong, a button to delete the prediction is displayed, and if a prediction is correct we assume that the poster would want it displayed and no button is visible. 

As I wrap up my time as a student in the Flatiron School I am thrilled with my progress. I can confidently say if I need to build a project in Sinatra, or Rails, or using jQuery, or including client-side programming like React/Redux, that I will be able to do that. It absolutely won't be easy---that will come with more and more practice, but I have the skills, dedication, and confidence to get the job done. The first and last of those, come directly from the school. 
