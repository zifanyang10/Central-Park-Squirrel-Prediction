# Can We Predict Whether a Central Park Squirrel Ignores Humans?

This was my final project for the CSS Bootcamp.

I wanted to see if we could predict whether a Central Park squirrel would ignore humans based on things like its behavior, location, time of day, and the environment around it.

## Data

I used two datasets from the 2018 Central Park Squirrel Census: the [Squirrel Data](https://data.cityofnewyork.us/Environment/2018-Central-Park-Squirrel-Census-Squirrel-Data/vfnx-vebw/about_data) and the [Hectare Data](https://data.cityofnewyork.us/Environment/2018-Central-Park-Squirrel-Census-Hectare-Data/ej9h-v6g2/about_data).

After cleaning and merging them, I ended up with 3,014 squirrel sightings.

## What I Did

I first looked at some basic patterns in the data, and then I built two models: logistic regression and random forest.

I also compared them with a simple baseline and used five-fold cross-validation to get a better idea of how well the models were actually doing.

I left out variables like `Approaches` and `Runs from` because they already directly describe how a squirrel reacted to humans, so using them would make the prediction a little too easy.

## Results

Around 48.1% of the squirrels were recorded as indifferent to humans.

I found that squirrels were more often indifferent in the morning, and foraging squirrels were also more likely to be recorded as indifferent.

The baseline accuracy was 51.9%, logistic regression got 59.8%, and random forest did the best at 63.5%. The random forest also had an average cross-validation accuracy of 64.6%.

It did get 100% accuracy on the training data, though, so it was clearly overfitting.

Overall, squirrel indifference was somewhat predictable, but the models still got a lot wrong. Squirrels are apparently not that easy to figure out.

## Notebook

The full analysis, code, graphs, and results are in:

[`squirrel_indifference_analysis.ipynb`](squirrel_indifference_analysis.ipynb)

## Slides

[squirrels_final_project](https://docs.google.com/presentation/d/1vxKHADZ3E2aYeyhUSUrX0cDur0KFlcvkgJHuqlmD8lI/edit?usp=sharing)

## Author

Zifan Yang

