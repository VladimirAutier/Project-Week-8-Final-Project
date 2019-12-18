<img src="https://bit.ly/2VnXWr2" alt="Ironhack Logo" width="100"/>

# Copper Price, a new economic estimator?
*Vladimir Autier*

*Data Analytics, Barcelona, 20.12.19*

## Content
- [Project Description](#project-description)
- [Hypotheses / Questions](#hypotheses-questions)
- [Dataset](#dataset)
- [Cleaning](#cleaning)
- [Analysis](#analysis)
- [Model Training and Evaluation](#model-training-and-evaluation)
- [Conclusion](#conclusion)
- [Future Work](#future-work)
- [Workflow](#workflow)
- [Organization](#organization)
- [Links](#links)

## Project Description

Copper is a commodity that has a broad spectrum of use. It is part of many infrastructure structures and is now used in car batteries among other metals such as lithium or cobalt. Because of it's large impact in our society, a drop or an increase in its price might signify that something is happening in the economy. Moreover, there is this historical belief that the Price of Copper is "an estimator" for how well the global economy is doing.The main objective of this project is to check if the Price of Copper can be an actual estimator of global economy just as the GDP or the Yield Curve. I directed my attention to this topic because the world of commodity is of great interest to me.

N.B: The main country that drives the global economy is China. Thus construction in China could also be an estimator of how well copper, the economy is doing.

## Hypotheses / Questions
* The main question that I asked myself: Can Copper price be considered as an economic estimators of the health of the economy?

* I believe that commodities have and will have still strong implication in the well being of the global economy. Therefore using Copper price to get an insight of how the economy is behaving is interesting. It can be used as an additional tool of controling the economy.

* To anser my original question I decided to compare estimators (economic estimators) with an without the inluence of Copper.
  I want to check if by using Copper as an estimator I can predict with more accuracy the next economic recession.

## Dataset

* The datasets I have used are maily issued from the US federal reserve but also other different website that allowed me to get the price of Copper for a large period of time.

 Most of the data was provided in Excel format or CSV format.

Those are the links were I retrieved the data:

 https://tradingeconomics.com/china/government-debt-to-gdp

 https://data.oecd.org/gga/general-government-deficit.htm#indicator-chart

 https://www.newyorkfed.org/research/capital_markets/ycfaq.html#/interactive

 https://data.worldbank.org/indicator/ny.gdp.mktp.cd

 https://www.macrotrends.net/1476/copper-prices-historical-chart-data

## Cleaning

I have separated my work in 6 different notebooks. Notebooks 1-4 are dedicated to cleaning. I reduce the data sets to a viable format in order for me to perform machine learning. I did not get rid of outliers values as I want all the possible information available. I did drop some missing values, however they did not influence my results.

## Analysis

* I separated my analysis into two steps. I decided to work with 3 main economic estimators :GDP, Yield Curve(Spread) and the Consumer Confidence Index (CCI).

Overview the general steps you went through to analyze your data in order to test your hypothesis.
* Document each step of your data exploration and analysis.
* Include charts to demonstrate the effect of your work.
* If you used Machine Learning in your final project, describe your feature selection process.

## Model Training and Evaluation
*Include this section only if you chose to include ML in your project.*
* Describe how you trained your model, the results you obtained, and how you evaluated those results.

## Conclusion
* Summarize your results. What do they mean?
* What can you say about your hypotheses?
* Interpret your findings in terms of the questions you try to answer.

## Future Work
Address any questions you were unable to answer, or any next steps or future extensions to your project.

## Workflow
Outline the workflow you used in your project. What were the steps?
How did you test the accuracy of your analysis and/or machine learning algorithm?

## Organization
How did you organize your work? Did you use any tools like a trello or kanban board?

What does your repository look like? Explain your folder and file structure.

## Links
Include links to your repository, slides and trello/kanban board. Feel free to include any other links associated with your project.


[Repository](https://github.com/)  
[Slides](https://slides.com/)  
[Trello](https://trello.com/en)  
