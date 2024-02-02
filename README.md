# Stanford Policing Project

## Project Description
### Data
This project is based on data that was obtained from the Stanford Open Policing Project. Their webiste can be found [here](https://openpolicing.stanford.edu/). In a nutshell, this data contains data pertaining to traffic stops from cities all around the United States. It contains data about the person pulled over, or "subject", such as their age, race, gender, etc. and various pieces of data on why a cop pulled them over and the circumstances and which they did. I decided to use their data for Raleigh, NC as that is the city I go to school in. The data set specific to Raleigh had 29 variables and a little over 800,000 rows of data.

### Process
With this data, I wanted to apply machine learning techniques I had learned in class to see if we could predict both whether a search would be conducted in a traffic stop and the outcome of a traffic stop (warning, citation, arrest). To do this, I had to clean the data, perform exploratory data analysis, and finally apply the modeling techniques.

To model the data, I used Linear Discriminant Analysis, Quadratic Disciminant Analysis, Naive Bayes, Random Forest, and Decision-Tree methods. I had also considered Support Vector Machines, but it was too computationally taxing on my computer. 

### Findings
From my modeling, I found that it can be predicted with an extremely high certaintly (Less than 4% error rate for almost every model) if a search would be conducted during a traffic stop. Interestingly, this was mostly based on the reason someone was pulled over. All of the models for predicting if a search would happen performed similarly well, aside from QDA which had a much higher error rate, which makes sense considering the nature of the data does not fit how that model functions particularly well.

When creating models to predict the outcome of a traffic stop, I found that it was much more difficult to predict. The four models I used (LDA, NB, RF, DT) all accurately predicted the outcome of the traffic stops about 2/3 of the time when using cross validation. This is likely less accurate than when predicting if a search will take place because there are more variables that come into play that I could not account for in this scenario. The interaction between the officer and subject can play a role into the outcome of a traffic stop, as well as things that I had no information for such as if the subject had prior violations or not.

Overall, I found that the models performed as well as I could've hoped considering all the the variables that come into play in a traffic stop. To expand on this project work, I would like to learn more about feature engineering and how it could be applied with this data set. I would also like to learn how to implement multi-model machine learning to see if I could create an even more accurate model. 

## Motivations
I wanted to complete this project to practice applying skills I have learned in the classroom to real-world data. This data set in particular caught my eye because I could use data from my local police department and better understand the trends in data that could apply to my real life if I am pulled over in the future. 

## File Descriptions
### Policing-Data-Cleaning.Rmd
This file contains all the code I used to clean this data set. This includes the use of 4 packages (dplyr, tidyverse, lubridate, zoo) and involves creating variables and removing irrelevant variables to create a final data set.

### Policing-EDA.Rmd
This is the code I used to conduct the exploratory data analysis. The majority of this was visualizing trends in the data using the inspectdf and ggplot2 library. This allowed me to better understand my categorical and quantitative data before modeling the data. I mention some of the findings in this file as well.

### Policing-Machine-Learning.Rmd
This is where I implemented my machine learning methods to create models to predict the outcome of a traffic stop and if a search was conducted or not. I also talk about the results of the models within the file. 
