# Predicting Winter California Precipitation with Convolutional Neural Networks
Repository for MSDS Residential 2023-2024 Capstone Project.

# Abstract
Predicting winter precipitation in California is crucial for policy decisions, ecosystem health, and inhabitants’ well-being. However, high variability and difficulty in prediction pose significant challenges. This study explores the potential of using a Convolutional Neural Network (CNN) trained on global summer sea surface temperatures (July-October) to forecast winter precipitation (November-March) across northern, central, and southern California. We leverage data from the Community Earth System Model 2 (CESM2) climate simulations for pre-training the CNNs and observational records to fine-tune the CNNs for real-world predictions. Testing on historical data from 1990-2021, the CNNs achieved R2 values of 0.089, 0.311, and 0.336 for the northern, central, and southern regions, respectively. The CNNs outperformed a baseline linear regression model,  which had R2 values of 0.005, 0.029, and 0.108. We also generated saliency maps to identify important sources of predictability around the globe. Our study provides evidence that predictions of California’s hydroclimate can be enhanced through the combination of deep learning and data from large-ensemble climate simulations.  

# Repository Structure

## Data Cleaning
***PRECT_Parser.ipynb***: Loads the response variable (PRECT) and saves results to a .csv file.

***SST_Nino_Parser.ipynb***: Calculates Nino 3.4 Index for simulated data and outputs as .csv file.

***SST_Training.ipynb***: Loads SST and outputs netCDF file (.nc).

***RealWorldData_Parser.ipynb***: Loads and parses SST and PRECT data for real world observations and saves to files.

***Detrend_Data.ipynb***: Detrends SST, PRECT, and Nino 3.4 Index data and outputs new files.

***exploratory_plots.ipynb***: Initial exploratory plots of data.

***netcdf_methods.ipynb***: Exploration of working with netCDF files and methods associated.


## Data Availability
All data is available via Google Drive. The data is initally from the CESM2 Climate Simulator.

## Model Training
The three CNN models (North, Central, and South) are trained via code found in respective notebooks can be found [here](/modeling/Train_CNNs_Simulations).

## Model Fine-Tuning
Tuning and evaluation on Real World Data can be found [here](/modeling/Real_World_Tuning).

## Model Weights
Final model weights can be found [here](/modeling/model_weights).

