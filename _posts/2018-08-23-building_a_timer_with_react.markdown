---
layout: post
title:      "Building a timer with React"
date:       2018-08-23 17:53:41 +0000
permalink:  building_a_timer_with_react
---


I was recently tasked with building a timer using React. The timer had to have the following specifications: When a button is clicked the timer starts. When the button is clicked again, the split time gets added to an unordered list on the page. When a split time is clicked, the timer is reset to that split time, the split time is highlighted, and higher split times are removed from the page. 

I initially broke this assignment down into three seperate issues. The first was handling the starting and stoping of a timer. The second was shifting the responsibility of the button. The third was giving the split time the desired functionality when it was clicked. I needed to take a step back and realize that all of these issues were connected with one another. I needed these responsibilities to talk to each other. 

The biggest pickle I found was giving the button two seperate responsibilites for the same click event. When the timer is "off", the button starts the timer on click. If the timer is ongoing, the button adds the split time to the page. I gave the Timer component a state attribute, ```status``` which I passed to the Button component as a prop. I also passed two functions--one to handle the starting of the timer when ```this.props.status``` was "off", and one to collect split times when ```this.props.status``` was "on". When the timer is off, the button click event changes ```this.state.status``` in the Timer component to "on", then starts an interval, which adds one to ```this.state.seconds``` every second. I am displaying ```this.state.seconds``` in the JSX so each change in that value is visible on the page. If ```this.state.status``` is "off" the interval is cleared, pausing the timer. Stopping the timer after its reset was another issue I faced but found a solution by connecting it to the component's state. 

When the button is clicked and the timer is off. 

```  sendStatusToTimer = () => {
    if (this.state.status === "off") {
      this.setState({status: "on"})
    }
    else {
      this.setState({status: "off"})
    }

    var nextSecond = this.state.seconds
    var startTimer = () => {
      this.state.status === "on" ? this.setState({seconds: nextSecond++}) : clearInterval(myInterval)
    }

    var myInterval = setInterval(startTimer, 1000)
		
		
    ...
		
		
  }
	```
	
	When the timer is on, another function is triggered on the click of the button. This adds the current value of ```this.state.seconds``` to ```this.state.clickedSeconds```,  which is an array that collects the split times. This array is then passed to the UnorderedList component. The UL component is tasked with rendering each split time as list items in the ul as well as giving each one the desired onClick functionality. The first thing a clicked split time should do is get highlighted-- I simply added a class to the event.target (which is the <li>{split time}</li> that's been clicked) that changes the background color. I then collected all of the list items, iterated through them (using Array.prototype.map.call()) and then removed the list items whose innerText was higher than the innerText of the event.target. Then I called a passed down function from the Timer component whose responsibility is to change ```this.state.status``` of the Timer component back to "off". This clears the interval that is in charge of our timer. 
	
	The click event handler that all dynamically created li's have. 
	```
	  resetTimer = (event) => {
    event.preventDefault()
    event.target.className = "clicked"
    const splitTime = Number(event.target.innerText)
    const lis = document.getElementsByTagName("li")
    Array.prototype.map.call(lis, li => {
      for (let i = 0; i < lis.length; i++) {
        const li = lis[i]
        if (li.className !== "clicked" && splitTime < Number(li.innerText)) {
          document.getElementById("splits").removeChild(li)
        }
      }
    })
    this.props.sendStatusToTimer()
  }
	```
	
	The final thing I needed to do was to reset the timer to whatever the value of the clicked split time was. I did this in the Timer component. I collected all the elements on the page that had a className of "clicked". I got the value of the last "clicked" element and then changed ```this.state.seconds``` to that value. 
	
	```  setSecond = () => {
    const clickedLength = document.getElementsByClassName("clicked").length
    if (clickedLength > 0) {
      var clicked = Number(document.getElementsByClassName("clicked").item(clickedLength - 1).innerText)
      this.setState({seconds: clicked})
    }
  }
	```
	
	It was a really cool feeling to get all the parameters of the assignment passing. I came across a number of tricky moments -- getting different functionality on the same click, appropriate starting and stopping of the timer, and removing higher, unclicked split times. I'm sure there are more efficient, syntactically sweeter ways to accomplish the goal and I welcome any suggestions from those who read the post. But taking a step back, breaking down your assignment into smaller issues, then realizing where and how your components were going to talk to each other to achieve your functionality---these are all things I did for this assignment, and steps I can build off of for future projects. 
	
	


