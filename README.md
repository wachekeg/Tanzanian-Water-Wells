# Tanzania Water Well Project
## Introduction
This project aims to utilize machine learning and data visualization to predict the operating condition of a waterpoint for each record in the dataset, and to identify potential issues with existing water well projects, in order to promote access to clean, potable water across Tanzania.

## Problem Statement
While recognizing Tanzania's recent efforts to enhance clean water accessibility, the UN-Habitat acknowledges that a significant portion of the population still lacks safe water access. To address this, an initiative is being proposed to evaluate the distribution of wells in Tanzania and assess the functionality of water pumps in existing wells. The wells in Tanzania can be categorized as functional, non-functional, or in need of repair.


## Objectives

### Primary Objective:
- Deliver accurate predictions regarding the operational status of wells.

### Specific Objectives:
- Identify installers resulting in the most nonfunctional waterpoint pumps.
- Determine how extraction type influences operational status of a water pump
- Identify where most non-functional water pumps are located in Tanzania.
- Identify the proportions of functional, non-functional and pumps in need of repair


## Data Source
The data used in this analysis was provided by Taarifa Tanzania, and downloaded from *Driven Data* Website.
The target Variable is **status_group**, which is a categorical class indicating whether a well is functional, non-functional or in need of repair:
- functional: The waterpoint is operational, and no repairs are needed.
- functional needs repair: The waterpoint is operational but needs repairs.
- non-functional: The waterpoint is not operational.

## Data Understanding
The following set of information was provided about the waterpoints:

- amount_tsh - Total static head (amount water available to waterpoint)
- date_recorded - The date the row was entered
- funder - Who funded the well
- gps_height - Altitude of the well
- installer - Organization that installed the well
- longitude - GPS coordinate
- latitude - GPS coordinate
- wpt_name - Name of the waterpoint if there is one
- basin - Geographic water basin
- subvillage - Geographic location
- region - Geographic location
- region_code - Geographic location (coded)
- district_code - Geographic location (coded)
- lga - Geographic location
- ward - Geographic location
- population - Population around the well
- public_meeting - True/False
- recorded_by - Group entering this row of data
- scheme_management - Who operates the waterpoint
- scheme_name - Who operates the waterpoint
- permit - If the waterpoint is permitted
- construction_year - Year the waterpoint was constructed
- extraction_type - The kind of extraction the waterpoint uses
- extraction_type_group - The kind of extraction the waterpoint uses
- extraction_type_class - The kind of extraction the waterpoint uses
- management - How the waterpoint is managed
- management_group - How the waterpoint is managed
- payment - What the water costs
- payment_type - What the water costs
- water_quality - The quality of the water
- quality_group - The quality of the water
- quantity - The quantity of water
- quantity_group - The quantity of water
- source - The source of the water
- source_type - The source of the water
- source_class - The source of the water
- waterpoint_type - The kind of waterpoint
- waterpoint_type_group - The kind of waterpoint

## Exploratory Data Analysis (EDA) Insights
![distribution of variable target](pictures/distribution of variable target.jpg)



## Preprocessing
Data preprocessing was performed to handle outliers and prepare the data for regression, including model fitting.

## Classification Models
Several Classification Models were employed for this Analysis:
- *Logistic Regression* - 

- *Decision Tree* - 

- *Random Forest*- 

## Conclusions
The top-performing model is the baseline XGBClassifier, demonstrating a training accuracy of 85.84% and a test accuracy of 82.09%. Minimal overfitting is observed, with a commendable cross-validation score of 0.819. This model's ability to generalize effectively to new data aligns with the predefined success criteria.

## Recommendations
1. Prioritize repairing non-functional wells to avoid multiple concurrent problems.
2. Distribute wells strategically to prevent overpopulation in specific areas.
3. Utilize the predictive model to prioritize waterpoints according to needs.

## Next Steps
Integrate maintenance records to reflect repairs made to waterpoints, preventing repeated classification as needing repairs. Explore additional classifiers to prioritize maintenance for non-functional waterpoints.
