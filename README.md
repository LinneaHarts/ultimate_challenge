## Ultimate Ride-share Challenge

This repository contains my answers to the Ultimate Ride-Share coding challenge.

More inforation can be found in [this explanatory pdf][ultimate_data_science_challenge.pdf]

### Part 1: Exploratory data analysis ###

The attached logins.json file contains (simulated) timestamps of user logins in a particular geographic location. Aggregate these login counts based on 15minute time intervals, and visualize and describe the resulting time series of login counts in ways that best characterize the underlying patterns of the demand. Please report/illustrate important features of the demand, such as daily cycles. If there are data quality issues, please report them.

__High Level Findings:__
* I found no data quality issues
* I found a daily cycle with peaks at noon and overnight, and valleys in the mornings and afternoons
* I found that logins rose over the course of a week

More detail can be found in this notebook: [Part 1: Exploratory Data Analysis on Logins][notebooks/Part%201%20Logins%20EDA.ipynb]

-------------

### Part 2: Experiment and Metrics Design ###

The neighboring cities of Gotham and Metropolis have complementary circadian rhythms: on weekdays, Ultimate Gotham is most active at night, and Ultimate Metropolis is most active during the day. On weekends, there is reasonable activity in both cities. However, a toll bridge, with a two way toll, between the two cities causes driver partners to tend to be exclusive to each city. The Ultimate managers of city operations for the two cities have proposed an experiment to encourage driver partners to be available in both cities, by reimbursing all toll costs.

1. What would you choose as the key measure of success of this experiment in encouraging driver partners to serve both cities, and why would you choose this metric?

2. Describe a practical experiment you would design to compare the effectiveness of the proposed change in relation to the key measure of success. Please provide details on:
a. how you will implement the experiment
b. what statistical test(s) you will conduct to verify the significance of the observation
c. how you would interpret the results and provide recommendations to the city operations team along with any caveats.

__High Level Proposal:__
* Key success metric is company profit
* Experiment re-imburses tolls only in the morning and evening, and only for cars without fares, since this risks the least of Ultimate's revenue
* P-test with 95% confidence interval on an increase in Ultimate's profit per driver per shift

For more detail see this notebook: [Part 2: Experiment and Metrics Design][notebooks/Part%202%20Experiment%20and%20Metrics%20Design.ipynb]

-------------

### Part 3: Predictive Modeling ###

Ultimate is interested in predicting rider retention. To help explore this question, we have provided a sample dataset of a cohort of users who signed up for an Ultimate account in January 2014. The data was pulled several months later; we consider a user retained if they were “active” (i.e. took a trip) in the preceding 30 days.

We would like you to use this data set to help understand what factors are the best predictors for retention, and offer suggestions to operationalize those insights to help Ultimate. The data is in the attached file ultimate_data_challenge.json. See below for a detailed
description of the dataset. Please include any code you wrote for the analysis and delete the dataset when you have finished with the challenge.

1. Perform any cleaning, exploratory analysis, and/or visualizations to use the provided data for this analysis (a few sentences/plots describing your approach will suffice). What fraction of the observed users were retained?

2. Build a predictive model to help Ultimate determine whether or not a user will be active in their 6th month on the system. Discuss why you chose your approach, what alternatives you considered, and any concerns you have. How valid is your model? Include any key indicators of model performance.

3. Briefly discuss how Ultimate might leverage the insights gained from the model to improve its longterm rider retention (again, a few sentences will suffice).

__Selected Finding Highlights:__
* Time since last ride is thhe most important driver of retention, so I would recommend giving incentives to riders who go too long without a ride
* Android users are less likely to be retained, so Ultimate might want to look into the usability and performance of their app on Android
* Membership in Ultimate Black drives retention, so marketing it more might help

For more detail see this notebook: [Part 3: Predictive Modeling][notebooks/Part%203%20Predictive%20Modeling.ipynb}