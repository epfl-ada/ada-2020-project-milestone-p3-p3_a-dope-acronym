# Detecting Seasonal Patterns in User Movement  

< Disclaimer: Some plots are rendered with `plotly`, therefore they might not be rendered correctly in GitHub. Please refer to the Data Story for the plots. >

## Abstract 

There is more to human mobility than periodic patterns and social-based movement. Understanding how people travel between geographic regions and how the properties of these regions influence movement can greatly benefit general applications such as tourism, urban-planning, and policy-making. Using the original Brightkite dataset, we analyse the details of national and international travel, as well as temporal discrepancies beyond weekly patterns. The visualization of our findings will allow us to understand how various geographical features, such as cities, beaches, or mountains, are responsible for travel in different temporal splits and how these differences in movement vary between countries. 

## Research Questions

Using the same datasets as in the Friendship and Mobility paper, we will try to answer the following questions:
- How does human mobility fluctuate as a function of time throughout the year (e.g seasons, holidays, school, etc)?
  - Do poeple travel further during certain times of the year?
  - Are they more likely to see friends at certain times?
  - Does their home location change during the year (e.g. summer house)?
- How does spatial distribution of check-ins fluctuate throughout the year?
  - Can we find spatial patterns and seasonal tourist destinations (e.g. ski resort, beaches)?

## Proposed Datasets

We plan on using the same datasets as the Friendship and Mobility paper. Both datasets contain check-in data and a friendship network. As we are trying to extend the work of the authors, we decided the use their dataset for consistency. This will allow us to further investigate different patterns in the same data. 
- Brightkite's check-in and friendship data
- Gowalla's check-in and friendship data

## Methods

To tackle the first question, we plan on using the timestamp and location from the check-in data in order to observe mobility patterns throughout the year.
- We will do this by dividing the check-ins by month (perhaps by season) and doing an analysis similar to the one from the paper on distance travelled from home, probabilities to see friends... 
- We plan on analyzing during what times of the year people are likely to travel far from home, i.e. go on vacation. 
- We plan on analyzing how the home locations of the users change during the year: e.g. a user could move to a vacation house during the summer. This can be done by conducting the home calculation for each month or season.  

To tackle the second question, we plan on analyzing check-ins depending on the country. To do this, we will group check-ins by country using a library mapping coordinates to an exact address (e.g. `geopy`). 
- We plan on analyzing if and when users are likely to travel abroad, by comparing their home country to the other check-ins' countries. Note that this might create confusion with respect to our analysis of a user's secondary home location: these are totally independent. In this part, we only plan on using the primary home location, i.e. the most frequent one. 
- We plan on isolating the users that travel abroad and inferring the most popular tourist locations. 
- We plan on visualizing the fluctuation of check-ins (or their density) on a world map as a function of time, using a library like `geopandas`. 

## Proposed Timeline

We will divide the time alotted for this assignment into roughly three weekly parts. 

- **Week 1 (30.11 - 06.12)**: during this first part, we plan on focusing on the data wrangling part of the task. This consists in preparing the data by computing home locations, grouping by months, finding travelers. This also consists in augmenting the check-ins by adding the country corresponding to each check-in coordinate.

- **Week 2 (07.12 - 13.12)**: the second part will focus on data analysis and visualization. This is where we will observe trends and patterns using the prepared data. Our goal by the end of this week is to have a first draft of the final creative extension. 

- **Week 3 (14.12 - deadline)**: we will spend this last week cleaning up the project and preparing for the final submission. We will also dedicate these last few days to the video.

## Team Organization

For each of the three weeks we have decided on a strategy that combines pair programming and working as a full team. We will each meet in pairs during the week to complete the tasks we have laid out above, and then at the end of each week we will meet as a group and assess the work we have done and any adjustments we have to make for the upcoming week.

### Week 1

- Ben and Karim: reuse methods from replication of figure 2a to assign a home to each user and expand upon this by assigning a country to each check-in coordinate and inferring the home country of each user.
- Sander and Ben: group check-ins temporally, i.e. by months and by seasons and identify users who are travelers.
- Karim and Sander: assess work done during week and start preliminaries for week 2.

### Week 2

- Ben and Sander: analyze and visualize how far people are likely to travel from home at different times of the year. 
- Sander and Karim: analyze how home locations of users change as a function of time of year (i.e. summer homes).
- Karim and Ben: isolate users that travel abroad and infer the most popular tourist locations.
- Ben and Karim and Sander: visualization of the world map and the fluctuation of check-ins throughout the year.

### Week 3

- The video will be worked on as a team and once the subtasks become more clear we will divide them accordingly.
- Before the end of the week we will meet and go over the project as a whole to ensure quality.

## Questions for TAs 

- Not a question, but feedback on this proposal and more suggestions are more than welcome.

