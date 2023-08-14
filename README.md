# README

Completion date: August 19, 2022      

## Table of Contents
1. [Overview](#overview)
2. [Data Question](#dataquestion)
3. [Methodology](#methodology)
4. [Technologies](#technologies)
5. [Data Sources](#datasources)
6. [Conclusion](#conclusion)

<a name="overview"></a>
## Overview

Golf. From Putt Putt to PGA, it seems most people have had some exposure to the sport. Growing up in Middle Tennessee, I've seen golf courses everywhere. I worked in Williamson County for a few years. That being said, it feels like I can't drive into Williamson County without passing at least one course. I wanted to take my real life observations and put my skills to use to prove (or disprove) my hypothesis that there are more golf courses in higher income areas.
  
<a name="dataquestion"></a>
## Data Question

Is there a correlation between high income areas and the number of golf courses in any given county? Are there correlations between other county characteristics?
  
<a name="methodology"></a>
## Methodologies
  #### Gathering the Data

I looked to census.gov for my county characteristics. I used the census API to bring in population numbers from the 2020 Decennial Census.

Also utilizing the census.gov for income, I pulled estimated median household income per county using the Small Area Income and Poverty Estimates API

I was able to find golf course location data on poi-factory.com, listing full detail of courses across the U.S., including geospatial info.

One metric I wanted to include was county areas, which I found on usa.com.

I also wanted to divide the data into data regions, East, Middle, and West. I pulled counties by region from tn.gov

I pulled TN county geospatial data from hub.arcgis.com, needing this for mapping golf courses after analysis.
  
  #### Cleaning the Data

Bringing in this much data, I knew there was plenty of cleaning ahead of me. Utilizing Python, I was able to import all data and edit columns to format my dataframe in a way which simplified merging the data. The data retrieved from census.gov was broken down in small metrics, therefore I edited and renamed columns over multiple pulls from the API.


  #### Analyzing the Data

I joined the clean dataframes to give a cetralized look at all the metrics I wanted to analyze. This dataframe included golf course and county info(name, over 65 population, total population,estimated household income, area in square miles, and region)

Bringing the data into Tableau, I had to manipulate the data further. Using the different tables, I had to connect them on county name in order to display the data properly.

  #### Telling the Story

Using a combination of heat maps, scatter plots, and overall maps in Tableau, I told a story that walks through the data leading to the conclusion of the analysis in Powerpoint.

<a name="technologies"></a>
## Technologies

Python: Pandas, GeoPandas, RegEx, Matplotlib.pyplot, Folium
Tableau: Visualizations of data findings
Excel: Minor post-analysis data manipulation

## Data Sources
  
  #### API

2020 Decennial Census: https://www.census.gov/data/developers/data-sets/decennial-census.html

Small Area Income and Poverty Estimates: https://www.census.gov/programs-surveys/saipe/data/api.html

  #### Imported

Golf Course Locations: http://www.poi-factory.com/node/29395

TN Counties Geospatial: https://hub.arcgis.com/datasets/b3b22bda38d54d0686efb4a9d60c8d1b/explore?showTable=true

TN Counties Region List: https://www.tn.gov/partnersforhealth/insurance-premiums/counties-by-region.html

TN Counties Area by Square Mile: http://www.usa.com/rank/tennessee-state--land-area--county-rank.htm

<a name="conclusion"></a>
## Conclusion
The immediate observation upon analyzing the data leads to the understanding of golf course locations being driven by total population. With the data that was analyzed, We can see that there is not a strong correlation between median income and the number of golf courses in a county. The same can be said about the county's land area in square miles. One shocking observation from the analysis is that the percent of a population over the age of 65 has little correlation with the amount of golf courses.

## What Now?
From here, a look at the same metrics on a larger scale could provide different results. Moving forward, I plan on looking at the country as a whole. I also plan to do the same analysis with Florida, as it as seen as the retirement state and may show a different outcome in terms of the age metric. Another annalysis would include looking at individual cities in populated counties. Based on my knowledge of the area, I feel that some of the county data could be skewed by larger cities in certain counties. A smaller scale analysis could balance this. 