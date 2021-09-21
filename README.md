# Starbucks Customer Segmentation using K-Means Cluster Analysis

## Problem Statement

Conducting analysis on a company’s customer base and sending personalized campaigns to high value targets has massive benefits in any industry. Using unsupervised learning, I will implement a K-Means cluster analysis for customer segmentation and targeted marketing outreach for Starbucks. This type of analysis can be used by Starbucks to automate promotional outreach and reward fulfillment, as well as measurement and tracking of spending behaviors and other KPIs.


## Executive Summary

For this project I used [Starbucks customer data](https://www.kaggle.com/ihormuliar/starbucks-customer-data) that includes transactions, demographics and promotional offer data from their rewards program. Companies often do this type of deep dive customer segmentation analysis in order to better understand the purchasing habits of their customers and be able to target specific promotional deals. The dataset includes 306,534 events related to 17,000 customers and 10 event types over the course of 30 days. One of the main tasks of this project was to synthesize these three different datasets for customer segmentation analysis and a deep dive into each cluster for business insights and recommendations.


## Project Workflow

### Part 1: Overview, Data Cleaning & EDA

[1-Overview_Cleaning_&_EDA.ipynb](code/1-Overview_Cleaning_&_EDA.ipynb)

This notebook gives an overview of the project, data cleaning and quality control of each of the 3 datasets, and initial exporatory data analysis (EDA).

#![mias_mask](images/mias_mask.png)

### Part 2: Dataset Merging & RFM Metrics

[2-Merging_&_RFM_Metrics.ipynb](code/2-Merging_&_RFM_Metrics.ipynb)

This notebook includes more data preprocessing, steps taken to aggregate and merge the datasets, as well as RFM (Recency, Frequency, and Monetary) Metrics calculated from the data.

### Part 3: Cluster Analysis

[3-Unsupervised_Learning_&_Clustering.ipynb](code/3-Unsupervised_Learning_&_Clustering.ipynb)

This notebook includes dimensionality reduction with PCA, analysis done to find the number of clusters (k) for K-Means cluster analysis, as well as an attempt at DBSCAN that proved to be not a good application with this dataset.

### Part 4: Post Hoc Analysis and Customer Insights

[4-Post_Hoc_Analysis_&_Conclusions.ipynb](code/4-Post_Hoc_Analysis_&_Conclusions.ipynb)

This notebook includes a post hoc analysis of the 6 clusters in order to build customer personas for each of the segments to be used for marketing and promotional purposes.

## Recommendations

- Segment 0: Don’t bother with many promotions.
- Segment 1: Do well with promos, and have high potential with their incomes and highest $/trans. but they only represent small % of customers.
- Segment 2: Informational offers - if targeting them with a different type of promo make it shorter duration, lower difficulty, but offer a lower reward.
- Segment 3: Discount offers - Loyalty in terms of membership lengths, feel free to send them more difficult offers to complete but with higher rewards.
- Segment 4: BOGO offers but generally have lower # of trans. possibly because of this. Older members with higher incomes, they are likely to redeem rewards so choose difficulty and reward levels accordingly.
- Segment 5: Recent members (<1 year) and not a lot going on. Possibly need more time & demographic info (left a lot of this blank) to better understand their spending habits.

## Final Insights

Clusters are separated by relevant metrics for related marketing decisions to be made with each of the segments by Starbucks. Gender, Income and Age seemed to have less of a direct impact compared to amount $ spent, number of transactions, promotional offers, and length of membership. This work highlighted that the bulk of a data science problem is often the data cleaning and wrangling. There is longer term potential for this project to keep developing these customer segments and iterating through this workflow with even more customer data.


## References
1. Data Source: https://www.kaggle.com/ihormuliar/starbucks-customer-data
2. https://seifip.medium.com/starbucks-offers-advanced-customer-segmentation-with-python-737f22e245a4
3. https://www.barilliance.com/rfm-analysis/
4. https://formation.ai/blog/how-starbucks-became-1-in-customer-loyalty/
5. https://lifetimes.readthedocs.io/en/latest/
6. https://www.natasshaselvaraj.com/customer-segmentation-with-python/
7. https://towardsdatascience.com/find-your-best-customers-with-customer-segmentation-in-python-61d602f9eee6
8. https://www.datacamp.com/community/tutorials/introduction-customer-segmentation-python
9. https://clevertap.com/blog/rfm-analysis/
