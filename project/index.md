---
date: 2021-06-16
title: "Analysis of Covid-19 Vaccination Rates in Different Races"
linkTitle: Vaccination Rate Analysis
tags: ["project", "reu", "COVID-19"]
description: "With the ready availability of COVID-19 vaccinations, it is concerning that a suprising large portion of the U.S. population still refuses to recieve one. In order to control the spread of the pandemic and possibly even erradicate it completely, it is integral that the United States vaccinate as much of the population as possible. Not only does this require ensuring that everyone who wishes to be vaccinated recieves a vaccine, it also requires that those who are unwilling to recieve the vaccine are persuaded to take it. The goal of this report is to analyze the demographics of those who are hesitant to recieve the vaccine and find the reasoning behind their decision. This will make it easier to properly persuade them to recieve the vaccine and aid in raising the United States' vaccination rates."
author: Ololade Latinwo
github_url: https://github.com/cybertraining-dsc/su21-reu-375/edit/main/project/index.md
resources:
- src: "**.{png,jpg}"
  title: "Image #:counter"
---

[![Check Report](https://github.com/cybertraining-dsc/su21-reu-375/workflows/Check%20Report/badge.svg)](https://github.com/cybertraining-dsc/su21-reu-375/actions)
[![Status](https://github.com/cybertraining-dsc/su21-reu-375/workflows/Status/badge.svg)](https://github.com/cybertraining-dsc/su21-reu-375/actions)
Status: draft, Type: Project


Ololade Latinwo, [su21-reu-375](https://github.com/cybertraining-dsc/su21-reu-375), [Edit](https://github.com/cybertraining-dsc/su21-reu-375/blob/main/project/index.md)

{{% pageinfo %}}

## Abstract

With the ready availability of COVID-19 vaccinations, it is concerning that a suprising large portion of the U.S. population still refuses to recieve one. In order to control the spread of the pandemic and possibly even erradicate it completely, it is integral that the United States vaccinate as much of the population as possible. Not only does this require ensuring that everyone who wishes to be vaccinated recieves a vaccine, it also requires that those who are unwilling to recieve the vaccine are persuaded to take it. The goal of this report is to analyze the demographics of those who are hesitant to recieve the vaccine and find the reasoning behind their decision. This will make it easier to properly persuade them to recieve the vaccine and aid in raising the United States' vaccination rates. 


Contents

{{< table_of_contents >}}

{{% /pageinfo %}}

**Keywords:** tensorflow, example. 

## 1. Introduction

It has been shown by several economic and health institutions that rates COVID-19 in the United States have been among the highest in the world. Estimates show that about 10 million people have been infected and over a quarter of a million have died in the U.S. by the end of November 2020 [^1]. Fortunately, several pharmaceutical companies such as Pfizer, Moderna, and Johnson & Johnson have managed to create a vaccine by the end of 2020, with several million Americans being given the vaccine by early March. Interestingly, it appears that despite the ready availability of vaccines, a sizeable portion of the population has no intention of receiving either their second does or either dose at all. Voluntarily receiving the COVID-19 vaccine is integral to putting the pandemic to an end, so it is important to explore which demographics are hesitant to receive their vaccine and explore their reasons for doing so. In this project, the variables that will be examined are age, sex, race, education level, location within the United States, and political affiliation.    


## 2. Data Sets

The first of these larger data sets are the results from a study done in the Journal of Community of Health done by Jagdish Khubchandani, Sushil Sharma, James H. Price, Michael J. Wiblishauser, Manoj Sharma, and Fern J. Webb. In this study, participants of a variety of backgrounds were given a questionnaire regarding whether or not they were likely or unlikely to receive the COVID vaccine. The variables included in the study and explored in this project are sex, age group, race, education level, regional location, and political affiliation. The raw data for this study is not available, however, the study has published the results as percentages. The second and third data sets are two maps of the United States that are provided by the CDC and illustrate the estimated rates of vaccine hesitancy and vaccination progress. Additionally, the United States Census Bureau provided a breakdown of vaccine hesitancy and progress by certain variables, of which age, sex, race and ethnicity, and education level are explored in this project. Like the study done by the Journal of Community Health, the raw data is not available, but percentages are available for each variable.  

### 2.1 COVID-19 Vaccination Hesitancy in all 50 States by County

![Figure 1](https://github.com/cybertraining-dsc/su21-reu-375/blob/b624e0213bad00132fe7ec9762730466aa4210b3/Pictures/USA%20Vaccine%20Hesitancy.jpg)

**Figure 1:** An image of the United States illustrating the percentage of adults who are hesitant to recieve a vaccine for COVID-19[^2].

### 2.2 Vaccination Rates by Demographic

![Figure 2a](https://github.com/cybertraining-dsc/su21-reu-375/blob/b89d46fedf16c94b543512c2e1999a1d6e2d4baa/Pictures/Vaccination%20Rate%20by%20Age.jpg)

![Figure 2b](https://github.com/cybertraining-dsc/su21-reu-375/blob/b89d46fedf16c94b543512c2e1999a1d6e2d4baa/Pictures/Vaccination%20Rate%20by%20Education%20Level.jpg)

![Figure 2c](https://github.com/cybertraining-dsc/su21-reu-375/blob/b89d46fedf16c94b543512c2e1999a1d6e2d4baa/Pictures/Vaccination%20Rate%20by%20Race%20and%20Ethnicity.jpg)

![Figure 2d](https://github.com/cybertraining-dsc/su21-reu-375/blob/b89d46fedf16c94b543512c2e1999a1d6e2d4baa/Pictures/Vaccination%20Rate%20by%20Sex.jpg)

**Figures 2a-d**: Images of vaccine hesitancy rates by certain demographics [^2].

### 2.3 COVID-19 Vaccination Rates in all 50 States 

![Figure 3](https://github.com/cybertraining-dsc/su21-reu-375/blob/e13597076f290e67ddc888ec8ac2a7f6fbf8a3ad/Pictures/USA%20Vaccine%20.jpg)

**Figure 3:** An image of the United States illustrating the percentage of adults who have recieved at least one dose of the COVID-19 vaccine[^3].

### 2.4 Vaccination Rates in all 50 States 

![Figure 4a](https://github.com/cybertraining-dsc/su21-reu-375/blob/4c274d9eff61ea7ed38e57202150b8f1222eef09/Pictures/Hesitancy%20Rate%20by%20Age.jpg)

![Figure 4b](https://github.com/cybertraining-dsc/su21-reu-375/blob/4c274d9eff61ea7ed38e57202150b8f1222eef09/Pictures/Hesitancy%20Rate%20by%20Education.jpg)

![Figure 4c](https://github.com/cybertraining-dsc/su21-reu-375/blob/4c274d9eff61ea7ed38e57202150b8f1222eef09/Pictures/Hesitancy%20Rate%20by%20Race%20and%20Ethnicity.jpg)

![Figure 4d](https://github.com/cybertraining-dsc/su21-reu-375/blob/4c274d9eff61ea7ed38e57202150b8f1222eef09/Pictures/Hesitancy%20Rate%20by%20Sex.jpg)

**Figures 4a-d**: Images of vaccine hesitancy rates by certain demographics

### 2.5 Results of the Study Done by the Journal of Community Health

![Figure 5a](https://github.com/cybertraining-dsc/su21-reu-375/blob/35296bc3e854e979a0798c57e3d8557e430519a6/Pictures/1.jpg)
![Figure 5b](https://github.com/cybertraining-dsc/su21-reu-375/blob/35296bc3e854e979a0798c57e3d8557e430519a6/Pictures/2.jpg)
![Figure 5c](https://github.com/cybertraining-dsc/su21-reu-375/blob/35296bc3e854e979a0798c57e3d8557e430519a6/Pictures/3.jpg)


**Figure 5a-c**: Relevant results for the explored variables from a study in vaccine hesitancy rates done by the Journal of Community Health


## 3. Results

### 3.1 Race

In the study done by the Journal of Community Health, Black Americans are shown to have the highest rate of vaccine hesitancy at 34% with White Americans not very far behind at 22%[^1]. Additionally, Asian Americans have the lowest rate of hesitancy at 11%[^1]. Similar results can be seen in the data provided by the US Census Bureau, with Black and White Americans having the highest two vaccination hesitancy rates, however they are shown to be very close, at 10.6% and 11.9%, respectively[^4]. In Addition, Asian Americans are once again shown to have the lowest vaccination rates at as low as 2.3%[^4]. This information correlates with the data provided by the US Census Bureau, which shows that Black Americans have the lowest rate of vaccination at 72.7% and Asian Americans have the highest rate of vaccination of 94.1%[^4].

### 3.2 Sex

In the study done by the Journal of Community Health, men and women are shown to have very similar rates of vaccine hesitancy at 22% for both groups[^1]. This can also be seen in the data provided by the US Census Bureau with women having a hesitancy rate of 10.3% and men having a barely higher rate of 11.3%[^4]. This goes along well with the vaccination rates provided by the US Census Bureau, which shows that men and women have vaccination rates of 81.4% and 80.5%[^4].

### 3.3 Age

The age ranges for both studies are grouped slightly differently, yet, interestingly enough, both data sets show two completely different age groups having the highest rate of hesitancy. In the Journal of Community Health study, the 41-60-year-old group is shown to have the highest rate at 24%[^1]. Yet, in the US Census Bureau's data, ages 25-39 have the highest hesitancy rate at 15.9%[^4]. Because it has a much larger sample size, it is safer to assume that the US Census Bureaus data is more correct in this case. However, both data sets show that seniors have the lowest hesitancy rates, which makes sense as this age group has the highest vaccination rate of 93%[^4]. 

### 3.4 Education Level

Once again, the education levels are grouped slightly differently with the US Census Bureau not taking account for those with a Master's degree above and the Journal of Community Health grouping together those who have a high school education and those who have not completed high school. However, unlike the previous variable, very similar results are yielded despite the difference. In both studies, those who had a high school education or below had the highest hesitancy rate at 31% in the Journal of Community Health study and 15.7% for those who have less than a high school education and 13.8% for those who have one in the data provided by the US Census Bureau[^1][^4]. This correlates with the vaccination rate data as those who have a high school education or less have the two lowest vaccination rates of 74.3% and 70.9%, respectively[^4]. 

### 3.5 Location

The Journal of Community Health is the only data set that assigns specific percentages to the hesitancy rates to regions of the United States with the Northeast having the highest hesitancy rate of 25%, followed very closely by the West and South at 24% and 23%, respectively[^1]. This leaves the Midwest with the lowest hesitancy rate of 18%[^1]. This is partially reflected by the data displayed in the map of the United States that illustrates the rates of hesitancy made by the Census Bureau, which shows that the rates of vaccine hesitancy are slightly higher in the Northeast, West, and Midwest, with the lowest hesitancy rate in the South[^2]. Once again, due to the much larger sample size, it is safer to assume that the Census Bureau is more correct. 

### 3.6 Political Affiliation

This variable is only seen in the Journal of Community Health study. It shows that vaccine hesitancy is highest in Republicans at 29% and lowest in Democrats at 16%. 

 
## 4. Conclusion

After analyzing the data, a person's sex appears to have no influence regarding a person's willingness to recieve a COVID vaccine. However, the other variables looked at during this study appear to have an influence. One's level of education appears to have great influence over their willingness to take the vaccine. This makes sense as those who are less educated are less likely to understand the significance of vaccinations and how they protect the U.S. population and may also be more vulnerable to false information about the vaccine as they may not have the skills to deduce whether a source is reliable or not. Additionally, the data shows that younger adults are less likely to recieve the vaccine. This is possibly due to the common misconception that young people are not adversely affected by the virus and as a result the vaccine is not necessary, which could be why , according to the US Census Bureau, 34.9% of those who are hesitant to take the vaccine don't believe that they need it[^4]. One's political affiliation had a great influence on whether or not someone would be receptive to the vaccine as there is a 13% difference between the hesitancy rates in Republicans and Democrats[^1]. This is very interesting considering that the region with the greatest Republican presence, the South, has the lowest hesitancy rate while the rest of the regions, which have a smaller Republican presence, have the highest hesitancy rates [^3][^2]. Race is also a significant variable, with Black Americans having the lowest vaccination rates and among the highest vaccination hesitancy rates. This could be due to a number of overlapping factors, such as level of education and past historical events. For example, a majority of Black Americans only have a high school diploma, while a relatively small amount of them have a Bachelor's Degree and as we've seen before, those with a lower level of education are more likely to be hesitant about taking the vaccine[^5]. Additionally, Black Americans have a fairly long history of being used as medical guinea pigs, with the most infamous example being the Tuskeegee syphillis study, which would understandably result in some aversion to new vaccinations from the community[^6]. 

After analyzing this data, it is very apparent that, in order to persuade more Americans to take it, that a significant amount of time and effort be put towards having easily accesible education to the real facts about the COVID vaccine, especially in poorer areas where there people are more likely to have lower levels of education. Additionally, to reduce vaccine hesitancy amongst Republicans, we must stop politicizing the vaccine as well as the severity of COVID-19 and frame the pandemic as a bipartisan matter of public health. Regarding the high vaccination hesitancy amongst Black Americans, there are no short-term fixes as a significant portion of the community has not forgotten about the several transgressions that the United States has committed against them, however, the sooner the United States manages to regain the trust of the Black community, the closer we come to ending this pandemic.  



## 6. Acknowledgments

Special thanks to Yohn J Parra, Carlos Theran, and Gregor Lasweski for supporting this project. 


## 7. References

[^1]: Khubchandani, J., Sharma, S., Price, J.H. et al. 
      COVID-19 Vaccination Hesitancy in the United States: A Rapid National Assessment. 
      J Community Health 46, 270–277 (2021). 
      https://doi.org/10.1007/s10900-020-00958-x


[^2]: Estimates of vaccine hesitancy for COVID-19
      Center for Disease Control and Prevention 
      https://data.cdc.gov/stories/s/Vaccine-Hesitancy-for-COVID-19/cnd2-a6zw


[^3]: Party Affiliation by Region
      Pew Research Center
      https://www.pewforum.org/religious-landscape-study/compare/party-affiliation/by/region/-trend


[^4]: Household Pulse Survey COVID-19 Vaccination Tracker 
      United States Census Bureau  
      https://www.census.gov/library/visualizations/interactive/household-pulse-survey-covid-19-                 vaccination-tracker.html
     
     
[^5]: Black High School Attainment Nearly on Par With National Average
      United States Census Bureau
      https://www.census.gov/library/stories/2020/06/black-high-school-attainment-nearly-on-par-with-           national-average.html
      
[^6]: Washington, Harriet A. 
      Medical Apartheid: The Dark History of Medical Experimentation on Black Americans from Colonial           Times to the Present
      https://www.jstor.org/stable/25610054?seq=1#metadata_info_tab_contents
