---
toc: true
layout: post
description: Project DOVE was built for the 2020 HackAPI. It's a web app that scraps Twitter for news, filters it and displays it.
categories: [blog, hackathon]
title: Project DOVE
image: /images/project-dove/dove-screen.PNG
---

In December 2019, I participated in a hackathon organized in Ashesi: the [HackAPI](https://twitter.com/hack_api). This article will explain the solution my team built.

## What is project Dove?
> "According to the biblical story (Genesis 8:11), a dove was released by Noah after the flood in order to find land". 
>> https://en.wikipedia.org/wiki/Doves_as_symbols


Similarly, the team I worked with for the 2019 HackAPI decided to send doves on twitter to let us know what is going on. To be a bit more explicit about the product we developed, Dove is a platform that scraps Twitter to find tweets relative to disasters in various locations, mainly floods. 

The intended use is mostly information sharing. The motivation for using Twitter is the speed at which information spreads on this particular social network, often preceding traditional news platforms. Dove filters and organizes information from Twitter and displays it in a more digestible way, using a map.

## How we built it?
Dove is a web app with three main components: a database, a script for scraping and analyzing text and a frontend.
### Database
The database is a simple MongoDB database hosted on mlab.com. It stores information about tweets such as the links, location, the time it was scraped, and the text of the tweet. This information is what the frontend will display to the user. 
### Frontend
We built the frontend as a single page app with React, which fetches the tweet data directly from the database. This app will then display the information on a map and a feed for the corresponding locations.
### Backend script
Then there is the backend script which scraps Twitter for new tweets using pre-defined keywords and locations. For each tweet, the script will use a logistic regression model to determine how likely it is that the tweet is about a disastrous event. If the probability is higher than a pre-defined threshold, the data is sent to the database.

I think it is interesting to note that by tuning the probability threshold, we can decide how much data we are letting in. The search keywords and locations can also be edited to reflect ongoing events. 

## What does it look like?
To explain what a project is about, talk is cheap, and a video is worth more than a thousand words. Here is a video where I demo the platform.

<iframe width="560" height="315" src="https://www.youtube.com/embed/c8n53Zhl4TM" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>