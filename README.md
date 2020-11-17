# West-Nile-Virus-Chicago


## Problem Statement
West Nile virus is most commonly spread to humans through infected mosquitos. Around 20% of people who become infected with the virus develop symptoms ranging from a persistent fever, to serious neurological illnesses that can result in death.

In 2002, the first human cases of West Nile virus were reported in Chicago. By 2004 the City of Chicago and the Chicago Department of Public Health (CDPH) had established a comprehensive surveillance and control program that is still in effect today.

Every week from late spring through the fall, mosquitos in traps across the city are tested for the virus. The results of these tests influence when and where the city will spray airborne pesticides to control adult mosquito populations.

Representing CDPH, we will develop a model to predict outbreak of West Nile virus in mosquitos so that the City of Chicago can more efficiently and effectively allocate resources towards preventing transmission of this potentially deadly virus.​

## Objective

Predict West Nile virus in mosquitos across the city of Chicago

## Data Dictionary 
The dataset with description, can be found here: https://www.kaggle.com/c/predict-west-nile-virus/ 

## Project Planning
We started by examining the different datasets and coming up with an overall framework on how we should approach the EDA process. We have decided to split up the work based on different features and conduct EDA individually. Next, we will combine the EDAs into one notebook where we will be start modelling. The imbalanced dataset is a key challenge that needs to be address.We then tried different classfication techniques (including Logistic Regression, SVM and KNN). We selected logistic regression as our choice model as it gives the highest ROC score and did hyperparameter tuning to see if we could get an even higher score. 

|Workflow Step|Team Member|Description|
|---|---|---|
|**Project Scoping**|*All*|Define delierable and problem statement.| 
|**Gather Data**|*Sarah*|Download dataset, setup and manage GitHub repository.|
|**EDA**|*Yew Tong*|Look into date, day and weather.|
|**EDA**|*Sarah*|Look into trap, number of mosquitoes, species and spray (2011, 2013).|
|**EDA**|*Tieming*|Look into trap, number of mosquitoes and species (before spray 2007, 2009).|
|**EDA**|*Daiyu*|Look into address, longitude and latitude.|
|**EDA**|*Tieming*|Combine all EDA into one notebook.|
|**Modelling**|*Yew Tong/Sarah*|Test and refine different models.|
|**Conclusion and Recommendation**|*Yew Tong/Sarah*|Cost-benefit analysis.|
|**Read.Me**|*Tieming*|Read.Me write up|
|**Presentation**|*All*|Preparation of presentation slides|




## Model Evaluation

Based on the results of the models, we have chosen logistic regression as our preferred model. Firstly, logistic regression gives a better roc score compared to SVM and KNN. The SVM roc score for 2011 was 0.611, KNN roc score was 0.5 while logistic regression gives a roc score of 0.97. This means that logistic regression provides a better classification of west nile virus compared to SVM and KNN. Secondly, logistic regression allows us to draw meaningful information from its coefficients therefore allowing us to make useful conclusion and recommendations.    



## Conclusion and Recommendation

From the logistic model, the most important factor determining whether a trap had WNV was time. The further away from August, the less likely there is to be WNV, most likely because there are less mosquitoes (as per the EDA). Following this, the next most important features are the species, most notably Culex Pipiens and Resuans. These are the most likely to have WNV. The other species means it's less likely (most likely because if it's Culex Erraticus, for example, it's not Culex Pipiens/Restuans)
The more snow there is, the less WNV there and the higher the wet bulb the less WNV. Traps T900, T903 and T225 are the most likely to have WNV, these are the areas most likely to have WNV.

### Based on the above conclusion, we make the following recommedations:
1. Spraying should be done before and up till August each year. Both EDA and our model suggest that the mosquito population and mosquito carrying virus tends to peak before August. Therefore, spraying would be most effective if it was done before August. After August, the mosquito population begins to dwindle.
2. There might be value to studying the genetic make up of species Culex Pipiens and Restuans, and to manufacture spraying chemicals that could more effectively target Culex Pipiens and Restuans as they are the greatest carrier of the virus.
3. Our model has revealed that the greater the snowfall, the less likely that WNV will be present. Areas/periods that had snowed will have a lower priority for spraying. The budget for spraying can be saved for when WNV will be/going to be most prevalent.
4. During periods that with greater average wind speeds (and therefore less humid), incidence of WNV goes up. Intervention is recommended during these periods, but the efficacy of spraying on a windy day has to be studied further.
5. Areas in the vicinity of traps T900 and T225 will need to be more thoroughly sprayed as these traps observed the greatest incidence of WNV-carrying mosquitoes.




