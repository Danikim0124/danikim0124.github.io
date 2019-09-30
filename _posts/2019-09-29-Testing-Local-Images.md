---
layout: post
title: Project 1.  MTA Subway Data Analysis
---
The first project at Metis was based on analyzing the MTA subway data to provide a specific guideline to our clients.

WomenTechWomenYes(WTWY) has an annual gala at the beginning of Fall each year. Out clients from WTWY wanted to maximize attendance in an annual gala to fill their event space and to outreach for fundraising.

In this project, our team in Metis provided a strategy to place street teams at entrances to subway stations to gather the most people to meet their needs.


## Data Acquisition and Preprocessing

The MTA subway data was acquired from [Turnstile data sets](http://web.mta.info/developers/turnstile.html). Each data consists of turnstile information with entrance and exit counts, which was counted every four hours. Here are more detailed information in MTA datasets.

-C/A = Control Area

-UNIT = Remote Unit for a station

-SCP= Subunit Channel Position (an specific address for a device)

-STATION= Station name

-LINENAME= Train lines that can be boarded at this station

-DIVISION= Line originally the station belonged to BMT, IRT, or IND   

-DATE= Represents the date (MM-DD-YY)

-TIME= Represents the time (hh:mm:ss) 

-DESc= Represent "REGULAR" scheduled audit event (Normally occurs every 4 hours) or "RECOVR AUD" (a missed audit that was recovered)

-ENTRIES= The comulative entry register value for a device

-The EXIST= The cumulative exit register value for a device

Here, our team collected total of six datasets from first two weeks in October from 2016-2018. Then, data cleaning and analysis was done with Pandas and Seaborn.

## Analysis (Place, Day, Time)

#### Places

The entrance and exit traffic for top 10 stations were accounting for about 20% of total traffic. A Figure 1 shows list of top 10 stations with their percentage of traffic among top 10 stations. For example, Penn Station, located on 34th street, is about 15%(~ 11 millions) of top 10 traffics.


Figure 1. Station vs. Percentage of traffic for top 10 stations.
![Image test]({{ site.url }}/images/Top10_stations.png)

#### Day and Time

A Figure 2 shows percentrage of traffic vs. day of week. As expected, this graph clearly shows that working days, from Monday to Friday, have the most traffic. Thus, placing street steams on the working days is desirable.

Figure 2. Percentage of traffic vs. day of week for top 10 stations
![Image test]({{ site.url }}/images/Traffic_day.png)


A Figure 3 shows percentage of traffic vs. time of day. The most traffic occurs between 4:00 and 8:00 pm, thus placing street teams in this time period would be practical. If you really have to outreach on weekend, the same time period will be applied, as shown in Figure 4.

Figure 3. Percentage of traffic vs. time of day for top stations
![Image test]({{ site.url }}/images/Traffic_hour.png)
Figure 4. Percentage of traffic vs. weekend for top 10 stations
![Image test]({{ site.url }}/images/Traffic_weekend.png)


## Street Team Strategy

Our strategy is based on percentage of total traffic for the top 10 stations, as shown in Figure 1. For example, if our clients have total of 100 available people to place on the street, then about 15 people in Penn Station, 13 in Grand Central Station, and so on. The best day and time to place people on the street is between Monday and Friday with 8:00 am and 8:00 pm with an strong emphasis on 4:00 and 8:00 pm.