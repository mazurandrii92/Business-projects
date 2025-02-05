
# A/B Testing of Landing Page Designs for a Travel Agency

## Project Overview

This project analyzes A/B testing data for two versions of a landing page design for a travel agency. The goal is to determine which version performs better in terms of two key business metrics:
1. **Conversion Rate**: The proportion of visitors who make a purchase.
2. **Average Purchase Value**: The average revenue generated per purchase.

The analysis uses Python to:
- Preprocess and clean the data.
- Perform exploratory data analysis (EDA) to understand trends and distributions.
- Compute cumulative metrics to track the stabilization of results over time.
- Perform statistical tests to determine the significance of observed differences.
- Visualize key findings to support business decisions.

## Repository Structure

- `notebook.ipynb`: Jupyter Notebook containing the entire analysis, including data processing, visualization, and statistical testing.
- `data/ab_data_tourist.csv`: The dataset used in this analysis.

## Dataset Description

The `ab_data_tourist.csv` file contains the following columns:
- `user_id`: Unique identifier for each user.
- `group`: The group assignment for the user (`A` for the control group, `B` for the test group).
- `date`: The date of the user's activity.
- `purchase`: Binary value (1 if the user made a purchase, 0 otherwise).
- `price`: The purchase value in rubles (only available if `purchase = 1`).

## Key Steps in the Analysis

1. **Data Preprocessing**:
   - Remove users who appear in both groups.
   - Convert date columns to the appropriate data type.

2. **Exploratory Data Analysis (EDA)**:
   - Analyze conversion rates and average purchase values for both groups.
   - Track the cumulative stabilization of metrics over the experiment period.

3. **Statistical Testing**:
   - Use the Shapiro-Wilk test to assess normality.
   - Apply appropriate statistical tests (t-test or Mann-Whitney U test) to compare metrics between groups.

4. **Visualization**:
   - Plot cumulative metrics and their trends over time.
   - Highlight confidence intervals for key metrics.

## Results Summary

- **Conversion Rate**: No statistically significant difference between Groups A and B.
- **Average Purchase Value**: Statistically significant difference observed, with Group B showing a higher average purchase value.

### Recommendation:
The landing page design for **Group B** is recommended, as it generates higher revenue while maintaining a similar conversion rate.

## Requirements

- Python 3.8 or higher
- Libraries: pandas, numpy, matplotlib, scipy


## Author

- [Andrii Mazur](https://github.com/mazurandrii92)

