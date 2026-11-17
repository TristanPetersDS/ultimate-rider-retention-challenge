# Ultimate Inc. Data Science Challenge: Rider Retention Analysis

This repository contains a comprehensive analysis for the Ultimate Inc. data science challenge. The project is divided into three parts: an exploratory data analysis of user login patterns, the design of an A/B test to measure the impact of a driver incentive program, and the development of a predictive model to identify factors influencing long-term rider retention.

## Part 1: Exploratory Data Analysis of Logins

An initial analysis of user login data was conducted to understand the temporal patterns of demand.

### Key Findings:
- **Peak Activity:** User logins peak during late-night hours (10 PM - 4 AM) and on weekends.
- **Weekly Trend:** There is a clear upward trend in user activity throughout the week, with the highest number of logins occurring on Saturdays.

---

## Part 2: Experiment and Metrics Design

This section outlines a proposed experiment to encourage driver partners to operate in both Gotham and Metropolis by reimbursing toll costs.

- **Key Success Metric:** The primary metric for success is the **percentage of driver partners who complete trips in both cities within a given week.**
- **Experimental Design:** A **controlled A/B test** is proposed, with a control group (no reimbursement) and a treatment group (toll reimbursement).
- **Statistical Test:** A **two-sample z-test for proportions** will be used to determine if the difference in cross-city driving between the two groups is statistically significant.

---

## Part 3: Predictive Modeling for Rider Retention

The core of this project is a predictive model to identify users likely to churn and to understand the key drivers of retention.

### 1. Data Wrangling & EDA

- The dataset was cleaned, and missing values were handled.
- The target variable, **`retained`**, was engineered based on user activity in the 30 days prior to the data pull.
- The overall retention rate was found to be **37.6%**.
- EDA revealed that early user activity (first 30 days), average rating by driver, and the user's city are strong initial indicators of retention.

### 2. Predictive Modeling

- **Models Tested:** Logistic Regression, K-Nearest Neighbors, and Random Forest Classifier.
- **Selected Model:** The **Random Forest Classifier** was chosen for its superior performance and interpretability.
- **Performance:** The model achieved an accuracy of **76%** on the test set.

### 3. Key Predictors of Retention

The Random Forest model identified the following features as the most important predictors of long-term retention:

1.  **Average Distance** in the first 30 days
2.  **Weekday Trip Percentage**
3.  **Average Rating by Driver**
4.  **Average Rating of Driver**
5.  **Trips in First 30 Days**

---

## Actionable Recommendations

Based on the model's findings, the following recommendations are proposed to improve rider retention:

- **Enhance the First-Month Experience:** Since early activity is a strong predictor, create targeted onboarding campaigns to encourage more trips and varied usage (e.g., trying Ultimate Black) in the first 30 days.
- **Proactive Rider Reputation Management:** Implement a system to notify and assist riders whose average rating from drivers begins to drop, as this is a key indicator of churn risk.
- **Replicate Success from King's Landing:** Analyze the factors contributing to the significantly higher retention rate in King's Landing and apply those learnings to other cities.
- **Optimize Surge Pricing Strategy:** For users identified as at-risk, offer targeted incentives like "surge-proof" passes to mitigate the negative impact of frequent surge pricing.

---

## Data

The two data files (`logins.json` and `ultimate_data_challenge.json`) and the
challenge brief were supplied for this take-home exercise and are not
redistributed here. The notebook's saved outputs show every result. To re-run
it, place both files in `data/`.

## License

The code is released under the [MIT License](LICENSE). It does not cover the
challenge brief or the data, which are not included.
