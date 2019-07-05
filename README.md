## Senior Pedestrians in NYC: 
## A Diff-in-Diff Approach to Evaluating Safe Streets for Seniors


### Motivation

1. People are flocking to cities and the US population is growing older
2. A key component of urban life: Walkability
3. But NYC streets are dangerous for senior pedestrians
  - Fatality rates are 4x higher for seniors
  - And 16% higher in NYC than the rest of the nation (Nicaj et al.)
4. NYC’s response → Senior Pedestrian Focus Areas (SPFAs)


### Relevant Literature
1. What works:
  - Increased pedestrian crossing times, more traffic signals, more bike lanes (Chen et al.)
2. What doesn’t:
  - Midblock pedestrian fencing (Chen et al.)
3. 10 community districts in NYC with lots of seniors and senior pedestrian accidents left out of SPFAs (NYC Comptroller’s “Aging with Dignity” study)
4. Our research question → Do SPFAs reduce senior pedestrian accidents?

### Data

| Type of Data | Datasets | Relevant Fields |
| :---:         |     :---:      |          :---: |
| FARS Data (Fatality Analysis Reporting System) | Accident Dataset | ST_CASE, Date, Latitude, Longitude |
| FARS Data (Fatality Analysis Reporting System)   | Person Dataset   | Age, Sex, Person Type, Date of Death, Drinking involvement, Drug involvement, Related Factors, Dead at scene or not, Injury severity |
| SPFA Data (Senior Pedestrian Focus Areas) | SPFA shapefile | SPFA Name, SPFA Implementation Round, Shape area, Longitude, Latitude |

### Methodology

**Difference-in-difference**
- A statistical technique that attempts to mimic experimental research by studying the differential effect of a treatment on a 'treatment group' versus a 'control group'.
- Our treatment group: 41 SPFAs (areas in blue on the map)
- Our control group: all other parts of the city (areas in white on the map)

Compare trends in senior pedestrian accident rates in SPFAs over time with trends in parts of the city outside SPFAs:
 - If our analysis shows a significant change in trends in SPFAs post-treatment (after SPFA implementation), then our analysis will suggest that SPFAs have had a causal effect on improved safety for senior pedestrians. 
 - If, on the other hand, pedestrian accident rates see similar trends in SPFAs and in non-treated parts of the city, then the City may need to readjust its methodology for selecting SPFAs or infrastructure improvement projects.

### Initial Result


Accidents Decline After Program Implementation          |    Most Senior Involved Accidents Occur Outside SPFAs
:-------------------------:|:-------------------------:
![](https://raw.githubusercontent.com/jzhou60/website_tester/master/Picture2.png)  |  ![](https://raw.githubusercontent.com/jzhou60/website_tester/master/Picture3.png)


![](https://raw.githubusercontent.com/asilayi/Senior-Pedestrians-in-NYC-A-Diff-in-Diff-Approach-to-Evaluating-Safe-Streets-for-Seniors/master/pedestrian%20accident.gif) 

![](https://raw.githubusercontent.com/asilayi/Senior-Pedestrians-in-NYC-A-Diff-in-Diff-Approach-to-Evaluating-Safe-Streets-for-Seniors/master/senior%20pedestrian.gif)


### Tableau embedding

<iframe src="https://public.tableau.com/profile/sam.b.#!/vizhome/aging_15602219800680/Sheet1" width="800" height="600" ></iframe>
