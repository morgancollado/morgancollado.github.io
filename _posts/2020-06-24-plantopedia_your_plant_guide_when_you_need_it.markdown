---
layout: post
title:      "Plantopedia: Your Plant Guide When You Need It"
date:       2020-06-24 20:14:51 -0400
permalink:  plantopedia_your_plant_guide_when_you_need_it
---

I wanted to do something ambitious for my first project. 

So I turned to my spouse and shared with them the requirement for the project. They came up with several ideas but we landed on an app that would look up plant information. As gardeners, we both could use something that can look up plant data in a snap.

I looked up public APIs that might have the kind of data that I was looking for and ran into [Trefle](http://https://trefle.io/). Trefle is an API that takes data from botanical gardens and other sources, presenting them in a RESTful JSON format. I reached out to the developers of the API and they were kind enough to offer code samples that would help integrate the API into my app. 

Once I was able to successfully access the plant data from the API in the terminal through my `APIManager` class, I needed to build out my plant objects. The trickiest part of this was the sheer number of attributes that any given plant could have. There were 77 attributes in all and many of them existed as nested hashes that I needed to iterate over the key values in order to access. The data set from Trefle was also incomplete as the API is still in alpha so for many of the attribute keys that existed their value was nil.

So I need to figure out a way to access the nested hashes while also only returning the values that actually had data. Otherwise, the user would be overwhelmed with a bunch of empty keys that had nothing meaningful and this would make it hard to see at a glance the data that was available. 

So I built my `APIManager` class to only assign attributes to the `Plant` object if such an attribute existed. I did this by using mass assignment and the `.send.` method detect if the key existed and if so to assign that key and value.

I also built a method within the `Plant` class called `full_details` that would output to the terminal the full details of the plant object as available from the data in the API. This was done by iterating over the key, value pairs in the object and using string interpolation to display those elements to the user in an easy to read manner.  Additionally, to compensate for the incomplete data set that many plants had, I used the statement modifier `unless` to keep the terminal from printing any key that had a value of nil.

Once the back end work of building my `APIManager` and `Plant` class was done, I move to building the interface for my app which is housed within an object aptly named, `CLI`. This part required me looking up loops and using a case statement effectively so that the loop would run correctly. Initially, I wrote the loop such that when the user inputted ‘y’ when asked if they wanted to run the program again, it would repeat the first set of instructions. This caused uneven application of the loop and the app would not respond the way that it needed too.

In my instructors office hours, he shared with me that case statements have a key word next that allows you to run the initial set of instructions without having to write them all out again. With this change, the loop ran properly every time and it became predictable and easy to navigate through the app. 

The CLI is also where I wrote the methods to initiate the getting of data and instantiating the objects that would then be presented to the user. I also ran up against the problem communicating the input from the initial method that created a list of plants and the method that would flesh out that plant object with all the details that it needed. I was able to solve this by taking the input from the user and translating that into another index variable that could then be inserted in the second method which assigned all the remaining attributes appropriately. 

Finally, I used a ruby gem Colorize to make the interface more readable. With my spouse's design acumen, we were able to select colors for each string that made it really pop and easy to read. 

I learned so much about the separation of concerns and how to write clean, dry code from this project. I also learned just how critical collaboration is in software development. I would not have been able to build this alone without the support of my instructor, classmates or my spouse. I look forward to collaborating with them further to build bigger and better projects in the future. 
