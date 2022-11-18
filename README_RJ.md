![austin animal center](./images/==jonathan's design here? or filmy pic?==.jpg)

# Microsoft Movie Analysis

**Authors**: [Jonathan Fetterolf](mailto:) [Matthew Duncan](mailto:) [Nate Kist](mailto:) [Roshni Janakiraman](mailto:)

## Overview

This project analyzes multiple film databases to determine what factors make a movie successful. Descriptive analyses of movie characteristics and box office data show that high budget films provide the strongest return on investment (ROI), Animation is the movie genre with the highest profit, and the highest-rated films tend to be 85 - 100 minutes long. Microsoft can use this analysis to invest in the types of movies that are more likely to become successful.

## Business Problem

![img]==insert film pic here==(./images)

Microsoft may be able to improve their likelihood of producing box office successes by investing in films with similar characteristics to recent successful releases. The following questions guided our analyses:
    1. What genre of movie is most profitable?
    2. What type of budget should we plan for this movie?
    3. What is the movie's expected runtime?

## Data

Data for this analysis is taken from three of the largest online movie databases, described in detail below.

### 1. The MovieDB (TMDB)

[TMDB](https://www.themoviedb.org/?language=en-US)is a user-built database of movie information and user ratings. The current dataset includes 26,517 datapoints and 9 columns of data. The target data includes release date and genre, where the genre codes are ordered by relevance.

### 2. The Numbers (TN)

[TN](url) dataset consists of box office information across 5,782 movies. The target data includes release date, production budget and worldwide gross revenue.

### 3. Internet Movie Database (IMDB)

[IMDb](url) is an online database consisting of movie information, statistics, and user ratings. The IMDB dataset is comprised of multiple tables. For the current analysis, we used two tables consisting of basic movie data and user ratings for movies. The target data includes release date, runtime length (in minutes), and average rating.

## Methods

This project uses descriptive analytics to describe trends in the features of successful movies. 

For all tables, we removed unnecessary columns, cleaned, and filtered all of the tables used. To make sure that the data we used was relevant to Microsoft's business question, we limited the data to only include movies released between 2010 - 2019 and English movies. All numerical columns were scaled to be in millions (MM). 

We merged TN with TMDB to address Question #1. TMDB uses 18 primary genres to classify the movies in their database. We used a bar chart to examine the average net profit of each genre of movie, and limited our findings to the top 10 most profitable genres.

Using the TN dataset, to answer question #2, we calculated two new variables of interest: Net Profit and Return on Investment (ROI). The main analysis used a bar chart to compare the median ROI of films based on production budget. Based on definitions used by [Hollywood market researchers](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3751648), we grouped our data into 3 budget categories:
1. Low (less than $20 MM)
2. Medium ($20 MM - $100 MM)
3. High (greater than $100 MM)\

We then compared the median ROI of each budget groups to determine which budget group provided the best value for its cost. We used the median ROI because there are extreme outliers in each budget group that might misrepresent how a 'typical' movie would fare. The median tells us the ROI for a 'typical' movie across budget groups.

To address Question #3, we used the IMDB dataset. Since the IMDB dataset had over 35,000 datapoints, even after applying our filter criteria, we decided to further refine our question: *of the highest rated films on IMDB, what is the most common movie length?* We then narrowed down the dataset to include only the highest rated movies (average user rating of 8.0 or greater) on IMDB. 

## Results

### Question 1: What genre of movie is most profitable? ###
* Over the 2010s, the **Animation** genre had the highest average yearly profit. ($313 MM per year)
* **Family** films, a related genre, was the second-highest profitable genre of the 2010s ($292 MM per year).

### Question 2: 
* High budget films provide the strongest ROI, with the typical high-budget film yielding a 200% ROI

### Question 3: 
* Out of all of the highest rated movies (ratings > 8.0), there were more movies in the 85 - 100 minute range than any other movie length.  
* This would indicate a viewer preference for movies with this length.

## Conclusions

This analysis leads to three recommendations for improving operations of the Austin Animal Center:

- **1. Produce movies within the 'animated' or 'family' genres to maximize net profit.** Movies with the primary genres of 'animated' and ‘family’ have the highest average yearly net profits over the 2010s.
- **2. Produce high-budget films: Microsoft should plan to invest at least 200 MM per film** High-budget films have the greatest potential for maximum returns, with the typical high-budget film yielding returns worth 200% more than the initial investment. 
- **3. Hire seasonal staff and rent temporary space for May through December.** To accommodate the high volume of intakes and number of sheltered animals in the spring and fall, AAC should leverage seasonal resources, rather than full-year ones. This will allow AAC to cut back on expenditures during the months when there is lower

### Next Steps

Further analyses could yield additional insights to further improve operations at AAC:

- **Better prediction of animals that are likely to have long stays.** This modeling could use already available data, such as breed and intake condition.
- **Model need for medical support.** This modeling could predict the need for specialized personnel to address animals' medical needs, including neutering, using intake condition and sex data.
- **Predicting undesirable outcomes.** This modeling could identify animals that are more likely to have undesirable outcomes (e.g. Euthanasia) for targeted medical support or outreach.

## For More Information

See the full analysis in the [Jupyter Notebook](./animal-shelter-needs-analysis.ipynb) or review this [presentation](./Animal_Shelter_Needs_Presentation.pdf).

For additional info, contact Alison Peebles Madigan at [alison.peeblesmadigan@flatironschool.com](mailto:alison.peeblesmadigan@flatironschool.com)

![logo](./images/aac_logo_tall.jpg)

## Repository Structure

```
├── code
│   ├── __init__.py
│   ├── data_preparation.py
│   ├── visualizations.py
│   └── eda_notebook.ipynb
├── data
├── images
├── __init__.py
├── README.md
├── Animal_Shelter_Needs_Presentation.pdf
└── animal_shelter_needs_analysis.ipynb
```
