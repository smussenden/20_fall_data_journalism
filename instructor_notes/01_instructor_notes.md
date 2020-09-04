# Session 01 Instructor Notes

### To Have Up on Desktop

1. Session 01 Instructor Notes - X
2. Webpage of roster pictures on UMEG - X
3. Roster sheet with presence - https://docs.google.com/spreadsheets/d/1HKt0Dr6YajcRXLu-0IpWRWBMb4C9J-detlI0TE45jh8/edit#gid=1136077922
3. Course Canvas Page - X
4. Slides https://docs.google.com/presentation/d/1Wol-o16bhaGAbUbd6LmmMrzlFYmOO2sMk-Bu4I4eyWU/edit#slide=id.g6056882942_0_50 X
5. Document What is Data Journalism https://docs.google.com/document/d/14umxQK1mYVqQ6wd7yyTZMEaiM28RLK3bvTfmS8dsj-E/edit# X
6. R Studio with Intro COVID Notebook
7. R Studio HTML output page
8. ZOOM main window. Zoom participants window. Zoom chat.
9. Spreadsheet of roster


#### Introduction

* Welcome everyone to Data Journalism.
* I'm Sean Mussenden, data editor of the Howard Center for Investigative Journalism and a senior lecturer of data and computational journalism.
* A few notes before we get started:
  * Right now, please pull up the chat and just type, I'm here! I just want to figure out who is here.
  * I am recording video and audio of this session, and keeping a record of the chat transcript.
  * Please mute your microphone, unless you're speaking.
  * I encourage you to ask questions as we go! If you have a question you can do one of the following. Please use the type it in the chat or just speak up.  I’ll be stopping at regular intervals to check for questions.   
  * If you have something else you’re working on unrelated to this class, I’d ask you to put it away for now.   

* We're going to go over the syllabus in a bit, and explain this course in detail, but first I want to show you all something that I think will give you a taste of what this course is all about and to show you some of the work you'll be able to do at the end of 14 weeks if you put in the effort in this class.

#### Coding Exercise

###### Setup
* I want you to imagine that you're a reporter for reporter for a national news organization and your editor has given you an assignment: find a place that has been uniquely hard hit by the COVID-19 epidemic and go find a story in that community, using it as a base from which to report out a story on the epidemic.
* You can go anywhere. Where do you go?
* Because you've taken this class, and have some data journalism skills, you want to use data to guide your decision.
* Data is a source. There are lots of sources that power journalism: people, documents, video, audio, pictures.   
* If you wanted to talk to a human source, you’d talk to them on the phone and ask them questions, an interview.  
* We can interview data, too.  But we have to ask it questions in a very particular way to get it to tell us anything.  This class, in many ways, is about figuring how to get data, to ask it questions in the format it desires, and to use that as a jumping off point to find interesting stories.
* Data helps us identify trends, to find characters for our stories, to put what we've learned into context.

###### Introduction
* So, you get some data from the U.S. Census, population data, and data on COVID-19 related deaths and cases, from the New York Times tracking project.
* [PULL UP COVID DATA REPO and NYT PAGE]
* You load it into a program, write some code, and push out this little web page, answering some questions.
* [PULL UP MARKDOWN FILE]
* [WALK THROUGH QUESTIONS]

###### Here's how it was produced
* Here's how it was produced.
* A warning that a lot of this may seem like Greek to most of you now, but give me a few weeks -- and certainly by the end of the semester -- and my pledge to you is that you will come to understand this.  
* This is the first time you're looking something like this, most of you, I'm guessing. I've been teaching this class for years, and trust me, if you take the time to learn this, you will be able to do it.
* You don't need to have ever taken a com sci class.  You don't need to be a math whiz.  You just need to want to do it.  This is not rocket science.
* You don't need to take notes now, this is just to give you a flavor.
* [PULL UP R STUDIO]
* This was written in a language called R, a data programming language.
* It was written inside of program called R Studio, an integrated development environment that helps us load data and explore code.
* It was written in a specific kind of file, called an R markdown file, that combines text and code.
* [WALK THROUGH HOW IT WORKS. Load data]
* I wrote this script to ingest data from the census and the New York Times.
* [SHOW ONE EXAMPLE of A dataframe].
* We can explore it like a spreadsheet.
* Some of you may be wondering: why aren't we just using spreadsheets.  
* The answer is: spreadsheets are messy, and not particularly reproducible, and transparent.  If you make a mistake when editing a spreadsheet, it's hard to go back and fix it if you don't notice it until later.  Plus, learning how to do this sets us up for even more challenging work in the future.
* [SHOW CODE BLOCKS]
* [SHOW FIRST ONE]
* We write code, and run it, and look at the results.
* By the end of the semester, you all will be doing this like champs, I promise.

#### What is Data Journalism Exercise?

##### Group exercise
* So, this class is what is data journalism? What do we mean by data journalism?
* It turns out that if you ask 10 people who do data journalism what data journalism is, you'll get 10 different answers.
* We're going to do a small group exercise.  I want to find out what you think it is, and then I'll share my definition.
* [PULL UP GOOGLE DOC, SHOW HOW TO FIND IN ELMS]
* BEFORE we create the rooms, does everyone have access to the doc.  Please type in the chat when you have it.
* [ASSIGN PEOPLE TO ROOMS]

##### My Definition
 * Transparency.  We are open about how we did our work and we freely share it and document it.  People don't trust journalists, and you can't just drop a story based on data analysis without backing it up. This is why I love these data notebooks.
 * Analysis.  Sometimes this means computing fancy statistics, and using advanced machine learning.  But sometimes it literally means finding one tiny bit of information scanning through a spreadsheet, and using that as a foundation for further reporting.
 * Digital Information. There is so much data in the world.  Stored in many formats.  Some of its structured, in spreadsheets. Some of its big huge bodies of dumped documents.  Sometimes it's Tweets or scraped web pages.
 * Reporting: It's not a separate thing from the reporting process.  It's part of the process. If you want to learn this because you never want to interview a human again, I have bad news for you.  Context.  Methods. Checks.  We'll talk again and again about that in this class.  Data journalism is part of the reporting process.  It doesn’t stand apart from it.  We need to talk to people, to human sources, to convince them to give us data, to make sense of data, to figure out what questions to ask, and to make sure our answers are correct. And, on their own, our data findings aren’t stories.  We need to bring our data findings to life by finding characters, doing contextual reporting and engaging in good-old-fashioned storytelling.  
 * Meticulous. We always assume we are getting something wrong, and set out to prove ourself wrong. This means getting obsessive about how we look at data.  
 * Community.  The growing group of people who do this work help each other, share data, share information.  NICAR and IRE. We'll get connected to some of these groups as part of this class.
 * Facts, Patterns, and Proof and Examples: data journalism is great for both establishing a pattern that forms bones of a story -- a pattern showing opioid deaths increased in counties the most where drug companies sent the most pills -- and identifying anecdotes -- the pharmacy in the county in West Virginia with the highest death rate that received the most pills.  It's great for finding characters.  It's great from waving us off of stories that aren't meaningful.
 * Stories: Our goal is to tell stories, not to present a bunch of data and say "look at this data".  That can happen in lots of forms, including text, graphics, video, podcasts, social platforms. We'll talk a lot about this.

##### Introductions
* What's your name, and is it different than what's on your zoom name.  
* Tell us why you're interested in learning about data journalism, and how do you hope it will help you after you graduate.  If the answer is: I needed a class and this fit in my schedule, that's FINE by the way.  

##### Syllabus review
