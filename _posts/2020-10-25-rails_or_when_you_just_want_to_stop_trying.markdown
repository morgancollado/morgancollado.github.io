---
layout: post
title:      "Rails, Or When You Just Want To Stop Trying"
date:       2020-10-26 02:57:26 +0000
permalink:  rails_or_when_you_just_want_to_stop_trying
---



Rails is an extremely powerful, flexible and sprawling software framework that allows a developer to get the basic structure of a web app created in very little time. Its purpose is to make a decision about how such a method should function, make that decision for everyone who develops on the same framework and thus allow the developer to focus on what really matters in the app. It frees up the developer to create fantastic solutions to very specialized and unique problems because the decision about how to structure the database, which is necessary for every modern program, has already been made. It makes space to push our craft forward because we really don’t need to reinvent the wheel every single time. 

At its heart, Rails is about the idea that together we do better work. By developing a shared language, a shared technique at building software, we can help each other push technology forward with our collective vision. This toolkit allows us to develop deeper abstractions, making our software more powerful and adaptive. This ability to create by convention, however, can lead to an obfuscation of what is really happening. If you don’t know what’s going on under the hood, it can be difficult to track down an issue when things break. On the other hand, this shared language allows us to communicate with each other must more quickly and it makes is easier to learn from one another.

I really enjoyed developing on Rails and for the first time I realized the scope of a software engineer’s work. These are complex systems that interlock in very particular and specific ways. Time and again it was the details that made or broke my program. A missed placed comma here, a forgotten quotation mark there, and everything grinds to a halt. But when it works - when the wires are aligned just so and you move through your application like water - the feeling is simply sublime. 

One particularly challenging part of this project was integrating Omniauth. Each bug I encountered was quashed after a careful revision of how I had built the connection between the two machines. At first, my app did not know where to send the user when they clicked the sign up with GitHub link. When I checked the settings in GItHub, I had written http://localhost:3000/`APP`/github/callback instead of what should have been http://localhost:3000/`AUTH`/github/callback. So my app was receiving the Omniauth hash from GitHub but the path that GitHub had was incorrect so my app could not match the route. The app had no way of knowing what controller to route that request nor how to process the data received. 

It took me the better part of a week to get it functioning properly. Making my way through each and every bug was a slow, methodical and at times agonizing process. I didn’t even have time to really style the front end of my app because it took me so long to just make a functioning product. It helped me understand that the job I’m signing up for requires tenacity and a thirst to solve problems. To really dig deep and understand how things function.

A typical Software Engineer wants her app to be so successful that it is played by billions of people. She wants it to impact culture and change people’s perspective on an issue. Rails allows us to join a community of developers who can help make this possible. Any wrong keystroke can stop even the most finely tuned machine and this is not a problem that can be solved through brute force methods alone. Interdependence is built into success; every time we reach out with a question we are giving ourselves and others the opportunity to get the perspective we need to solve the problem. Even when we are banging our heads against the table and wishing for a breakthrough, we are in control. 

There is always a way forward. 

We just need to keep trying. 
