### Johns Hopkins University (JHU) github data
Two sets: 
1. Daily Reports - answer questions like "How many total cases in {location} on {date}?"
2. Time Series - answer questions like "How many preported cases per day in {location} thru {date_range}?"

https://github.com/CSSEGISandData/COVID-19

#### A few notes:
1. All dates in the "current" are UTC
---------------------------

#### Daily Reports 
https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_daily_reports

**What**: Each file has 1 row that contains total cumulative totals from Jan 22 through this date\
**Keys**: Admin2 (city), Province_State, Country_Region\
**Update freq**: Daily\
**Use when**: 
1. You only care about the cumulative total numbers as of a specific date
2. You plot current/specific day's case numbers by either City/State/Country, State/Country, or Country
2. You want to map / chloropleth (inc. lat/long)

What: A count of the confirmed cases/deaths/recoveries from Nov 1, 2019 up until this date\
Granularity: City => State/Province => Country\

---------------------------

#### Time Series  
https://github.com/CSSEGISandData/COVID-19/tree/master/csse_covid_19_data/csse_covid_19_time_series

**What**: 1 row per Province/State, Country and 1 column per day since Jan 22 that contains that day's counts (not cumulative). Separate files for confirmed, deaths, recoveries.  \
**Keys**: State/Province, Country\
**Use when**: 
1. You want to plot daily case numbers by State/Province and/or Country
2. You want to map / chloropleth (inc. lat/long)

---------------------------

#### Archived - Daily Reports
**What**: \
**Keys**: \
**Use when**: 

#### Archived - Time Series
https://github.com/CSSEGISandData/COVID-19/tree/master/archived_data/archived_time_series

**What**: 1 row per City/State/Country and 1 column per day since Jan 22 that contains that day's counts\
**Keys**: State/Province, Country\
**Use when**: 
1. You want to plot daily case numbers by State and/or Country
2. You want to map / chloropleth (inc. lat/long)
* Example: On March 26, the March 25 csv had 66 columns - the 4 "keys" and 62 separate columns b/c there have have been 62 total days passed since Jan 22