---
layout: page
title: Portfolio
permalink: /portfolio/
---

## [Maskmaker](https://github.com/Asylumrunner/Maskmaker)

*Key Technologies: Node.js, Express, Docker, AWS Lambda, AWS API Gateway*

I run a number of tabletop role-playing games (such as Dungeons and Dragons) for a variety of groups, and one of the hardest parts for me is coming up with distinct personalities for non-player characters (NPCs) on the spot. So, I decided to write myself an application that could automatically generate NPCs, at least in the broad strokes, on my behalf.

Maskmaker is an API, created with the Express framework for Node.js and hosted via AWS Lambda, which generates non-player characters on the fly, including the ability to generate unique names via Markov Chain. I then consume this API using a series of customized, dockerized Discord bots, each customed tuned to the particular game I am playing, which use the Maskmaker API alongside some basic dice-rolling functionality to assist me while running tabletop RPGs.

## [Collection Manager](https://github.com/Asylumrunner/CollectionDatabase)

*Key Technologies: Python, Flask, DynamoDB, AWS Lambda*

Like a lot of people with nerdy sensibilities, I own a lot of physical media, from video games to movies to books to tabletop RPGs to board and card games. I've found that having a large digital record of this collection is fairly useful for a variety of reasons, so I built this Collection Manager to help me manage a simple database on the cloud which stores all of the information about my physical collections, recently useful for keeping inventory of stuff during large-scale moves.

The collection is stored in DynamoDB as a NoSQL database, which in turn is managed by an API built in the Flask framework for Python which allows me CRUD operations on this dataset. The API also hooks into a variety of external APIs which allow me access to large-scale datasets for books, movies, video games, etc, which allow me to rapidly populate database information based on just a title alone. 

## [Dallas Concert Scraper](https://github.com/Asylumrunner/DallasConcertScraper)

*Key Technologies: Go, AWS Lambda, AWS Simple Email Service*

While I was living in Dallas, I found myself frustrated by not knowing what shows were playing where and when, and the larger show-aggregation services like bandsintown tended to heavily focus their messaging on arena-scale shows, whereas I was looking for smaller, indie shows at proportionally smaller venues. To remedy this, I built this web scraper in Go, hosting it in AWS Lambda and running it based on a timer, to scrape the calendar pages of music venues I enjoyed, collating their calendars together into a single list, using Spotify's API to add links for the artists so I could sample their music (if they were on Spotify), and then emailing the total list to myself for my convenience.