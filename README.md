# surfs-up

## Overview of Oahu Weather Audit
We are helping an investor learn more about the temperature in Oahu before investing in a Surf and Ice Cream shop. For this, we were tasked with using pandas and sqlalchemy to obtain the summary statistics from Hawaii weather data in a SQLite database. We pulled the summary statistics for the months of June and December.

## Oahu Weather Audit Results

**Process**

- Import Dependencies
  -  Import Dependencies for numpy, pandas, and sqlalchemy.
  -  Create Engine, Automap Base, and Reflect Tables.
  -  Save references for Measurement and Station Tables.
  -  Create Session.
![Image Name](Image Path)

- June Temperature Data
  - Query the temperature observed column on the measurement table and filter by the date column in the measurement table for when month equals 6, as seen in #1.
  - Creating a new list by loop through the list of tuples from step 1 and taking the result of the in the first index of each tuple, as seen in #2.
  - Create a pandas Dataframe with the list created in step 2 and name the column "June Temps", as seen in #3.
  - Obtain summary statistics with the describe function, as seen in #4.
![Image Name](Image Path)

- December Temperature Data
  - Query the temperature observed column on the measurement table and filter by the date column in the measurement table for when month equals 12, as seen in #6.
  - Creating a new list by loop through the list of tuples from step 6 and taking the result of the in the first index of each tuple, as seen in #7.
  - Create a pandas Dataframe with the list created in step 7 and name the column "December Temps", as seen in #8.
  - Obtain summary statistics with the describe function, as seen in #9.
![Image Name](Image Path)

**Learnings**

- On average the temperature throughout December was roughly only 4 degrees colder than June. June's mean temperature 74.9 and December's mean temperature 71.0.
- The biggest difference in the distribution between June and December is the minimum temperature for each month. December's minimum temperature of 56 was 8 degrees colder than June's 64 minimum temperature. Nothing past the 25% percentile differed by more than 4 degrees staying closer toward the max.
- The total count of observations of 1517 from December is 183 observations lower than that of June's 1700 observations.

![Image Name](Image Path)
![Image Name](Image Path)

## Oahu Weather Audit Summary

**Findings**

In summary, both months on average will stay above 70 degrees most days. December will definitely have some colder days than June that might impact the level of ice cream and surfing that takes place those days but looks to be surfable a lot of the time. Using the climate_analysis we pulled earlier, there's likely more concern for being rained out than being too cold to surf.

**Additional Queries**

- I would write a query to look into the difference in observations to see if there's a gap in the temperature observations, whether that's missed days or a missed station, this difference in days could skew December's statistics for the investment's benefit or demise. You could query to get the count of stations that had an observation or even query the count of observations grouped by each station.
- We could also edit the query to return June and December precipitation summary statistics to compare with the temperature data. We would likely want to also query more months in order to compare more evenly throughout the year, even though seeing June and December's data is promising that the weather between those months stays relatively consistent.
