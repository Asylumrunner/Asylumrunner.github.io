---
layout: page
title: Portfolio
permalink: /portfolio/
---

## [Maskmaker](https://github.com/Asylumrunner/Maskmaker)

*Key Technologies: Node.js, Express, Docker, AWS (Lambda, API Gateway)*

I run a number of tabletop role-playing games (such as Dungeons and Dragons) for a variety of groups, and one of the hardest parts for me is coming up with distinct personalities for non-player characters (NPCs) on the spot. So, I decided to write myself an application that could automatically generate NPCs, at least in the broad strokes, on my behalf.

Maskmaker is an API, created with the Express framework for Node.js and hosted via AWS Lambda, which generates non-player characters on the fly, including the ability to generate unique names via Markov Chain. I then consume this API using a series of customized, dockerized Discord bots, each customed tuned to the particular game I am playing, which use the Maskmaker API alongside some basic dice-rolling functionality to assist me while running tabletop RPGs.

## [Cast Through Time](https://github.com/Asylumrunner/CastThroughTime)
#### Completed Webpage Viewable [Here](https://www.castthroughtime.com)

*Key Technologies: React, Redux, Python, Flask, AWS (Amplify, Lambda, S3, API Gateway)*

I recently restarted playing the tabletop card game _Magic: The Gathering_ after an almost decade-long hiatus, and discovered that while there were many resources available to help brand new players learn how to play the game from zero, there were seemingly no resources for helping a returning player "catch-up", allowing them to focus on learning changes to the game which happened since the last time they played. So, I decided to build such a site myself.

Cast Through Time is a one-page application in which a user inputs the last time they played _Magic_, and recieve a personalized set of quick-blurb recaps of changes to the game since they last played. The page recieves data through a Flask API written in Python, which also uses a third-party API to ensure it itself remains updated with data about the latest changes to the game. The site focuses on delivering the minimum amount of information in a digestable format which would allow players to quickly return to playing the game with confidence.

## [Spanish Conjugation Trainer](https://github.com/Asylumrunner/spanish-trainer)
#### Completed Webpage Viewable [Here](https://www.espanolverbconjugator.com/)

*Key Technologies: React, Redux, Vite.js, Python, Flask, AWS (Amplify, Lambda, API Gateway)*

Following a (delightful) trip to Mexico City, I've been trying to improve my knowledge of Spanish, specifically my number of known verbs and my ability to conjugate those verbs into various tenses. My normal Spanish practice regimen, mostly involving decks of flashcards on top of practice reading, writing, and speaking, is uniquely unsuited for the infinite configurability of verbs, with the combination of tense, mood, and subject allowing for dozens of permutations on a single verb. Thus, I decided to build a web application to act as my "flashcards" for verbs.

The Spanish Conjugation Trainer is a one page app that allows the user to practice their proficiency with Spanish verbs in two modes: Flashcard Mode, which simply asks the player to translate infinitive-form verbs from Spanish to English and back, and Conjugation Mode, which asks players to take a verb, a mood, a tense, and a subject, and correctly conjugate the verb. Score is tracked over a session of play, and a history is kept of answered questions allowing players to review what they've practiced in a session. The page receives conjugation data from a lightweight Python API hosted on Lambda and accessible via API Gateway, relying on [Fred Jehle's Conjugated Spanish Verb Database](https://github.com/ghidinelli/fred-jehle-spanish-verbs), a very helpful store of hundreds of Spanish verbs and all of their conjugations.

## [Collection Manager](https://github.com/Asylumrunner/CollectionDatabase)

*Key Technologies: Python, Flask, DynamoDB, AWS Lambda*

Like a lot of people with nerdy sensibilities, I own a lot of physical media, from video games to movies to books to tabletop RPGs to board and card games. I've found that having a large digital record of this collection is fairly useful for a variety of reasons, so I built this Collection Manager to help me manage a simple database on the cloud which stores all of the information about my physical collections, recently useful for keeping inventory of stuff during large-scale moves.

The collection is stored in DynamoDB as a NoSQL database, which in turn is managed by an API built in the Flask framework for Python which allows me CRUD operations on this dataset. The API also hooks into a variety of external APIs which allow me access to large-scale datasets for books, movies, video games, etc, which allow me to rapidly populate database information based on just a title alone. 

## [Dallas Concert Scraper](https://github.com/Asylumrunner/DallasConcertScraper)

*Key Technologies: Go, AWS (Lambda, Simple Email Service)*

While I was living in Dallas, I found myself frustrated by not knowing what shows were playing where and when, and the larger show-aggregation services like bandsintown tended to heavily focus their messaging on arena-scale shows, whereas I was looking for smaller, indie shows at proportionally smaller venues. To remedy this, I built this web scraper in Go, hosting it in AWS Lambda and running it based on a timer, to scrape the calendar pages of music venues I enjoyed, collating their calendars together into a single list, using Spotify's API to add links for the artists so I could sample their music (if they were on Spotify), and then emailing the total list to myself for my convenience.