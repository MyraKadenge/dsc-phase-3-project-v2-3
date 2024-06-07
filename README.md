
# Tanzania water well project

<img src="https://github.com/MyraKadenge/dsc-phase-3-project-v2-3/blob/main/images/Well-Water-Homeowner.jpg" alt="water" width="400"/>


# Project overview
Tanzania, the largest country in East Africa with a population of about 59 million, faces significant challenges in providing clean water, with approximately 47% of the population lacking access to safe drinking water. Many existing water points are either in need of repair or have failed altogether. This project aims to develop a classifier for two primary audiences: the Government of Tanzania and organizations focused on resource optimization. For the government, the classifier will identify patterns in non-functional wells and the factors contributing to their failure, helping improve the construction and maintenance of new wells to ensure their longevity. For organizations, the classifier will pinpoint non-functional and repair-needing wells, allowing for better resource allocation and maximizing the impact of efforts to provide clean water access.

# Business understanding and objectives
Tanzania faces water provision challenges due to issues with existing water points, with some wells needing repairs or failing entirely. The analysis aims to:
 1. Identfy which payment methods best contribute to maintenance of the wells.
 2. To distingush the different factors that contribute to functionality of the wells.
 3. To find the best classification method to analyze the dataset


 # Stakeholder:
The primary stakeholders for this project are organizations involved in providing clean water access, including NGOs and the Government of Tanzania. The model's predictions will help prioritize well-maintenance efforts and allocate resources effectively.


# Dataset
Below is an example of some of the features in the dataset:

amount_tsh - Total static head (amount water available to waterpoint)

date_recorded - The date the row was entered

funder - Who funded the well

gps_height - Altitude of the well

installer - Organization that installed the well

longitude - GPS coordinate

latitude - GPS coordinate

wpt_name - Name of the waterpoint if there is one

basin - Geographic water basin

subvillage - Geographic location

region - Geographic location

region_code - Geographic location (coded)

district_code - Geographic location (coded)

lga - Geographic location

ward - Geographic location

population - Population around the well

public_meeting - True/False

recorded_by - Group entering this row of data

scheme_management - Who operates the waterpoint

scheme_name - Who operates the waterpoint

permit - If the waterpoint is permitted

construction_year - Year the waterpoint was constructed

extraction_type - The kind of extraction the waterpoint uses

# Target Variable:
status_group: The functionality status of the water pump (target variable). Categories may include "functional," "non-functional," or "functional needs repair.

#  Data Understanding
The data was sourced from the Taarifa water dashboards which compiles information from the tanzania ministry of water. The dataset encompasses several features related to water pumps including the geographical location, organizations that contsruct them, and manage them, water quality and even the nearby population. The target feature which is the status group has three categories namely functional, non-functional and needs repair.

An example of an analysis done is the region below


 <img src="https://github.com/MyraKadenge/dsc-phase-3-project-v2-3/blob/main/images/region%20image.png" alt="region" width="400"/>

 The above image shows us how Iringa region has the highest number of functional wells.

# Modeling
In our analysis we used classification models to categorize wells into two groups as there was the decision to combine non functional and needs repair into one group called needs repair. The modeling helped me in predicting and understanding the status of the wells and would eventually help the stakeholders in this case the government and NGO's on which wells are located where and which wells are functional and non-functional guiding them on where to allocate resources and which payment methods to use.

# Evaluation
From the three classification models used the XGBoost emerged as the most accurate model as it had an accuracy score of 80% surpassing th eother two models by a few points.
Success of XGBoost: Given the prevalence of categorical data in our model, XGBoost's efficiency in handling such information contributed to its superior performance.

<img src="https://github.com/MyraKadenge/dsc-phase-3-project-v2-3/blob/main/images/model%20images.png" alt="model" width="400"/>


# Conclusion
In conclusion, 
1. 'never pay', 'per bucket', and 'monthly' are the most efficient payment methids when it comes to maintenance of the wells.
2. Age, ground water sources, and  private organisations seem to be the most important factors that contribute to the functionality of the wells.
3. We can see that having a public meeting helps in functioning of the wells. More than 50% wells are functional when there is a public meeting held for the same. Thus, Public meeting is an important factor for the functioning of wells.

