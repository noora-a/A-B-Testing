# A/B Testing Analysis Project

## Table of Contents

- [Installation](#installation)
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Analysis](#analysis)
- [Results](#results)
- [Conclusion](#conclusion)

## Installation <a name="installation"></a>

This project requires the following Python libraries:

- pandas
- numpy
- matplotlib
- seaborn
- scipy
- statsmodels
- jupyter

You can install these dependencies using:

```bash
   pip install pandas numpy matplotlib seaborn scipy statsmodels jupyter
   ```

## Project Overview <a name="project-overview"></a>

This project analyzes the results of an A/B test conducted by an e-commerce website to determine whether a new web page design improves user conversion rates compared to the existing design. A/B testing helps evaluate changes in a controlled environment to make data-driven decisions.

The dataset includes user interactions with both the old and new pages, including conversion outcomes. The goal is to decide whether to implement the new page, retain the old page, or continue testing.
The project is structured into three parts:

### Part I - Probability:

> - Calculate and compare the conversion probabilities for users shown the old and new pages.
> - Use these probabilities to understand if there is a baseline difference in conversion rates between the two pages.

### Part II - A/B Test:

> - Perform hypothesis testing to determine if the new page leads to a statistically significant improvement in conversion rates over the old page.
> - Employ bootstrapping techniques to simulate sampling distributions and calculate p-values for hypothesis testing.

### Part III - Regression:

> - Apply logistic regression analysis to confirm the findings from the A/B test.
> - Examine the interaction between the page variant and other factors, such as the country of the users, to see if they influence conversion rates.

Through these steps, the analysis provides a comprehensive assessment of the new web page's effectiveness, aiding the company's decision on whether to implement the new design.

## Dataset <a name="dataset"></a>

The dataset `ab_data.csv` contain information about the user interactions with two different versions of a website. The key columns in the dataset include:

- `user_id`: Unique identifier for each user.
- `group`: The group to which the user was assigned (`control` or `treatment`).
- `landing_page`: The version of the landing page the user saw.
- `converted`: Whether the user completed the desired action (e.g., made a purchase).
The dataset `countries.csv` contain information about the countries where user interactions sre from. The key columns in the dataset include:
- `user_id`: Unique identifier for each user (to join with ab_data.csv).
- `country`: The country of the user.


## Analysis <a name="analysis"></a>

The analysis involves the following steps:

1. **Data Cleaning and Preprocessing:** Handling missing values, data transformation, and splitting the dataset into control and treatment groups.
2. **Exploratory Data Analysis (EDA):** Visualizing the data to understand distributions and trends.
3. **Hypothesis Testing:** Conducting statistical tests (e.g., t-test, chi-squared test) to compare the performance metrics between the control and treatment groups.
4. **Results Interpretation:** Drawing conclusions from the statistical tests and determining if the changes made to the website are statistically significant.

## Results <a name="results"></a>
In the analysis, the following findings were observed:

- The treatment group exhibited a slightly higher conversion rate compared to the control group.
- However, the difference in conversion rates was not statistically significant, indicating that the observed difference could be attributed to random chance.
- Based on the statistical tests, it was concluded that the changes made did not have a significant impact on the conversion rate.

## Conclusion <a name="conclusions"></a>
This project provided a detailed analysis of A/B test results, offering insights to help make data-driven decisions. The notebook serves as a guide for performing similar analyses on other A/B test datasets.


---

