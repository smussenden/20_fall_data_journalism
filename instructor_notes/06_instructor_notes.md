VIDEO LAB Notes
AYWCM-3WHHV-CF3QH-5Y6HA-E2D7C
# 1
* First, let's look at the original tables
* Each contains the same first three columns, and a fourth that's different.
* The inner join worked by looking for matches.  
* Consider autuaga alabama.  the fipscode, state and city are exact same in both tables.
* So it knew to put them together.
* same for the next county
* everytime it found a mtach, it put them together.
* if it didn't find a match, it left them out.
* thats why, by the way, these tables have different numbers of rows
* population has 3143
* pills per year has 3130
* but our county pills population table has 3036 -- fewer than either?
* why? Because there are some counties in our pills table not in our population table.  And some counties in our population table not in our pills table.
* We'll see more below.

# inner join
* Show VENN - The inner join worked by looking for matches.  
* An inner join returns all columns from both tables.  But it only returns those rows where there's a match in both tables in the three columns we're joining on (countyfips, buyer_county and buyer_state).
* Consider autuaga alabama.  the fipscode, state and city are exact same in both tables.
* So it knew to put them together.
* same for the next county
* everytime it found a mtach, it put them together.
* if it didn't find a match, it left them out.
* Again, let's look at the numbers of rows
* population has 3143
* pills per year has 3130
* but our county pills population table has 3036 -- fewer than either?
* why? Because there are some counties in our pills table not in our population table.  And some counties in our population table not in our pills table.
* For example, our pills table has Puerto Rico -- PR. And our population table does not. And so PR doesn't end up in joined table.
* Oh, and BRISTOL BAY AK is in our pills table. But not in our population table. So Bristol Bay does not end up in joined table.
* When we do the inner join, they get left out.

# left join
* Show VENN - The left join
* a left join returns ALL rows from Table A (county_pills_per_year) regardless of whether there's a match in Table B (county_population).  If it finds a match in Table B, it will pull that information in and put it in the appropriate column.  If it doesn't find a match, it leaves it blank.
* Consider autuaga alabama.  the fipscode, state and city are exact same in both tables.
* So it knew to put them together.
* But now let's look at something our pills table has that our population table DOES NOT -- Puerto Rico.
* Look what it did here.  It included the value for pills.  But because there was NO match in our population table, it included the row, but left that blank.
* Notice that when we do the left join, the number of records in our joined table is the same as our pills table.  
* Because it's keeping all the rows.
* Also notice Bristol Bay AK isn't here.  Why, it wasn't in our pills table. So it doesn't get returned here.

# right join

* Show VENN - The right join
* It returns ALL rows from Table B (county_population) regardless of whether there's a match in Table B (county_pills_per_year).  If it finds a match in Table A, it will pull that information in and put it in the appropriate column.  If it doesn't find a match, it leaves it blank.
* Consider autuaga alabama.  the fipscode, state and city are exact same in both tables.
* So it knew to put them together.
* But now let's look at something our population table has that our pills table DOES NOT -- Bristol Bay AK.
* Look what it did here.  It included the value for population.  But because there was NO match in our pills table, it included the row, but left that blank.
* Notice that when we do the right join, the number of records in our joined table is the same as our population table.  
* Because it's keeping all the rows from that table.
* Also notice Puerto Rico isn't here.  Why, it wasn't in our pills table. So it doesn't get returned here.


# Session 06 Instructor Notes

## To Have Up on Desktop

1. Session 06 Instructor Notes -
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
https://docs.google.com/presentation/d/1T4gJrFP8ADBHJCl-M9un89I9-fNDfwNtV4KKfwBuTFw/edit#slide=id.g94540b6654_0_0
Get Help
* Review lab_05
* Review discussion_05 - grouping and summarizing stories
* Review data_acquisition_project next milestone [this week]
  * Write and send in letter
* Review data_analysis_project next milestone [next week]
  * Should be preparing for this now.  
* Exercise enterprise joins

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
