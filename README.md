# Project 1: World Development Statistics: Is Broadband accessible globally for all?

## Problem Statement

### Question: Is Broadband accessible globally for all?
A nonprofit, “Bridge the Gap,” is dedicated to partnering with large broadband companies abroad by informing and helping them decide to expand internet access and services in low-income areas. “Bridge the Gap” is running for a large grant from a multi-billion dollar corporation that would give the nonprofit funding to support the mission of helping provide broadband access to countries and areas that need it. This large corporation is US-based and not aware of the global impacts of broadband, its importance in low-income areas, and what it can do for countries/populations. The nonprofit's goal is to inform people about the inaccessibility of broadband in low-income countries and, through this, potentially get funds. This large corporation is looking for insight into its decision with data to support it. Our goal as the data scientists that will present this information with “Bridge the Gap” to the corporation is to first answer if Broadband is accessible globally for all, in addition to making recommendations/informing decisions of what countries the funds would go to since that is a requirement for the grant.

### Contents:
- [Background](#Background)
- [Data Import & Cleaning](#Data-Import-and-Cleaning)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Data Visualization](#Visualize-the-Data)
- [Conclusions and Recommendations](#Conclusions-and-Recommendations)

## Background

Since 1998, Broadband has established itself as a leading means to access the internet. 
Broadband is defined as the transmission of wide bandwidth data over a high-speed Internet connection([Source: Verizon](https://www.verizon.com/articles/internet-essentials/broadband-definition/)). Wi-Fi, being similar, provides wireless internet connections; however, the main difference between Wi-Fi and broadband is that broadband can be wireless or wired data and typically provides uninterrupted Internet access, while Wi-Fi may experience more interruptions and signal degradation. 


Broadband has been known to be crucial for accessing information without typical disruption of internet service for things such as teleconferencing, education, and healthcare. Because of its reliability, it has been said to be essential for economic growth and bridging the gap for opportunity in sectors such as education, employment, and healthcare, further positively contributing to economic development and enhancing services for all sectors([Source](https://www2.deloitte.com/us/en/pages/consulting/articles/bridging-the-digital-divide-with-broadband-for-all.html)).

Whether through Broadband or Wifi, in a country like the US, accessing information through the internet can often be done quickly, if not at the touch of our fingertips with the use of smartphones. In 2023, there were 311.3 million internet users in the U.S., with an internet penetration rate of 91.8% of the total population([Source](https://datareportal.com/reports/digital-2023-united-states-of-america)). While this may be true in countries such as the United States, this starkly contrasts many places in the world where internet access remains severely limited due to various factors, one of which is economic development.

A study from Data Reportal showed that approximately 67% of the world's population, equivalent to 5.4 billion people, are online, showing a growth rate of 4.7% since 2022([Source](https://datareportal.com/reports/digital-2023-united-states-of-america)). In this report, it was stated that 93% of people in high-income countries used the Internet compared to 27% in low-income countries ([Source](https://datareportal.com/reports/digital-2023-united-states-of-america)). It is important to note that broadband accessibility also varies on several factors in the global realm, one of them being infrastructure availability, especially in remote or rural areas due to infrastructure limitations; however, once implemented with the appropriate resources, high speed, and reliable internet connection can be feasible([Source](https://www.fcc.gov/consumers/guides/getting-broadband-qa)).

In the study, I will answer the question of whether Broadband is accessible for all globally and demonstrate the potential solutions. I will use various datasets to answer this question, including Gross National Income in Countries, population, and Broadband subscribers per 100 across several countries.

### Background on data
The following data was used in my analysis and was obtained from [Gapminder.com](https://www.gapminder.org/), a non-profit foundation based in Stockholm, Sweden, that aims to promote sustainable global development and enhance understanding of important global trends through the use of reliable data. With guidance from General Assembly, I was able to find this source.

Gross National Income (GNI) per capita in current US dollars - Variable: Gni_per_cap_atlas_method_con2021.csv - Includes data from 1800 to 2050

Population by Country - Variable: Population.csv - Includes data from 1800 to 2100

Broadband subscribers per 100 people - Variable: broadband_subscribers_per_100_people - Fixed broadband subcriptions refers to fixed subcriptions to high-speed access to the public internet(A TCP/IP Connection) at downstream speeds equal to or great than 256 kbit/s.This includes data from 1998 to 2022, as 1998 was the year Broadband was created. Note: I choose to look at Broadband subscribers per 100 people vs all Broadband subscribers due to manageability and more standardization comparison.

## EXECUTIVE SUMMARY 

The purpose of the study was to analyze data on Broadband subscribers per 100, gross national income, and population in global countries to demonstrate their relationships and answer the question of whether broadband is accessible globally for all.

In summary, the answer is no. Broadband is still not accessible globally for all, but it could be beneficial to create broadband infrastructure in certain parts of the world, specifically countries with lower incomes. There are still countries with low access to the internet, specifically countries with low incomes relative to population. 

The way that I decided to approach this was my first, considering the data that I needed to answer the question. I needed to decide between choosing Broadband subscribers per 100 or total broadband subscribers and choosing Broadband  subscribers per 100 because of the manageability and standardization of the data. After deciding what data to use, I began researching to formulate my hypothesis with the data. Based on my research, I hypothesized that it is not accessible for all globally because of the unequal distribution of income according to the population across the countries.

In my data cleaning process, I took the three data sets and identified null values, data types, variable names, and missing data. As I identified the data, I took appropriate measures to clean it by replacing missing data with no values, turning thousands, millions, and billions into floats/integers, changing data types, and dropping certain rows and columns that I considered either irrelevant information to the scope of the project or information that was not applicable for analysis such as empty rows or data that created forecasting predictions since I only needed current data. I mainly wanted to focus on comparing 1998 to 2022 to show the difference since the creation of broadband in both income and population. Then, I merged together to begin the exploratory data analysis process. Finally, I saved my data into their corresponding folders in the data folder of my project.

For my EDA, I decided to take the summary statistics from each data set and apply them to my analysis. I decided to take the gross national income median from 1998 to 2022 and create a separate data table. I took the median to compare median data with broadband data and countries. 

After this, I was interested in finding the top 10 countries with the highest income in 2022 compared to the broadband data in 2022. I found that Switzerland, Luxembourg, Norway, Ireland, the United States, Denmark, Iceland, Qatar, Singapore, and Australia had the highest income in 2022. 

I then was  interested in comparing that with the lowest incomes of countries in 2022, and I found that the Congo Democratic Republic, Central African Republic, Sierra Leone, Afghanistan, Madagascar, Eritrea, Mozambique, Somalia, and Burundi had the lowest incomes in 2022. After this, I wanted to take the global indicator of low income and verify that these countries all fell below the 1045 threshold number using boolean filtering.


From the data, my findings were that…

* There is an unequal distribution of gross national income over the years in global data of all countries.

* Areas with larger populations tend to have higher access to broadband.

* There is a positive correlation between higher income and broadband access. 

* The top 10 countries with the highest income have higher chance of accessing broadband, while the lowest GNI countries have a signficant less amount of access in relation to GNI Per cap.

* The lowest countries fall below the global number indicator of low income of $1045.


Based on my findings, I recommend that countries with less income should be prioritized for the broadband access fund from the large corporation. Countries such as Congo Dem. Republic, Central African Republic, Sierra Leone, Afghanistan, Madagascar, Eritrea, Mozambique, Somalia, and Burundi should be further researched into the feasibility of how broadband access could be implemented, even in high or low-population areas. Overall, Broadband access is important for closing the gap in resources and opportunities for those with limited access. It could potentially be beneficial in the long term for the country's economic development as well.

Limitations

Some of the limitations to this analysis include correlation vs. causation, feasibility in implementing due to government laws for certain countries and assessing other important factors to demonstrate how beneficial it is to have broadband access with other data such as education, healthcare impact, etc. 

Some project limitations include accidentally changing my original income dataset. Originally, my data set broadband needed an additional variable to show. The data was clean, but I saved it as a new file instead. I also had an issue with the top 10 lowest countries because of a null value that was not cleaned. Because of this, I showed 9 countries. Next time, I would also like to divide the incomes of all countries, organizing them between low, median, and high and comparing them all in that way.  

Sources:

Data reportal: https://datareportal.com/reports/digital-2023-united-states-of-america

FCC: https://www.fcc.gov/consumers/guides/getting-broadband-qa

Deloitte : https://www2.deloitte.com/us/en/pages/consulting/articles/bridging-the-digital-divide-with-broadband-for-all.html

Verizon: https://www.verizon.com/articles/internet-essentials/broadband-definition/

https://www.itu.int/itu-d/reports/statistics/2023/10/10/ff23-internet-use/

For python help:  

https://www.perplexity.ai/