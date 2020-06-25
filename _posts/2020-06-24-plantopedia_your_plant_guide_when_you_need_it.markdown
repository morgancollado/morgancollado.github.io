---
layout: post
title:      "Plantopedia: Your Plant Guide When You Need It"
date:       2020-06-25 00:14:50 +0000
permalink:  plantopedia_your_plant_guide_when_you_need_it
---

I wanted to do something ambitious for my first project. 

So I turned to my spouse and asked them, "What kind of data app would be helpful to you in your daily life?" 

They responded that having an app that would look up plant information would be extremely helpful to them as a gardener. I set about to do just that. 

I looked up public APIs that might have the kind of data that I was looking for and ran into [Trefle](http://https://trefle.io/). Trefle is an API that takes data from botanical gardens and other sources, presenting them in a RESTful JSON format. I reached out to the developers of the API and they were kind enough to offer code samples that would help integrate the API into my app. 

Once I was able to successfully access the plant data from the API in the terminal through my `APIManager` class, I needed to build out my plant objects. The trickiest part of this was the sheer number of attributes that any given plant could have. There were 77 attributes in all and many of them existed as nested hashes that I needed to iterate over the key values in order to access. The data set from Trefle was also incomplete as the API is still in alpha so for many of the attribute keys that existed their value was nil.

So I need to figure out a way to access the nested hashes while also only returning the values that actually had data. Otherwise, the user would be overwhelmed with a bunch of empty keys that had nothing meaningful and this would make it hard to see at a glance the data that was available. 

So I built my `APIManager` class to only assign attributes to the `Plant` object if such an attribute existed. I did this by using mass assignment and the `.send.` method detect if the key existed and if so to assign that key and value.

I also built a method within the `Plant` class called `full_details` that would output to the terminal the full details of the plant object as available from the data in the API. This was done by iterating over the key, value pairs in the object and using string interpolation to display those elements to the user in an easy to read manner.  Additionally, to compensate for the incomplete data set that many plants had, I used the statement modifier `unless` to keep the terminal from printing any key that had a value of nil.

Once the back end work of building my `APIManager` and `Plant` class was done, I move to building the interface for my app which is housed within an object aptly named, `CLI`. This part required me looking up loops and using a case statement effectively so that the loop would run correctly. Initially, I wrote the loop such that when the user inputted ‘y’ when asked if they wanted to run the program again, it would repeat the first set of instructions. This caused uneven application of the loop and the app would not respond the way that it needed too.

In my instructors office hours, he shared with me that case statements have a key word next that allows you to run the initial set of instructions without having to write them all out again. With this change, the loop ran properly every time and it became predictable and easy to navigate through the app. 

The CLI is also where I wrote the methods to initiate the getting of data and instantiating the objects that would then be presented to the user.

I learned so much about the separation of concerns and how to write clean, dry code from this project. I also learned just how critical collaboration is in software development. I would not have been able to build this alone without the support of my instructor and classmates. I look forward to collaborating with them further to build bigger and better projects in the future. 
