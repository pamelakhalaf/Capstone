# Capstone Project: Prediction of likelihood of recurrence in bladder cancer patients

_Link to corresponding Jupyter Notebook: https://github.com/pamelakhalaf/Capstone/blob/main/Code/Capstone_BladderCancerRecurrence%20(2).ipynb_

## Problem Statement
This project aims to predict likelihood of cancer recurrence in patients diagnosed with bladder cancer. The goal is to understand disease and patient characteristics that are high risk factors and could result in recurrence. The project is based on a bladder cancer patients Kaggle dataset that tracks 118 patients through their journey from intial diagnosis through disease progression when applicable. 

## EDA
The dataset is structured by events with multiple events corresponding to the same patient. To take a look at a patient centric view, we aggregate events that correspond to the same patient and anchor to that dataset for most subsequent analysis. In order to prep the dataset for predictive modeling, here are the changes that were implemented: 
1. Renamed features for added clarity
2. Converted object based features to numerical ones e.g. treatment choice was converted from placebo, thiotepa and pyridoxine to 0,1,2 indicating increasing scale of treatment intensity
3. Created a new feature representing duration on therapy based on the start, stop time points 
4. Converted the number of recurrence feature to a binary class of 0 when no recurrence has taken place and 1 when 1+ recurrences have taken place
5. Eliminated the number of tumors and size of tumors feature due to extensive % of missing values 

## Data Trends 
Prior to predictive modeling, we understand data trends. We plot the distribution of each column feature and the correlation heatmap. From the heatmap, we observe that the smaller the interval duration of being on therapy, the more likely it is that the patient has recurring disease and the higher is their event number.
A positive but weak correlation is observed between the number of the initial tumors and the number of times that patient is likely to have disease recurring. When comparing likelihood of disease recurrence based on treatment received, we notice a disproportionate number of patients that received placebo treatment have had their disease recurr. These trends while interesting need to be further tested through the predictive model.

## Modeling 


## Model Findings 

