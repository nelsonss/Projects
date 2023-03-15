# Introduction to Storm Events Data
## Storm Event Data
Throughout this course, you’ll be using Storm Events data from the National Oceanic and Atmospheric Administration (NOAA) to practice performing data analysis techniques. 

This reading briefly describes key elements of the data sets and some insight into how events are recorded. It is intended to help you better understand the data if you’re interested in exploring its contents further. Refer to the links above to find more detailed information about the data.

The Storm Events data is useful for real-world applications such as:

Predicting future costs due to weather for disaster planning

Allocating resources to respond to natural disaster 

Calculating insurance cost for weather types or locations

For the goal of learning exploratory data analysis, the data is useful because we’ve all experienced weather! No domain knowledge is needed to understand that floods can cause damage. Additionally, the file: 

Has a mix of different data types

Contains many possible ways to group the data

Has missing data that needs to be addressed when calculating statistics

Lends itself to a variety of useful visualizations

You’ll learn how to do all the bullet points above in this course.

Overview  of the Data
Open the file “StormEvents_2018.csv” and look at the first row. This row contains the column headers for the data. Hopefully, some of the column headers are descriptive enough that you can interpret them, such as Month, Event_Type, Begin_Date_Time, Property_Cost, Begin_Lat, etc. In this reading, we’ll take a closer look at headers that may not be immediately obvious:

State

EpisodeID

Event_ID

Duplication of property and crop damage reporting

States and Counties in the United States
The United States of America consist of 50 states (plus several territories). Each state is made up of numerous counties. Counties vary greatly in geographic size and population. Counties may consist of several towns and cities, or possibly a single large city. The size and shape of counties as well as the number of cities in the county impact on the number of events recorded in the file. For example, events that cross state or county boundaries are recorded as multiple events. 

EpisodeID and EventID
Understanding how your data is collected and organized is very important in data science. This varies significantly depending on the source. For the Storm Events data, the key to understanding individual entries is to distinguish between the EpisodeID and the EventID.   

The EpisodeID describes an entire storm system. The EventID describes a specific event associated within an EpisodeID. In the example below, a single storm system produced multiple damage-causing Thunderstorm Wind events. Additionally, Hail was reported as a separate event. When the storm affects different counties and towns, a new event is recorded for the new location. Thus, what you might think of as a single event may be reported as multiple events.

EpisodeID describes the weather system and is not unique

EventID describes a locality affected by a weather event and is unique

Example - Thunderstorm Wind and Hail in New York State
Below is a preview of a few entries from the 2018 Storm Events data. Notice that the highlighted lines all have the same EpisodeID but have unique Event_IDs. Additionally, while most are recorded as Thunderstorm Wind, there is an entry also listed as Hail. 


Events spanning multiple months
Long duration weather events, such as droughts, may also appear as multiple events in the data. For example, a drought that affects a single location in the months of July and August will appear as two events, one for each month.   

Damage Cost to Property and Crops
You’ll notice an apparent duplication of information in the data and shown in the image below. The damage values are reported in two different formats – one using a K or M after a number to denote thousands or millions of dollars respectively, and the same value listed purely as a number. 



The original data is recorded with a K or M. As cleaning data for analysis is covered later in the specialization, the numeric values were added to the file for you. In this course, you will only need to work with the numeric data.

How Would You Organize the Data?
Data sources will never be perfect. Part of your job as a data scientist will be to make sense of the data and communicate it to others. In this course, you’ll learn how to group your data, select a subset of data from the table, calculate statistics on the data, and visualize the results. By the end of the course, you will be able to filter the data to include only events listed in a narrow time range and geographic area to define a storm outbreak, and calculate the damage caused by that storm.
