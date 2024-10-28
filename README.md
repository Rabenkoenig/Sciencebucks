# Sciencebucks

## Project Overview

This project focuses on analyzing and predicting user responses to various marketing offers using the dataset provided by Starbucks. We conducted exploratory data analysis (EDA), built predictive models, and gained insights into user engagement with marketing offers. The goal of this analysis is to understand which user demographics are most responsive to specific offer types and to provide recommendations for improving marketing strategies.

## Dataset

The data provided by Starbucks consists of user profiles, promotional offers, and offer-related events. The key datasets include:

- **Profile Dataset**: Contains demographic information such as age, gender, and income.
- **Portfolio Dataset**: Describes the offer types, rewards, difficulty, and communication channels.
- **Transcript Dataset**: Logs user interactions with offers (e.g., offer received, viewed, completed).

These datasets were merged to provide a comprehensive overview of how users responded to different offers.

## Analysis Steps

1. **Exploratory Data Analysis (EDA)**
   - We calculated several metrics, such as Received-to-View Rate (74.98%), View-to-Completion Rate (65.07%), and Overall Completion Rate (48.79%). These metrics provide insights into user interactions with different offers.

2. **Modeling**
   - We used a Random Forest Classifier to predict user response to offers. After fine-tuning the model using GridSearchCV, the best parameters were identified, and the model achieved an accuracy of 91%.
   - Feature importance analysis highlighted that `event_offer received` and `event_offer viewed` were the most significant features influencing offer completion.

3. **Evaluation**
   - We evaluated the model using metrics such as accuracy, precision, recall, and ROC-AUC scores.
   - The confusion matrix showed a high precision for predicting non-completion (90%), but there was a need for further improvement in identifying users who completed the offers.

## Key Findings

- **Important Factors**: The most important predictors of offer completion were whether the user received or viewed the offer.
- **Channel Effectiveness**: The web channel was the most effective in driving offer completions, followed by mobile and email.
- **Demographic Insights**: Younger users ("Youth" and "Young Adults") were more likely to engage with and complete offers compared to older demographics.

## Challenges and Improvements

- **Offer Response Attribution**: A key challenge was correctly attributing which channels and offer types had the most influence on users. This is crucial for optimizing marketing efforts and budgets.
- **Recommendations**: Future improvements include integrating user location data and analyzing the effect of seasonal variations. Exploring different combinations of marketing channels may also reveal synergies that boost engagement.

## Links
- **[Blog Post](https://rabenkoenig.github.io/Sciencebucks/)**: Published summary of the analysis and findings.

