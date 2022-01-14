# 🕵️ Cardiotoxicity Prediction 🕵️

## Overview 📖
This is a project created for course Machine Learning in Drug Design (MLDD).
The main goal of this project is to find out what TODO

## Installation ⚙️
In order to be able to use the code in this repository it's first necessary to create
new conda environment - this can be done with

`conda create --name <env> --file environment.yml`

After this it's possible to run in main folder

`jupyter notebook`

The `.ipynb` files are located in `implementation` folder.

## Project structure 🏗️
* [`data`](/data) : contains data used to predict cardiotoxicity
* [`implementation`](/implementation) : contains `.ipynb` files used to explore/preprocess/process/visualize data
* [`predictions`](/predictions) : contains `.csv` files with predictions of the best models, used to find out what 
kind of data the models handle well and what not
* [`presentations`](/presentations) : contains `.pptx` files explaining the project and it's assumptions
* [`results`](/results) : contains `.csv` files with different models accuracy for different data types
* [`visualizations`](/visualizations) : contains `.png` files with models accuracy visualizations for different 
data types

## Implementations ⌨️
* [`data_exploration.ipynb`](/implementation/data_exploration.ipynb) : code related to data exploration - finding out 
what's wrong with it, what kind of data needs to be cleaned and what point of cutoff would be the most sufficient
* [`data_preprocessing.ipynb`](/implementation/data_preprocessing.ipynb) : code related to data processing - combining 
different fingerprint types, performing the data cleaning, splitting different fingerprints into smaller parts containing
only subset of features
* [`cardiotoxicity_prediction.ipynb`](/implementation/cardiotoxicity_prediction.ipynb) : code related to cardiotoxicity 
prediction - choosing the best parameters for models, saving results into `results` folder and figuring out what kind of
deep neural network gives the best results
* [`results_visualization.ipynb`](/implementation/results_visualization.ipynb) : code related to result visualization: 
plotting results from `results` folder and displaying them as a plot and saving them into `visualizations` folder
 