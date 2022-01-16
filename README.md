# 🕵️ Cardiotoxicity Prediction 🕵️

## Overview 📖
This is a project created for course Machine Learning in Drug Design (MLDD).
The main goal of this project is to find the best approach to predict cardiotoxicity. 

### Initial data 💾
The initial data located in 
[`data/initial`](/data/initial) folder contains of three different fingerprints types:
* Extended-Connectivity Fingerprint
* Klekhota-Roth Fingerprint
* Molecular Access System Fingerprint

### Goals ⚽
As part of the project several goals are set:

- figure out which fingerprint type gives the most accurate predictions.
- test whether mix of different fingerprints types results in more accurate predictions. 
- validate if removal of the *X* least correlated features results in better predictions. 

### Reasons 🤔
In the drug design process, the test compounds may have undesirable consequences, such as blocking the potassium ion 
channel of the hERG gene.

Virtual screening for the prediction of drug-induced hERG-related cardiotoxicity could facilitate, speed up and improve 
the drug discovery process by filtering out toxic drug candidates in the early stages.

### Prerequisites 📝
In order to predict cardiotoxicity firstly data needs to be cleaned as it contains some invalid rows. 

IC50 values need to be mapped to binary values that indicate whether given compound coded by fingerprint is toxic or 
not
* the cutoff level which is used to determine it is set to *10000* nanomoles


## Installation ⚙️
Because this repository uses git lfs you need to clone it using 

`git clone <repository>`

Simply downloading it with `Download ZIP` option on Github will not download whole `.csv` files, and you will need tp
download them separately - that's why using `git clone` is preffered.

In order to be able to use the code in this repository it's first necessary to create
new conda environment - this can be done with

`conda create --name <env> --file environment.yml`

After this it's possible to run in main folder

`jupyter notebook`

The `.ipynb` files are located in [`implementation`](/implementation) folder.

## Project structure 🏗️
* [`data`](/data) : contains data used to predict cardiotoxicity
* [`implementation`](/implementation) : contains `.ipynb` files used to explore/preprocess/process/visualize data
* [`predictions`](/predictions) : contains `.csv` files with predictions of the best models, used to find out what 
kind of data the models handle well and what not
* [`presentations`](/presentations) : contains `.pptx` files explaining the project and it's assumptions
* [`results`](/results) : contains `.csv` files with different models accuracy for different data types
* [`visualizations`](/visualizations) : contains `.png` files with models accuracy visualizations for different 
data types

## Implementation ⌨️
* [`data_exploration.ipynb`](/implementation/data_exploration.ipynb) : code related to data exploration - finding out 
what's wrong with it, what kind of data needs to be cleaned and what point of cutoff would be the most sufficient
* [`data_preprocessing.ipynb`](/implementation/data_preprocessing.ipynb) : code related to data processing - combining 
different fingerprint types, performing the data cleaning, splitting different fingerprints into smaller parts containing
only subset of features
* [`cardiotoxicity_prediction.ipynb`](/implementation/cardiotoxicity_prediction.ipynb) : code related to cardiotoxicity 
prediction - choosing the best parameters for models, saving results into [`results`](/results) folder and figuring out 
what kind of deep neural network gives the best results
* [`results_visualization.ipynb`](/implementation/results_visualization.ipynb) : code related to result visualization: 
plotting results from [`results`](/results) folder and displaying them as a plot and saving them into 
[`visualizations`](/visualizations) folder

## Results 📈
The graphical visualization of the results can be found in [`results`](/results) folder. 