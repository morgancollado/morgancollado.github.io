---
layout: post
title:      "Sinatra: The Best is Yet to Come"
date:       2020-08-22 21:58:45 +0000
permalink:  sinatra_the_best_is_yet_to_come
---


This project was my first foray into full stack web development. While my first app is simple in design, it provides some of the most basic functionality that the Internet provides. Namely the ability to send messages across the web to be saved into a database and then reproduced for someone somewhere else. This magic is what has kept our world spinning through the pandemic and has offered a life line to so many people stuck in isolation even before COVID struck. It was access to this technology that kept me alive when I was younger and it is a marvel that I can now build it myself. 

Constructing the logic for this project was much easier then it was for my CLI app. This is because Sinatra and ActiveRecord have so many short cuts built into it that allow one too quickly and easy create models, controllers and views. 

ActiveRecord gives you the short cuts to create relationships between your models. I was able to create aliases for my models, making one model flexible enough to play two roles in their interaction with the other models. It was fascinating to set up foreign keys in my ticket model/database and use those keys to create a customer user sub class and an admin user sub class. In fact, both the Ticket class and the User class had aliases, submitted tickets that come from a customer and worked tickets that come from an admin, and this allowed me to keep my code DRY and flexible so that the relationship between allowed a customer to edit only their tickets and an admin can respond to and edit all tickets. All of this done with a few lines of code. Most of it was already written by the devs who make ActiveRecord.

Building the controller actions is simplified due to RESTful conventions. The routes operate the same across the industry, the only thing that changes is the specific views rendered and words associated with your particular app. 

 I even used software to build the file structure for my app with the Corenal gem. 

 Metaprogramming at its finest.

The hardest part for me was writing the HTML and styling the page with CSS such that it looked the way I wanted to. With the keen stylistic eye of my spouse, I used a CSS library called Bootstrap that has CSS already written and documentation established such that I only have to tag my HTML appropriately so that the style rules apply correctly. 

What strikes me here is that there is so much code that we do not write ourselves that makes our lives easier. I knew on some level that developers had access to tools that would make software development easier but it really hit home on this project just how dependent we are on each other. If I had to write all the code in my project by hand, it would have taken me many more weeks. There is something to be said about bespoke code written entirely from scratch as you will be infinitely more familiar with how it works and thus how to extend and debug it, however, the time saving nature of these tools make them too good to pass up.

Whenever I use metaprogramming, I need really dig deep to make sure that I know what is happening under the hood. There is still so much that I do not understand and while these shortcuts can be helpful it can obscure how the code works which defeats the purpose of being in school. While magic is great, it is much more useful and gratifying to know how the technology works. 

This is just the beginning of my journey as a software developer and I am so excited for what is to come. 
