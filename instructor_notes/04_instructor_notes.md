
# Session 03 Instructor Notes

## To Have Up on Desktop

1. Session 03 Instructor Notes -
2. Webpage of roster pictures on UMEG -
3. Roster sheet with presence - https://docs.google.com/spreadsheets/d/1HKt0Dr6YajcRXLu-0IpWRWBMb4C9J-detlI0TE45jh8/edit#gid=1136077922
3. Course Canvas Page - https://umd.instructure.com/courses/1288268/modules
4. Slides - NO SLIDES TODAY
8. GitHub Desktop
9. R Studio with lab_03 in my file to show exercises
11. Email to check at regular intervals at beginning.
12. Phone to check for "can't get in texts"

# Review of answers to previous lab.
 * Call on people who got it right to answer question
 * Q1: Sara, Kellina, Hana, Rona, Sasha, Susannah, Jummy
 * Q2: Rayonna, Jack, Hana, Rona, Sasha, Jummy
 * Q3: A lot of variations on other qesustions, which looked great.
      * Call on Spencer.  He created change and percent change in the same block! Double mutate.
      * Call on Kara to show what she tried to do, filtering by 23%
      * Call on Audrey to show str_detect()
 * Issues:
  * precision: questions asking specific things.  Accuracy matters.  If you get the wrong answer, and someone calls you on it, that's a correction!
  * confusing percent change with change
  * A lot of you are still sorting from lowest to highest by using desc()
  * In some of your code, it's clear to me you're not running before you submit (or getting an error and not fixing). A common one I'm seeing is misspelled column names.
# WHat are people hearing from data acquistion assignment and what's due.
  * Problmems people are running into
# Reading based discussion, on data points from the climate story.
  #### Clues to data driven sentences
  * Comparison: something was the highest or lowest, or higher and lower than something else. "McElderry Park, which despite its lyrical name offers little green space, is one of these: the hottest neighborhood in Baltimore, a city whose climate has long been classified as humid subtropical."
  * Change: something went up or down. "Average annual temperatures in Baltimore have gone up more than 3 degrees over the last century, nearly twice as much as the rest of the country.”
  * Measure of central tendency: the average of something or median or something.  "Average annual temperatures in Baltimore have gone up more than 3 degrees over the last century, nearly twice as much as the rest of the country.”
  * Relationship: In a place or at a time where one feature of that place is high, another feature is also high (or low).  I.E. we haven't established causality, but it's true that places that are hotter have higher crime rates.  
  ### Number 1
  * "McElderry Park, which despite its lyrical name offers little green space, is one of these: the hottest neighborhood in Baltimore, a city whose climate has long been classified as humid subtropical."
  * Explanation: "Using the mean afternoon temperature in the urban heat island study, McElderry Park was the city’s hottest neighborhood, with a mean afternoon temperature of 99.4 degrees F."
  * The code:
    * Show in the MD Document what we did
    * Selecting
    * Sorting
    * NOTE: before we got to this point, we did some cleaning! The code to get the data into a format where we could write a fairly simple function was more complicated.     
  * Discussion points:
    * The data led us to a specific point for a story.  
    * But it also led us to CENTER our reporting in McElderry Park.
    * In many ways, even when we quote people from the story from McElderry Park, or show a photo in McElderry Park, those were all decisions that eminated from data analysis.
    * Note the writing here.  General, backed up by specifics in the markdown document.
  #### Number 2
  * Sentence 1: “The heat index on the first floor of Tammy Jackson’s McElderry Park home registered 93 degrees, 9 degrees hotter than it was outside, at 10 p.m. Sunday, July 21”  
  * Explanation: Tammy Jackson, a resident of Baltimore’s McElderry Park neighborhood, had a temperature and humidity sensor installed in her house by our reporters. In her home, at 10 p.m. on Sunday, July 21, the heat index was 93 degrees F, 9 degrees hotter than the outside heat index of 84 degrees.
  * The code:
    * Show in the MD Document what we did
    * Took the processed data: https://github.com/Howard-Center-Investigations/code-red-baltimore-climate-divide/blob/master/data/output-data/temperature_sensors/tammy/tammy_day_hourly_averages.csv
      * Had indoor and outdoor heat index values.  
      * Filter and Selected
      * The code to get the data into a format where we could write a fairly simple function was more complicated.  
    * Discussion Points:
      * Used this data to flesh out the experience of one character
      * Also used it to establish a pattern: that it was often hotter inside than outside, especially at night. As we'll see in next one.
      * This data didn't exist, so we had to make it. A form of journalism called "sensor journalism". Show video on temperature sensors https://cnsmaryland.org/interactives/summer-2019/code-red/behind-scenes.html
  #### Number 3
  * Sentence 2: “The heat index was consistently higher inside Pingley’s home than it was outside.”
  Sentence 2: "A sensor inside a bedroom showed that the heat index during the heat wave was consistently higher inside than outside Pingley’s house."
  * Explanation: Between July 16 and July 23, the heat index inside of Pingley’s house was higher than the outside for more hours (108) than hours when the opposite was true (60).
  * The Code:
    * Show in the MD Document what we did
    * Took in the processed data: https://github.com/Howard-Center-Investigations/code-red-baltimore-climate-divide/blob/master/data/output-data/temperature_sensors/stephanie/stephanie_day_hourly_averages.csv
    * Filtered for just what we defined as heat wave (July 16 to July 23)
    * Created a new column in our data that had one of two values -- either it was hotter inside than outside.  
    * Then we grouped and summarized, which is process we will learn today and in this week's lab.


# What's due
* Upcoming reading Ida B Wells - pioneering investigative journalist - in the reading she groups and summarizes. We'll talk more about her next week.
* Lab this week
* Data acquistion memo due this week
* You should be reaching out to your groups

# In class ASSIGNMENT
* Show grouping and summarizing.

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
