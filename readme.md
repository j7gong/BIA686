# Course BIA686: Applied Analytics in a World of Big Data.

This repository contains the source files for the project of course BIA686.

The objective is to study the topic trends in biomaterial research, especially focus on the social media feature.

## Introduction and Problem Background

A biomaterial is defined as a nonviable material that is deployed in medical devices for the purpose of interacting with biological systems.[1] A great number of biomaterials have been strongly developed in many areas, such as: medicine, biology, chemistry, and materials science. With the development of social media technology, the communications among researchers have undergone great changes. Our objective is to study the emerging topics in biomaterial research in future and investigate whether the social media can be an effective indicator of topic trends.

## Process and Conclusion
### Topic Analysis and Validation
#### a. Overview of dataset
From Web of Science Database, we used keywords of biomaterials and biomedical materials   to generate our datasets, which counts 43480 records in total from 1972 to 2018. Using VOSViewer to create density map, we had a general overview of hottest topics that consist of microstructure and regeneration.
#### b. Topic Extraction 
We utilized two methods to classify the topics. One is the TF_IDF counting which is originated from the combination of keywords and titles. The other is LDA model that is able to create 24 topic groups including a series of topic words in each group. Both results are different from previous teams’ conclusion respectively since the dataset has been changed over time. Also the algorithm of TF_IDF and LDA made a difference on topic classification results.
#### c. Feature Analysis
We explored five features including reviews, citation numbers, funding agency numbers, journal impact factors and publication types. All findings are consistent with that of previous teams.
### Social Media Analysis and Validation
#### a. Scraped and classify the social media sources
The scraped social media can be divided into five different types, which contains google scholar, google trends, youtube search, twitters and blogs. And blogs compose of science blog, scientific american and Plos. For each type, we counted the number of articles or records in terms of topics. Due to the bias of different platforms in social media, there are significant differences among topic distributions.
#### b. Multi Linear Regression Model
Using TF_IDF as the dependent variable in multi linear regression model, with independent variables of citation numbers, funding agency numbers and journal impact factors, we can assess the model by R^2 value to determine the relationship between TF_IDF and other variables. Then added the variable of the social media, we generate R^2 value again to compare it with previous value. With increased R^2 value, we ascertained the effective impact of the social media on TF_IDF that is articulated with the topic trends.
#### c. Time Series Model
Given testified impact of social media in indicating topic trends, we employed time series model to predict the future trend of topics based on google trends and youtube search. The results shows that the topics of adhesion, polymer, bone and regeneration are emerging in forecasting.
## Future Work 
In further improvement of model accuracy, we could also investigate and append the geographical factor into modeling. What's more, we can try multi time series model instead of using univariate time series model for the same purpose.

**References**
1. Ratner, B. D., Hoffman, A. S., Schoen, F. J., & Lemons, J. E. (2004). *Biomaterials science: an introduction to materials in medicine.* Elsevier.
