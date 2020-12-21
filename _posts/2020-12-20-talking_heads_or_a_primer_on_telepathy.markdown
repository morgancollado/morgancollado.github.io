---
layout: post
title:      "Talking Heads or a Primer on Telepathy"
date:       2020-12-21 03:05:38 +0000
permalink:  talking_heads_or_a_primer_on_telepathy
---

In essence, this was two projects in one.

For our 4th Flatiron project, we were tasked with building a Single Page Application with a relatively simple object model relationship using object oriented Javascript as the front end and Rails as the backend. I opted to create a make up review site named Aphrodite’s Mirror. A user should be able to go to the website, create new make up and other users can leave reviews of their experiences on any make up that any user has created. This way, knowledge of products can be crowd sourced and a discerning make up shopper could use my website as a reference when deciding on what to buy. 

I had to fully design the front end of my application using HTML, CSS and Javascript. After operating in the opinionated constraints of Rails for so long, it was jarring to suddenly find myself with so much freedom in regards to how to structure my app. As long as my Javascript and CSS files were linked to my HTML file, how exactly they handled the users input to implement the backend logic is entirely up to me. I found myself in the early parts of the development process overwhelmed because I had so many features that I wanted to build but I still lacked the experience to fully realize my vision. 

I talked things through with my spouse who is the designer of all the apps I’ve built thus far and brought it back to basics. I just need some data stored somewhere(my rails back end) and a front end application that renders that data and allows the user to manipulate that data (my javascript, html and css front end). 

What struck me most during my building of this app was how specific one needs to be in order to get these two software programs to correctly speak to each other. The language that these two systems speak in common is Javascript Object Notation or JSON. Rails renders to the API endpoint the data that exists within the database as JSON. The front end then unpackages that JSON and displays it to the user. In order for my front end to know what parts of the data to display, how to display and when, I must be very particular about what key exists within the JSON to get the value that I need. 

Debugger was my best friend in tracking down which keys lead to which values within the returned JSON object. Writing my code in an object oriented manner also made it much easier to track down where in my program the data was either being missed or called on incorrectly. Being able to call on `makeup` and have it tell me all it secrets made it possible for me to track down all the ways that my program was manipulating and changing that object. It made it possible for me to ensure that the data was being manipulated in a way that made sense and produced the result I was looking for. 

It is this abstraction that allows software engineers to create experiences that surprise and delight our users. But at the end of the day, it’s not magic making these things happen behind a curtain. Its science. More specifically, it is the science of turning human thought into math and using the power of electricity to transmit these thoughts across great distances. While we may not divulge our secrets to our users on the surface, one has just to right click + inspect and laid bare are the guts of our program for any to examine.

Every time I complete a project I am reminded of how much left I have to learn and how excited I am to continue on this journey. 
