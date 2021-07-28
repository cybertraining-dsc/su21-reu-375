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

It has been shown by several economic and health institutions that rates COVID-19 in the United States have been among the highest in the world. Estimates show that about 10 million people have been infected and over a quarter of a million have died in the U.S. by the end of November 2020 [^1]. Fortunately, several pharmaceutical companies such as Pfizer, Moderna, and Johnson & Johnson have managed to create a vaccine by the end of 2020, with several million Americans being given the vaccine by early March. Interestingly, it appears that despite the ready availability of vaccines, a sizeable portion of the population have no intention of receiving either their second does or either dose at all. Voluntarily receiving the COVID-19 vaccine is integral to putting the pandemic to an end, so it is important to explore which demographics are hesitant to receive their vaccine and explore their reasons for doing so. 


## 2. Data Sets

(It is important to note that the data sets available regarding this topic are technically incomplete due to the coronavirus being an ongoing phenomenon.) The larger data sets used for this project are located in a github folder called "Vaccine Rate Data Sets". The first of these larger data sets are the results from a study done in the Journal of Community of Health done by Jagdish Khubchandani, Sushil Sharma, James H. Price, Michael J. Wiblishauser, Manoj Sharma and Fern J. Webb. In this study, participants of a variety of backgrounds were given a questionnaire regarding whether or not they were likely or unlikely to recieve the COVID vaccine. The variables included in the study and explored in this project are sex, age group, race and ethnicity, marital status, whether or not they had children at home, education level, area and location of residence, and political affiliation. The raw data for this study is not available, however, the study has published the results as percentages. The second of these data sets is a data table comprising of the estimated rates of vaccine hesitancy in each county of the United States provided by the CDC. The third of these data sets is a data table that illustrates vaccination progress in each of the 50 states that is also provided by the CDC. Additionally, the CDC also provided a breakdown of vaccine hesitancy and progress by certain variables, of which age, sex, race and ethnicity, and education level are explored in this project. Like the study done by the Journal of Community Health, the raw data is not available. Thankfully, they did provide percentages for each variable. 

The smaller data sets and associated visualizations for the larger sets will be provided below. 

### 2.1 COVID-19 Vaccination Hesitancy in all 50 States by County

![Figure 1](https://github.com/cybertraining-dsc/su21-reu-375/blob/b624e0213bad00132fe7ec9762730466aa4210b3/Pictures/USA%20Vaccine%20Hesitancy.jpg)

**Figure 1:** An image of the United States illustrating the percentage of adults who are hesitant to recieve a vaccine for COVID-19[^2].

### 2.2 Vaccination Hesitancy Rates by Demographic

![Figure 2a](https://github.com/cybertraining-dsc/su21-reu-375/blob/b89d46fedf16c94b543512c2e1999a1d6e2d4baa/Pictures/Vaccination%20Rate%20by%20Age.jpg)

![Figure 2b](https://github.com/cybertraining-dsc/su21-reu-375/blob/b89d46fedf16c94b543512c2e1999a1d6e2d4baa/Pictures/Vaccination%20Rate%20by%20Education%20Level.jpg)

![Figure 2c](https://github.com/cybertraining-dsc/su21-reu-375/blob/b89d46fedf16c94b543512c2e1999a1d6e2d4baa/Pictures/Vaccination%20Rate%20by%20Race%20and%20Ethnicity.jpg)

![Figure 2d](https://github.com/cybertraining-dsc/su21-reu-375/blob/b89d46fedf16c94b543512c2e1999a1d6e2d4baa/Pictures/Vaccination%20Rate%20by%20Sex.jpg)

**Figures 2a-d**: Images of vaccine hesitancy rates by certain demographics [^2].

### 2.3 COVID-19 Vaccination Rates in all 50 States 

![Figure 3](https://github.com/cybertraining-dsc/su21-reu-375/blob/e13597076f290e67ddc888ec8ac2a7f6fbf8a3ad/Pictures/USA%20Vaccine%20.jpg)

**Figure 3:** An image of the United States illustrating the percentage of adults who have recieved at least one dose of the COVID-19 vaccine[^3].

### 2.4 Vaccination Rates by Demographic 

![Figure 4a](https://github.com/cybertraining-dsc/su21-reu-375/blob/4c274d9eff61ea7ed38e57202150b8f1222eef09/Pictures/Hesitancy%20Rate%20by%20Age.jpg)

![Figure 4b](https://github.com/cybertraining-dsc/su21-reu-375/blob/4c274d9eff61ea7ed38e57202150b8f1222eef09/Pictures/Hesitancy%20Rate%20by%20Education.jpg)

![Figure 4c](https://github.com/cybertraining-dsc/su21-reu-375/blob/4c274d9eff61ea7ed38e57202150b8f1222eef09/Pictures/Hesitancy%20Rate%20by%20Race%20and%20Ethnicity.jpg)

![Figure 4d](https://github.com/cybertraining-dsc/su21-reu-375/blob/4c274d9eff61ea7ed38e57202150b8f1222eef09/Pictures/Hesitancy%20Rate%20by%20Sex.jpg)

**Figures 4a-d**: Images of vaccine hesitancy rates by certain demographics

## 3 Methodology

## 4. Results

### 4.1 Race

### 4.2 Sex

### 4.3 Age

### 4.4 Education Level

### 4.5 Residential Classification, Location, and Political Affiliation

### 4.6 Familial and Marriage Status

 
## 5. Conclusion

A convincing but not fake conclusion should summarize what the conclusion of the project is.


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


[^3]: COVID-19 Vaccination in the United States, Jurisdiction
      Center for Disease Control and Prevention 
      https://data.cdc.gov/Vaccinations/COVID-19-Vaccinations-in-the-United-States-Jurisdi/unsk-b7fc/data


[^4]: Household Pulse Survey COVID-19 Vaccination Tracker 
      United States Census Bureau  
      https://www.census.gov/library/visualizations/interactive/household-pulse-survey-covid-19-vaccination-tracker.html


[^5]:



[^6]:

      
      
