# DATA ANALYSIS ON  IMAPCT OF COVID-19 PANDEMIC IN NIGERIA

Coronavirus disease (COVID-19) is an infectious disease caused by a newly discovered coronavirus, and it has affected major parts of the world. Nigeria, a West-African country, has also been affected by the COVID-19 pandemic after recording its first case on 27th February 2020.

Nigeria is a country with 37 states - Federal Capital Territory included- and a fast-growing economic environment with about 200 million citizens. COVID-19 has affected several country activities as the country steadily progressed from its first case to shutting down major airports, state-wide lockdown, curfews, and reviving its economy.

In this project data science & analytics skills are used to collect data, explore the data, perform analysis, create visualizations, and generate insights.

# Project Steps

In the course of the analysis the following steps were taken before and during the analysis; 

1). Gathered data from three different sources; ncdc website, and john hopkins github repoitory and covid_external_data repository
* Web scrapped the dataframeusing pd.read_html()
* Dowloaded the files from John Hopkins Data Repository
* Downloaded external data from Covid_external Repository

2). NCDC DATA
* Basic insights derivation form .info(), .describe() and viewed the complete data
* Plotted a bar charts of all the states affected to number of confirmed cases, no of discharged cases and number of deaths
* Performed correlation analysis using scatterplots and relplots
* Observed the distribution of confirmed cases

3). John Hopkins Data
* There are three subdivisions of the data; the nuber of confirmed cases, discharged cases and death cases. 
* Exttracted and combined into a single dataframe
* Basic insights derivation form .info(), .describe() and data.head()
* Used the pd.melt() function to convert all the confirmed, discharged and death date features into one date feature mapping to the date value
* Merged the three frames in step two(2)
* Converted the date object to datetime using pd.to_datetime()
* Created and added Active cases feature by subtracting the deaths and discharged features from the confirmed features
* Extracted Nigeria's data
* Plotted a line graph of date to all three cases (i.e, confirmed,discharged and deaths)
* Created and added infection rate feature using the diff() function on the confirmed cases
* Plotted date to infection rate
* Used masking to get date with maximum infection rate

4). External Data
 
 a). Covid External Data (Indexes)
* Basic insights derivation form .info(), .describe() and viewed the complete data
* Group data by region
* Merge the data with the ncdc data
* Correlation analysis
* Used nlargest function to get top 10 confirmed, discharged and deaths cases
* Plotted cases of top 10 CCVI index and population density
* Scatter plot of deaths and epidemiology index and fit a regression line on it

 b). Quarterly GDP Analysis
* Used the melt function to get the gdp for all the years from 2014-2020 and splitted them into quarters
* Plotted a bar chart to show GDP for all the years into the quarter subplots

 c). Budget Analysis
* Basic insights derivation form .info(), .describe() and viewed the complete data
* Used jointplot to visualize relationship between initial and revised budget
* Used seaborn barplot to plot a bar chart for the states and their initial and revised budget
* Computed average percentage decrease in the budget across all states in Nigeria
* Extracted state state with the minimum percent change
* Extracted state state with the maximum percent change

# Insights

* The top 10 states with the highest number of confirmed cases are Lagos with	58713 cases, FCT with 19841 cases, Kaduna 9068 cases, Plateau 9060 cases, Rivers 7169 cases, Oyo 6855 cases, Edo 4907 cases, Ogun 4680 cases, Kan 3967 cases,and Ondo 3248 cases.
* The top 10 states with the highest discharged cases are Lagos with 56990, FCT 19104, Plateau	9002, Kaduna 9000, Rivers 7040, Oyo 6729, Edo 4715, Ogun 4627, Kano	3849, and Kwara	3067
* The top 10 death cases are Lagos with 439, Edo	185, FCT 166, Oyo 124, Kano	110, Rivers	101, Delta 71, Kaduna 65, Ondo 6, Plateau 57
* Maximum infection rate is 2464 we look further to discover when this occured
* The date with the maximum infection rate was on the 23rd of january 2021 with an infection rate of 2464.
* The average cummmulative gdp is highest at the third quarter
* The year with the highest total GDP was year 2019 and the lowest being 2020 most likely because of the pandemic (COVID-19)
* The analysis from the initial and revised budget data shows that the average percentage budget drop in Nigeria across all states is approximately 30%
* katsina had the lowest percentage change of about 13% from 344Bn to 213Bn 
* Cross River had the highest percentage change of about 87% from 1.1trn to 147bn
* Areas with low CCVI have relatively high number of confirmed cases
* Lagos has the highest budget prior to the pandemic with 1.7trn and after the revised budget which was approximately a 45% decrease from the year before was 920bn
* ALL COVID-19 INDEX INTERPRETATION
* The COVID-19 Community Vulnerability Index (CCVI) allows us to leverage the power of data to understand how and why communities are vulnerable, so we can develop solutions to help them. © 2020 Surgo Ventures.
* The Fragility Index is the minimum number of patients whose status would have to change from a nonevent to an event that is required to turn a statistically significant result to a non-significant result. The smaller the Fragility Index, the more fragile the trial's outcome.
* The Aging Index refers to the number of elders per 100 persons younger than 15 years old in a specific population. This index increases as population ages.
* Health Care Index is an estimation of the overall quality of the health care system, health care professionals, equipment, staff, doctors, cost, etc. ... It is similar to a health care index, but it raises more exponentially.
* It includes the study of the attack rate of the various diseases (incidence) and the number of people suffering from each condition at any one time (prevalence). Industrial and environmental health problems are also an important aspect of epidemiology.
* SEIFA, or Socio-Economic Indexes for Areas, is a number, or series of 4 numbers, which describe the relative level of socio-economic advantage or disadvantage in an area. Advantage is defined in terms of “access to material and social resources and ability to participate in society
* Population density: Since March 2020, many countries around the world have been experiencing a large outbreak of a novel coronavirus (2019-nCoV). Because there is a higher rate of contact between humans in cities with higher population weighted densities, Covid-19 spreads faster in these areas. 
*  Urban Mobility Index that assesses the mobility of leading cities and tells us about the infrastructural preparedness of the cities for the future. It provides policymakers and transportation experts with a detailed view of the transportation capability and patterns of the city. In the age of interconnected technological advances in the modes of transportation, mobility will be the lifeline of a city.
* While disease outbreaks and other acute public health risks are often unpredictable and require a range of responses, the International Health Regulations (2005) (IHR) provide an overarching legal framework that defines countries’ rights and obligations in handling  public health events and emergencies that have the potential to cross borders.


# Future Work
Analysis should be extended to the following:
* Impact should extend to other economic factors like education 
* Petroleum sector
* Agricultural sector
* Climatic evaluation
* Stock market and the net impact on top institutions.


# Standout Section
* Performed more bivariate analysis on all dataset
* Maximized the groupby tool to extract different kinds of dataframe for analysis, especially in the case of region and index analysis 
* Used masking to extract particular information about a desired value like the states with the minimum and maximum percentage budget change
* Created features to help get deeper insights like getting the Active cases in the John Hopkins data and percentage decrese in budget
* Used regression line to validate correlation
* Drew insights on the effects of covid-19 on oil prices
