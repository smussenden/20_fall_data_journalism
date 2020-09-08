# Session 02 Instructor Notes

## To Have Up on Desktop

1. Session 01 Instructor Notes - X
2. Webpage of roster pictures on UMEG - X
3. Roster sheet with presence - https://docs.google.com/spreadsheets/d/1HKt0Dr6YajcRXLu-0IpWRWBMb4C9J-detlI0TE45jh8/edit#gid=1136077922
3. Course Canvas Page - X
4. Slides on introducing data acquisition project - NEED TO MAKE
5. Slides on post opioid story  - need to make
6. Sides on reasons to do data journalism - need to make
7. Slides on importance of documentation. - need to make
8. Link to download data and file we'll use for today for class assignment.
9. R Studio


## Openers

[START RECORDING]
I'm recording.

## First Half Class

### Washington Post Opioids

##### Q: Where did the data come from?

It's maintained by the DEA.  It's the way the DEA tracks shipments of controlled substances.   Automation of Reports and Consolidated Orders System (ARCOS).  In its original form, it tracks thousands of controlled substances, documenting the movement of each batch of pills from the manufacturer, to a distributor to the person who sells or dispenses it, typically a pharmacy.

https://www.deadiversion.usdoj.gov/arcos/index.html

##### Q: Was it designed by the government to help journalists tell stories about shipments of controlled substances?

No, it was not.  It was designed by the government to look for suspicious purchases and movements of controlled, dangerous substances.  They fought the release of it for years.  Journalists only got access to it by filing a lawsuit, intervening in a lawsuit by state and local governments against opioid manufacturers.

Even today, you can't just like go to the DEA Website and download it. We're going to use cleaned up versions released by the Post.

A LOT of data is public.  But often, to tell the story you want to tell, you have to use reporting and public records laws to get the good stuff.

You'll get some practice in this class.

##### Q: What are some key facts generated by data analysis?   

You all killed it on this.

[PULL UP in_class_02_lecture_demo.Rmd]

In the raw data, each row is a shipment of a unique unit of pills that has the date, manufacturer, distributor, end pharmacy (including address), number of pills, info about the type of pill and more.   



* A: A total of 76 billion opioids shipped between 2006 and 2012.
  * Q: How did they calculate this, just in English, don't worry about what the code might look like?
  * Discussion: Each transaction has the number of pills in that, so if we add all those up, we can answer this question.
* A: The total number of pills increased "about 51 percent from 8.4 billion in 2006 to 12.6 billion in 2012.
  * Q: How did they calculate this, just in English?  
  * Discussion: Each transaction has the number of pills in it, plus the date.  If we create a total for each year -- add up all the 2006 shipments together and all the 2012 shipments together -- we will get two totals. We can use a percent change formula to calculate the increase.
* A: Just six companies distributed 75 percent of the pills during this period: McKesson Corp., Walgreens, Cardinal Health, AmerisourceBergen, CVS and Walmart, according to an analysis of the database by The Washington Post.
  * Q: How did they calculate this, just in English?  
  * Discussion: Each transaction has the number of pills in it and the distributor. We know the total number of pills shipped from the first question, it's 76 billion.  If we calculate the total number of pills shipped by each distributor, and divide it by the total of 76 billion, we get the percentage share for each company.  And if we add together the top six, we get 75 percent.
* A: Rural areas were hit particularly hard: Norton, Va., with 306 pills per person; Martinsville, Va., with 242; Mingo County, W.Va., with 203; and Perry County, Ky., with 175.
  * Q: How did they calculate this, just in English?
  * Discussion: The data includes pills in each shipment, and the pharmacy it was sent to, including the address.  By totaling up all of the pills sent to each city, and then dividing by population (which they got from another dataset), they were able to calculate the per person rate for each city.  Then they rearranged the data from highest to lowest.  

A few takeaways here:
* Our ability to ask specific questions is limited by our data. We couldn't ask, for example, any questions about the gender of people who received the pills using this data, because there's nothing in here about patients who got the pills.  And, for example, we could only answer the "rural areas hit hard" question because we went out and got another data set -- population.
* There are common types of questions we ask over and over again -- how have things changed over time, who has been affected the most or the least, who is most responsible (share). But the best questions are often specific questions we know to ask because some reporting has guided us there.  
* There's a process we're going to follow when attempting to answer questions. This is a key skill to cultivate.   
  * One: Come up with a loose question we want to know the answer to. How many total pills were shipped by all manufacturers between 2006 and 2012?
  * Two: Figure out out if we can ask the question with the data we have, and get a bit more specific about the process to answer that question.  Let's take the ARCOS database and add together all of the pills in each shipment between 2006 and 2012.
  * Three: Let's "operationalize" our question, take it from our rough English question and put it into a language our data understands. And by that I mean, write code.   

##### Q: What are some key facts generated by data analysis?   

* Some of you picked out Andrew Ba Tran, Steven Rich and Aaron Williams.  But the truth is everyone plays a role.  Understanding the data is critical, and reporting plays into it. All that context and sourcing helps understand how to use the data, what questions to ask, and how to make sense of it.  Analysis is not separate from reporting. It's part of it.

##### Q: How do we know what fields mean?

What does dosage_unit
* Show post data dictionary
https://github.com/wpinvestigative/arcos-api/blob/master/data/data_dictionary.csv
* Show example data
https://www.scribd.com/document/353876856/ARCOS-Registrant-Handbook#download
* What do we do if we still dont' know what this means. Call someone.

Documentation is key. ALWAYS LOOK FOR THIS

### Why Data Journalism

* Skipping this.  

### DATA PROJECT
https://docs.google.com/document/d/1KiXObj9AflDX4kJ5vQlvj36yx5KFumlJ1wHLQ04z7Ic/edit
https://docs.google.com/document/d/151W6oZ-wwHhOWZJWRMHXDIlEPTEdRG59Afo5CRI5pl0/edit
https://www.nhlp.org/resource-center/public-housing/
https://www.nhlp.org/wp-content/uploads/2018/01/NHLP-Public-Housing-outline.pdf