VIDEO.
Video 1.
#### VIDEO TEXT

For now, let's look at the table.  It's pretty messy:

* The column names are very complicated.  
* It's got a blank row in the middle, plus a row with a bunch of meaningless text.
* Half of the death rate values have an asterisk, instead of being a proper N/A value.
* It's got a blank row in the middle, plus a row with a bunch of meaningless text.
* Half of the death rate values have an asterisk, instead of being a proper N/A value.
* The death rate values are characters, as are opioid rates.
* There's an N/A value in the state column.

It will prevent us from answering questions.  

```{r}
opioid_scrape %>%
  summarise(avg_death_rate = mean(`Opioid.Prescriptions.100.persons2..2018`))

```


# JOINS


1. SUN-SENTINEL

* Review findings
* I love this story, because it's not like there was some magic data set of cops speed.  Like, there wasn't a transponder in cars that reocrded devery time they speed.
* They had to get creative.
* Realized sunpass tolls data is public. Realized they could get list of sunpass ids from each agency.
* And then had to build data set of location.   
* As data journalists, we often need to think about how we can use data that was captured for some other purpose entirely to answer questiosn we want to answer.  
* And if we put them togethe rin creative ways, WOW.


Data set one.  
* Had data showing sun pass ids, time it went through different toll plazas.  Used that to calculate time it took for cops to go through two different toll plazas.
* Built their own data set of distance between two toll plazas and joined them together.  
* Joined them together. Divided time by distance to get speed.

2. Review lab, show what happens when you join one to many. MAKE a little example.

## Upcoming Stuff

# Data Acquisition
1. Data memo due Sunday -- show link
2. NEXT WEEK Week 9 Presentation (Lightning Talk) - 10 percent
In week 9, you will update the class verbally on two things in a presentation with a hard cap of three minutes:
* Where your data request stands. Have you obtained the data? If not, why?
* Tell us a brief story about a single part of the data acquisition process, and the lesson you learned from it that you think is worth sharing from the class.

2. Set up time to meet with me as a group.
3. Lab setup -- data cleaning. Show common errors.

# Data Analysis
1. I'll be giving you feedback on work you've done so far.  
2. Set a time to meet with me THIS WEEK to go over results.  THURSDAY or FRIDAY afternoon.
3. Not this Sunday, but next Monday, final notebook PLUS critical analysis memo. Note that as part of this, you will need to reach out to the reporters to ask the some questions.  So, I wouldn't wait on that!
4. And not next class, but the class after, you'll have a presentation and a code walk through!   

## Data Cleaning

* ALWAYS assume your data is flawed, deeply.
* Data is often entered by humans, which means it's error prone.
* We spend 90 percent of our time cleaning data.
* Failure to clean data can lead to inconsistent results.
* Often, we'll do some basic cleaning at the top.
* But more often, identify flaws as we go about errors.

Quartz bad data guide.
* Don't make assumptions
*

PDFs
* A bunch of you have encountered this.

* EXCEL ERRORS
https://arstechnica.com/tech-policy/2020/10/excel-glitch-may-have-caused-uk-to-underreport-covid-19-cases-by-15841/

KARA - timeframe has been manipulated
Part 2

In 2015, math proficiency rates have dropped anywhere from 20 to 50 percentage points across elementary schools in the county I covered as a reporter. Alarming, right? Well, yes, when I put it that way. But this is a timeframe and frame of reference manipulation. Some important context: 2015 was also the first year of new, harder state assessments (Links to an external site.). A better analysis of math proficiency would compare a span of years after the tests — and the teaching standards to which they were aligned — had rolled out. In the interim, however, it was important to report on and give the public context for the drop, because those test scores factored into school ratings and teacher evaluations. Another thing that reading the Quartz article made me realize I could have done was look at a range of years before 2015. That would have allowed me to report what the trend line for math scores was prior to the test change.

JACK -
While reporting for the Capital Gazette this summer, I examined data from the Treasury Department about Paycheck Protection Program loans given to small businesses in Prince George’s County to write two stories. A substantial amount of data was missing.

Many business owners opted not to include their gender or race, and business names and location were only listed for those that received loans less than $150,000. The Quartz bad data guide advises that the data may be blank because the value was never collected or because a respondent refused to answer this question –– which is what happened with the dataset I worked with. The guide says to beware blank values in any data set, unless certain about their meaning, and advises to ask your source if you’re unsure what the absence of the value means.

ALEX

I lead a non-partisan campus Get Out The Vote group and we use TurboVote to register students to vote and sign them up for election updates and reminders. Because we pay for the service, we are able to download data on student voter registration. Another thing we can do with the software is make "referral links" to track how many students registered at a particular event, from a certain email, etc. We were told that all registrations had some kind of "referral," so even if people just typed in the URL, it would say "web" in that column on the spreadsheet. When we started going through the data one day we realized some of the cells were blank under the referral column, so like the bad data guide says, we reached out to the TurboVote team to find out what that meant, rather than assuming how someone was referred to the service. Turns out, if someone clicks the plain link on social media, the cell remains blank.

HANA
The data in the L.A. Times repo my group is using to reverse-engineer street racing statistics is missing geolocation information for 4 incidents. Where there should be data, there is none - just a blank space. This was one of the things we chatted about in our group meeting, and the bad data guide just drove home the point: when you have values missing, you should ask yourself why those values are missing. Did they not know exactly where these people died? Why not? Since we can’t answer those questions,  we should ask the L.A. Times journalists who write the story why those discrepancies exist.

## EXAMPLES FOR CLEANING
* Duplicate misspelled names
* Missing values
* Funky column headers
* numbers read in as character

# Session 07 Instructor Notes

## To Have Up on Desktop

1. Session 07 Instructor Notes -
2. Webpage of roster pictures on UMEG -
3. Roster sheet with presence - https://docs.google.com/spreadsheets/d/1HKt0Dr6YajcRXLu-0IpWRWBMb4C9J-detlI0TE45jh8/edit#gid=1136077922
3. Course Canvas Page - https://umd.instructure.com/courses/1288268/modules
4. Slides -
8. GitHub Desktop
11. Email to check at regular intervals at beginning.
12. Phone to check for "can't get in texts"

## Openers

[START RECORDING]
* I'm recording.
* Reminders to mute your microphone.  
* And unless you've sent me a note explaining that you don't want to keep your video on during class, I'd ask that you turn it on now.  I won't force you to do it, just a reminder that it helps me teach.  
* And also a reminder to keep the chat up, cause I'll be asking you questions.

## Slides and what's due

Get Help
* Overview of class today
* Review lab_06
* Review discussion_06 - join story from ProPublica
* In class exercise on joins
* Review of what's due this week.
* Some points on data analysis project.


## Review lab 05
* Ask if any questions, things people didn't understand
 * Review exercise 1: Tori, Wesley, Audrey
 * How many total COVID **deaths** were there in each U.S. state as of August 30? which one had the fewest? Video showed wrong answer for some of you, I updated it, thanks Kara and Rona.
 * One mistake I saw a few of you make: confusing sum() and n()
   deaths_per_state <- covid_county %>%
     group_by(state) %>%
     summarise(total_deaths = n()) %>%
     arrange(total_deaths)
   # Display below
   deaths_per_state

 # Q: which state has the smallest number of deaths?
 # A: District of Columbia
* Review exercise 1 - Tori, Wesley, Audrey
* Ask people to volunteer what they did for exercise 2.
* Kellina question: Is there a way to find the county within a state that had the most amount of covid deaths? I tried the "filter" option but it didn't work. Maybe I needed to add something else? I would please like to know.
  * Kara:
  * Let's look at Spencers.  Florida filter.  
  * And John's.
  * And Hana's
  ```{r}
#Q: which county in Texas had the highest average number of deaths?
texas_most_deaths <- covid_county%>%
  group_by(county)%>%
  filter(state == "Texas")%>%
  summarise(texas_deaths = mean(deaths))%>%
  arrange(desc(texas_deaths))
texas_most_deaths
#A: It looks like the answer is Harris county with 2188 deaths....I'm suspicious of the whole number. I'd love to check this out in class.  
```
* And Rona: adding a filter would help here. ```{r}
counties_per_state <- covid_county %>%
  group_by(state) %>%
  summarise(total_counties = n()) %>%
  arrange(desc(total_counties))
# Display below
counties_per_state
```
* Kara: double

## Grouping and Summarizing Stories
* Review methodology for two stories we reviewed in forum over the weekend.

## Data Acquisition Project
* Review what's due.
* * Meticulously accurate, grammatical.  Treat this like a story, in terms of accuracy. Tone: Polite, professional and firm.

## Data Analysis project
* Review what's due.


# Session 06

1.  Review previous week's lab.  Look at questions people answered.
2.  Readings, how they did it.
* Donald Trump’s Campaign Is Cashing In On Impeachment | BuzzFeed News
* Huge increase in arrests of homeless in L.A. — but mostly for minor offenses | LA Times
2.  Go over send a letter.  Tips on writing a good letter.  As many details as possible. What's due.  Send in letter and post what you sent and that you sent it.  If you are emailing it, copy me on the email.
3.  Review findings from your posts.
4.  

# Review previous week lab
Questions people didn't understand.




# Session 05 Instructor Notes

## To Have Up on Desktop

1. Session 05 Instructor Notes -
2. Webpage of roster pictures on UMEG -
3. Roster sheet with presence - https://docs.google.com/spreadsheets/d/1HKt0Dr6YajcRXLu-0IpWRWBMb4C9J-detlI0TE45jh8/edit#gid=1136077922
3. Course Canvas Page - https://umd.instructure.com/courses/1288268/modules
4. Slides - https://docs.google.com/presentation/d/18-LMiujZ67s6_duLvo9CJ7iKL4HOspo9G6kHmoRz2GY/edit#slide=id.g94540b6654_0_0
8. GitHub Desktop
11. Email to check at regular intervals at beginning.
12. Phone to check for "can't get in texts"

# Openers

[START RECORDING]
* I'm recording.
* Reminders to mute your microphone.  
* And unless you've sent me a note explaining that you don't want to keep your video on during class, I'd ask that you turn it on now.  I won't force you to do it, just a reminder that it helps me teach.  
* And also a reminder to keep the chat up, cause I'll be asking you questions.

# SLIDES
https://docs.google.com/presentation/d/18-LMiujZ67s6_duLvo9CJ7iKL4HOspo9G6kHmoRz2GY/edit#slide=id.g94540b6654_0_0
* Do you need help?
* Review of what we're doing

# Ida Wells
Run through slides, including student response to data.
Show them one way she did it.

# Data acusition project.

* I'm in the middle of grading the first response.  
* In general, I was looking for a good deal of persistence on your part to get someone to respond.  If you started calling late, and only made a few calls, I was looking for more effort.  
* Persistince is key in this process.
* We're now at the point where we're going to send letters, if it's required. And we'll be going over next week what template to use.
* Some of you indicated you may be wanting to make some more calls before sending letter to get data, and I would STRONGLY encourage that.   

# Data analysis project
* What's due this week
* Be sure reached out to group.
* One response you work on together, but EVERYONE on your team submits.
* Questions

# In class ASSIGNMENT
* Show grouping and summarizing.
* We're taking a nother run at thsi, because I think last weeks' intro was overly complicated, too many other factors, and I want to make sure everyone gets this before we proceed.



# Session 03 Instructor Notes

## To Have Up on Desktop

1. Session 03 Instructor Notes -
2. Webpage of roster pictures on UMEG -
3. Roster sheet with presence - https://docs.google.com/spreadsheets/d/1HKt0Dr6YajcRXLu-0IpWRWBMb4C9J-detlI0TE45jh8/edit#gid=1136077922
3. Course Canvas Page - https://umd.instructure.com/courses/1288268/modules
4. Slides https://docs.google.com/presentation/d/1zWgyrPyrkwmv08ynnTX8JARzBcks5wiL8L8VgOh9U8w/edit#slide=id.p
8. GitHub Desktop
9. R Studio with lab_02 up to show exercises
11. Email to check at regular intervals at beginning.
12. Phone to check for "can't get in texts"


## Openers

[START RECORDING]
* I'm recording.
* Reminders to mute your microphone.  
* And unless you've sent me a note explaining that you don't want to keep your video on during class, I'3 ask that you turn it on now.  I won't force you to do it, just a reminder that it helps me teach.  
* And also a reminder to keep the chat up, cause I'll be asking you questions.

[PULL UP SLIDES]
https://docs.google.com/presentation/d/1zWgyrPyrkwmv08ynnTX8JARzBcks5wiL8L8VgOh9U8w/edit#slide=id.g98a4be9239_0_10

FIRST, before we go through what we're doing today, here's how to get help from me.

Here's what we're doing today.

1.  Review answers from previous lab.

[OPEN SM_2020_fall_data_journalism lab_02.RMD]
[RUN TIDYVERSE]
[LOAD BALTIMORE DATA ONLY on LINE 147]
[JUMP TO LINE 413 and answer question 1]
[ANSWER QUESTION 2]

2.  Review excuses forum post, talking about common features.
  * Everyone's were great, but a few common ones I hear all the time.  
  * We don't keep our data that way
    * Kara: report before making a request.  
    * Alexandra: heard from Columbus that they don't keep it as a spreadsheet. Her follow: okay, how do you keep it.
    * Find out how they keep it, and get it in whatever format they keep it in. They're obligated to give you what they have, not to create something new.  
  * We keep it on a computer OR, We keep it on a computer but we're giving you paper.
      * Audrey: get the paper or PDFs and start typing. Make your own database.
      * State law often says if it exists electronically, they HAVE to give it to you that way.  
  * It's not a public record or Part of it's public and part of it's not, so we're not giving you any of it. SHOW LINK - https://www.rcfp.org/open-government-guide/
    * Jeremy, Sara, Jummy: show me the statute.  The law is your friend.  Get to know the law in your state.  
    * Aadit: To that, I would say, take it out -- delete those columns or rows -- and give me what's left.
  * We don't know how to do that/we can't do that. The person who does it is gone.
    * Spencer: "We'll show you how".  
    * Ask to talk to data person.
  * It will cost you a LOT of money.
    * Tori: ask for charge breakdown.
    * Ask for fee waiver.  Many states have exemptions for journalist requests.
3.  Data assignment
    * What have you heard so far?  Help people work through problems.
4.  Review data reporting project 1
    * Groups
    * Assignment (Show example of story for this week for reading, and show first example)
    * How reading for this week fit in.
5. BREAK.
6. WORK THROUGH ASSIGNMENT
7. WHAT'S DUE THIS WEEK

state_population_duplicates <- read_csv("data/state_population.csv") %>%
  filter(state == "Maryland") %>%
  mutate(year = "2020") %>%
  select(year, everything()) %>%
  add_row(year = "2010", state = "Maryland", population = 5500000)

write_csv(state_population_duplicates, "data/state_population_duplicates.csv")

state_population_duplicates <- read_csv("data/state_population.csv") %>%
  filter(state == "Maryland") %>%
  mutate(year = "2020") %>%
  select(year, everything()) %>%
  add_row(year = "2010", state = "Maryland", population = 5500000)

write_csv(state_population_duplicates, "data/state_population_duplicates.csv")


# Filter to keep data only for Maryland, Virgina, Delaware, DC
county_covid_deaths_dirty <- read_csv("data/covid_county_2020_08_30.csv") %>%
  filter(state %in% c("Maryland")) %>%
  select(-cases) %>%
  mutate(state = case_when(county == "Allegany" ~ "MARYLAND",
                           county == "Calvert" ~ "mary land",
                           TRUE ~ state)) %>%
  mutate(deaths = as.character(deaths)) %>%
  mutate(deaths = case_when(county == "Garrett" ~ NA_character_,
                            county == "Caroline" ~ "three",
         TRUE ~ deaths)) %>%
  rename(`FIPS code !,` = fips)

write_csv(county_covid_deaths_dirty, "data/county_covid_deaths_dirty.csv")  
