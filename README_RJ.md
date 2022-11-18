![austin animal center](./images/austin-animal-center.jpg)

# Microsoft Movie Analysis

**Authors**: [Jonathan Fetterolf](mailto:) [Matthew Duncan](mailto:) [Nate Kist](mailto:) [Roshni Janakiraman](mailto:)

## Overview

This project analyzes multiple film databases to determine what factors make a movie successful. Descriptive analyses of movie characteristics and box office data show that high budget films provide the strongest return on investment (ROI), Animation is the movie genre with the highest profit, and the highest-rated films tend to be 85-110 minutes long. Microsoft can use this analysis to invest in the types of movies that are more likely to become successful.

## Business Problem

![img](./images)

Over the past decade, many promising film studios dissolved in their infancy, because they struggled to stand out in the marketplace. For an entrant to succeed in the film industry, producing successful films is critical to building brand recognition. Microsoft may be able to improve their likelihood of producing box office successes by prioritizing the funding of movies with certain characteristics.

## Data

The Austin Animal Center has the longest running public dataset of animal rescues in the country. Every animal has a unique ID associated with both their [intake](https://data.austintexas.gov/Health-and-Community-Services/Austin-Animal-Center-Intakes/wter-evkm) and [outcome](https://data.austintexas.gov/Health-and-Community-Services/Austin-Animal-Center-Outcomes/9t4d-g238) data. The data files provide the dates and types of each event, as well as other animal characteristics (e.g. type, sex).

## Methods

This project uses descriptive analysis, including description of trends over time. This provides a useful overview of AAC's typical intakes and outcomes to identify resource needs.

## Results

Most animals have short stays at AAC (under 15 days) but some have long stays (over 180 days), and most of these are dogs.

![stay_lengths_by_type](./images/stay_lengths_by_type.png)

The total number of sheltered animals typically peaks in May of each year and then hits its lowest point around January. There is often a secondary peak sometime after May before the number of sheltered animals drops rapidly. The number of sheltered animals has dropped precipitously in 2020, likely as a result of COVID-19.

![sheltered_by_month.png](./images/sheltered_by_month.png)

## Conclusions

This analysis leads to three recommendations for improving operations of the Austin Animal Center:

- **Engage in targeted outreach campaigns for dogs that have been sheltered at AAC for more than 30 days.** While most dogs will have been placed after 30 days, this may help reduce the number of dogs that end up having extended stays, potentially requiring many more months of care.
- **Reduce current spending until the numbers of intakes and sheltered animals return to normal.** Given the reduced activity during this period, AAC should consider ways to temporarily reduce costs by changing space utilization or staffing.
- **Hire seasonal staff and rent temporary space for May through December.** To accommodate the high volume of intakes and number of sheltered animals in the spring and fall, AAC should leverage seasonal resources, rather than full-year ones. This will allow AAC to cut back on expenditures during the months when there is lower

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
