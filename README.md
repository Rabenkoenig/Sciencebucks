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

## Project Files

- **notebooks/**: Jupyter notebooks used for data exploration, model development, and analysis.
- **scripts/**: Python scripts for ETL, modeling, and evaluation.
- **data/**: Folder containing profile, portfolio, and transcript datasets.
- **README.md**: This file, providing an overview of the project.
- **offer_analysis.html**: Blog post summarizing the analysis and findings.

## How to Run

1. Clone the repository.
2. Install the required dependencies listed in `requirements.txt`.
3. Run the Jupyter notebooks or Python scripts for different stages of the analysis.

```bash
pip install -r requirements.txt
```

4. Start the Jupyter notebook to explore data or execute the Python scripts.

```bash
jupyter notebook
```

## Libraries Used

- **Pandas**: Data manipulation and analysis.
- **Scikit-Learn**: Machine learning modeling and evaluation.
- **Matplotlib & Seaborn**: Data visualization.

## References

- [1] Scikit-Learn Documentation for Random Forest Classifier.
- [2] Article discussing class imbalance solutions in machine learning.
- [3] Source discussing the impact of different marketing channels on user behavior.

## Acknowledgments

Special thanks to Starbucks for providing the dataset and to the contributors who made this project possible.

