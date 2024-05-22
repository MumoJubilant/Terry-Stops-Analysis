# Terry-Stops-Analysis
" A terry-stop in the United States allows the police to detain an individual briefly based on reasonable suspicion of involvement in criminal activities. Reasonable suspicion is of lower standard than probable cause which is needed for an arrest. When the police stop and search a pedestrian this is commonly known as a stop and frisk. When the police stop an automobile, this is called a traffic stop. If the police stop a motor vehicle on minor infringements in order to investigate other criminal activities, this is known as a pretextual stop."  -Wikipedia


## Project Overview
n Terry v. Ohio, a landmark Supreme Court case in 1967, the court found that a police officer was not in violation of the "unreasonable search and seizure" clause of the Fourth Amendment. Thus was born the notion of "reasonable suspicion", according to which an agent of the police may temporarily detain a person. Terry Stops are stops made of suspicious drivers. We aim to build a classifier to predict whether an arrest was made after a Terry Stop.

## Data Understanding
The dataset source was from a website data.seattle.gov in a file named Terry stops.

The data is grouped into categorical data which includes a record of:
Subject Age Group, Frisk Flag, Stop Resolution, Arrest Flag, Weapon type,
Subject Race, Subject gender, Subject perceived race, Subject ID, 
Officer Gender, Officer Race, Officer Id,
![download](https://github.com/MumoJubilant/Terry-Stops-Analysis/assets/142311442/aedb2f91-6945-4df0-95be-4c3a445a247d)



![download](https://github.com/MumoJubilant/Terry-Stops-Analysis/assets/142311442/6b7a7ecb-9137-494c-b721-0da332060b86)



![download](https://github.com/MumoJubilant/Terry-Stops-Analysis/assets/142311442/bf4b3c4a-c1a2-4b1b-8b56-0263f2dd3c79)

### Main Objectives
I. Build a classifier to predict whether an arrest was made after a terry-stop
II. Investigate whether there is any data that plays a role in making arrests
III. To evaluate and improve models used in predicting arrests
###Specific objectives
Which features are identified as relevant for the binary classifier, considering factors like age, race, arrest flag, gender and frisk flag?
How do arrests vary concerning different features, such as race, gender and age?
What is the outcome of the Data Analysis in terms of understanding the distribution of key variables and relationships?


## Modelling.
### Logistic Regression
When you want to apply this to a binary dataset, what you actually want to do is perform a classification. In our case, we want to fit a logistic regression model to Target using Age, Race, Frisk flag, Subject id and Call type . Since Target, Race, and Sex are categorical, they need to be be converted to a numeric datatype first,fit the model and then model evaluation

Training model with Logistic Regression
Accuracy = 91%
F1 score = 59%

* Training model with Decision Trees
The accuracy of the model shows that it can predict the data 91% correctly after using cross validation for overfitting the model with 99%

* Training the model with Random Forest


* Training and improving the model with XG Boost


* Finally use GridSearchCV to find the best parameters

##Recommendation and Conclusions
###Recommendation.
Check on the male gender of the black American and White races Collect information on the reasons for Arrest to have better understanding of arrests Calculating over the population to get a sense of how the different parameters are affected
The unknown variables need to be reassessed.
Recommend using SMOTE to deal with the class imbalance 

###Conclusions
The different information affecting the arrest during the terry stops have made the models come together in harmony. Logistic regression and decision tree classifier were used to make the model predict the data which showed a 90% accuracy. There was some imbalance in the data due to the difference between the two classes in the target. 
Most of the classes were biased, as leaning to one group of people i.e Male, White and Black or African American
