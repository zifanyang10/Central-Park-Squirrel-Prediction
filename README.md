# Can We Predict Whether a Central Park Squirrel Ignores Humans?

This project looks at whether we can predict if a Central Park squirrel will ignore humans based on its traits, behavior, location, time of day, and surroundings.

I completed this project for my CSS Bootcamp final project.

## Research Question

Can we predict whether a squirrel will be recorded as **indifferent to humans** using information about the squirrel and its environment?

## Data

I used two datasets from the 2018 Central Park Squirrel Census:

* [Squirrel Data](https://data.cityofnewyork.us/Environment/2018-Central-Park-Squirrel-Census-Squirrel-Data/vfnx-vebw/about_data)
* [Hectare Data](https://data.cityofnewyork.us/Environment/2018-Central-Park-Squirrel-Census-Hectare-Data/ej9h-v6g2/about_data)

After merging the two datasets, I had **3,014 squirrel sightings** for the analysis.

## Methods

For this project, I:

* Cleaned and merged the two datasets
* Explored patterns in squirrel indifference
* Split the data into training and testing sets
* Created a baseline model
* Built a logistic regression model
* Built a random forest model
* Used five-fold cross-validation to compare model performance

I left out variables that directly described how squirrels reacted to humans, such as `Approaches` and `Runs from`, because including them could make the prediction too easy and lead to target leakage.

## Main Results

* **48.1%** of squirrel sightings were recorded as indifferent to humans.
* Indifference was more common in the **morning** and among **foraging squirrels**.
* Baseline accuracy: **51.9%**
* Logistic regression test accuracy: **59.8%**
* Random forest test accuracy: **63.5%**
* Random forest mean cross-validation accuracy: **64.6%**

The random forest performed the best, although its **100% training accuracy** suggests that it was overfitting the training data.

Overall, squirrel indifference was somewhat predictable, but even the best model still had a lot of room for improvement.

## Notebook

The full analysis, including the code, visualizations, and model results, can be found here:

[`squirrel_indifference_analysis.ipynb`](squirrel_indifference_analysis.ipynb)

## Author

Zifan Yang
