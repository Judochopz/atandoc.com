---
author: Alec
title: "California Internet Speeds by County"
date: 2023-09-12
draft: false
tags: ['Python', 'GeoPandas', 'Pandas', 'Data Analysis']
cover:
    image: img/california_county_internet.png
    alt: 'Internet Speeds in California Counties'
    caption:
---
# Intro
The goal of this project was to collect internet speeds in counties throughout California and explore the reasoning behind the differing county speeds.
([Github Link](https://github.com/Judochopz/california-internet-accessibility))
# Findings
Pictured below are the top 20 counties by average download speed (Mbps).
![Top 20 Speeds](/img/top_20_internet_speed_california.png)
Contrary to what many may think, only a few counties, like San Mateo,
Contra Costa, and Alameda, ranked in the top 20 for both average internet speed
and median household income
([Census Bureau](https://censusreporter.org/data/table/?table=B19013&geo_ids=04000US06,050|04000US06&primary_geo_id=04000US06)),
but more than half of the counties with top 20 internet speeds did not intersect
that top 20 income list. It is likely that there is little correlation with
county wealth and internet speeds. What I did find was that 8 out of the top 10
counties in internet speeds were located in the San Francisco-Sacramento area.
This is likely due to the high concentration of tech companies, especially in the
parts of Santa Clara, San Jose, Alameda, and San Mateo counties that are dubbed
Silicon Valley.
# Process
The internet speed tests were pulled from Ookla's API and the shapefile was pulled
from the U.S. Census Burea into two GeoPandas dataframes. I then isolated rows
containing data from California and then merged the dataframes. Afterwards I compiled the
individual tests and grouped them by county. I then used MatPlotLib to plot the data,
shading each county by their average download speed (Mbps) and labeled the 11
most populated counties for reference. ([Github Link](https://github.com/Judochopz/california-internet-accessibility))