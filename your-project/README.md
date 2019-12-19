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

* Copper is a commodity that has a broad spectrum of use. It is part of many infrastructure structures and is now used in car batteries among other metals such as lithium or cobalt. Because of it's large impact in our society, a drop or an increase in its price might signify that something is happening in the economy. Moreover, there is this historical belief that the Price of Copper is "an estimator" for how well the global economy is doing.The main objective of this project is to check if the Price of Copper can be an actual estimator of global economy just as the GDP or the Yield Curve. I directed my attention to this topic because the world of commodity is of great interest to me.

* N.B: The main country that drives the global economy is China. Thus construction in China could also be an estimator of how well copper, the economy is doing.

## Hypotheses / Questions
* The main question that I asked myself: Can Copper price be considered as an economic estimators of the health of the economy?

* I believe that commodities have and will have still strong implication in the well being of the global economy. Therefore using Copper price to get an insight of how the economy is behaving is interesting. It can be used as an additional tool of controling the economy.

* To anser my original question I decided to compare estimators (economic estimators) with an without the inluence of Copper.
  I want to check if by using Copper as an estimator I can predict with more accuracy the next economic recession.

## Dataset

* The datasets I have used are mainly issued from the US federal reserve but also other different website that allowed me to get the price of Copper for a large period of time.

 Most of the data was provided in Excel format or CSV format.

* Those are the links were I retrieved the data:

 https://tradingeconomics.com/china/government-debt-to-gdp

 https://data.oecd.org/gga/general-government-deficit.htm#indicator-chart

 https://www.newyorkfed.org/research/capital_markets/ycfaq.html#/interactive

 https://data.worldbank.org/indicator/ny.gdp.mktp.cd

 https://www.macrotrends.net/1476/copper-prices-historical-chart-data

## Cleaning

* I have separated my work in 6 different notebooks. Notebooks 1-4 are dedicated to cleaning. I reduce the data sets to a viable format in order for me to perform machine learning. I did not get rid of outliers values as I want all the possible information available. I did drop some missing values, however they did not influence my results.

## Analysis

* I separated my analysis into two steps. I decided to work with 3 main economic estimators :GDP, Yield Curve(Spread) and the Consumer Confidence Index (CCI).

* I used those economic estimators because they are known to be good indicators of how the economy is doing.In other words are we moving into a period of growth or recession. The goal of my analysis was to check if by addind or removing the price of Copper to the equation, the estimation of recession was going to improve or not.

* To perform my analysis before modeling, I worked on the price of Copper over a period of 50 years and looked for patterns and insights. However, I did not get any strong patterns or seasonality which would have helped me to perform a SARIMA model(Time Series). Thus I used an alternative model which is called Prophet and that allows me to predict future prices but also a strong Time Series on the Price of Copper. In order for Prophet to be able to compute information I had to resample the dataset by month. By addopting this strategy of month resampling I had to be consistent with this approach. Therefore, when I used Prophet on the other economic parameters, I encountered an issue with the GDP parameter which was defined every year(Icould not perform a month resampling). In order to overcome this situation and still be consistent with my project I decided not to use the effect on GDP to predict recession.

* With the use of Prophet I was able to predict values for 2020 for each parameter ( CCI,Copper,Yield). Using the predicted values but also existing values I used supervised Machine Learning to test my estimations but also check if copper could improve the accuracy of my model.

## Model Training and Evaluation

* In order to perform Machine Learning in this project I used the 2 or 3 economic parameters to be the elements that will allow me to observe if the economy was in recession or not (the target value). The target value is a boolean value, meaning that it will take a 0 value is the economy is not in recession and a 1 otherwise. 

* In order for me to test if Copper could be considered as a good estimator for detecting recession, I had to perform 2 models, one with the influence of the price of Copper and another one without. As my targeted value is a boolean I decided to perform a random forest & logistic regression algorithm on the data.

* The process that I used for both model  is the following:

- First I trained the model on a portion of the existing values(1970:2006) that I have to test on an other portion of the existing data to check if the model is accurate(2006:2009).I looked at this specific portion because it is the time period where the last economic recession took place. 
- Then I followed the same process but now on all the existing values (train) to test the predicted values that I obtained using Time Series with Prophet.

* I obtained promissing results:

-In the first step of my modeling I observed that by including  the price of Copper as a parameter in the model allows me to perform a more accurated estimation of the economic situation. Moreover, the random forest algorithm performs better than the logistic regression as the F1 score is better with random forest.
-Then I used this intuition to perfrom the same modelling on the predicted values. Again, the price of Copper was helping the model to get better results.

## Conclusion

* With this project I have been able to see that we can consider the price of Copper as a new tool to estimate the evolution of the global economy. Moreover, with this model I have been able to estimate as well how the economy will behave in 2020. According to my results we should not expect a recession. Of course those results are highly hypotethical and we should perform other tests to enhance my analysis.


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
