# Credit Turn Fear Analysis using SCF 2022 Dataset

Overview

This project analyzes financial behaviors, education, income brackets, and clustering patterns of individuals who expressed fear of credit turn-downs using the Survey of Consumer Finances (SCF) 2022 dataset. The insights focus on demography, asset profiles, education levels, and income distribution of the credit-fearful segment and apply unsupervised learning for clustering risk profiles.

Tools and Libraries Used

pandas, numpy, seaborn, matplotlib, plotly, sklearn (PCA, KMeans, StandardScaler), scipy.stats.mstats.trimmed_var

Dataset Summary

Total Records: 22,975

Total Features: 357

Targeted Group for Focused Analysis: 3,839 individuals with TURNFEAR == 1

Key Findings

1. Age Distribution among Credit-Fearful Individuals

Majority are between 35-54 years.

Younger individuals (<35) and older individuals (>65) show relatively lower fear.

2. Racial Distribution

Over 75% of credit-fearful individuals are Black/African American.

3. Income Categories

Fearful individuals are predominantly in the lower-income brackets:

34% in $0-20K

26% in $21-40K

4. Asset vs House Ownership Correlation

Entire dataset: 0.56

Fearful subset: 0.36

Indicates that among credit-fearful, assets do not heavily include home ownership.

5. Education Levels

Less fear among individuals with Bachelor's to Doctorate degrees.

Highest fear recorded among high school and below.

Clustering Analysis

Filtering Criteria

TURNDOWN == 1

NETWORTH < $3,000,000

Records after filter: 1,931

High Variance Features (Trimmed)

Top 5 features selected for clustering:

DEBT, NETWORTH, HOUSES, NFIN, ASSET

Standardization & Dimensionality Reduction

Applied StandardScaler

Used PCA to reduce to 2D for visualization

KMeans Clustering

Best cluster count (based on silhouette score): 3

Cluster Insights:

Cluster 0 (n=1491): Lowest income, assets, and net worth

Cluster 1 (n=366): Mid-tier net worth, house ownership

Cluster 2 (n=74): High earners with significant asset and house value

Visualizations

Bar Plots: Age group, education, income distribution, and race

Heatmaps: Correlation matrices

Box Plots: Outlier detection

Bar Charts: High-variance features

PCA Scatter: Cluster visualization

Business Recommendations

Credit Access Personalization:

Develop tiered credit products for low-income groups (Cluster 0) to minimize rejection fear.

Financial Education Initiatives:

Roll out community-based education especially among those without a college degree to improve credit confidence.

Asset-Backed Lending Reforms:

Reassess credit models to account for non-home assets, especially for Black or minority groups.

Digital Literacy Boost:

Tailor fintech solutions for individuals under 45, who represent the largest fearful demographic.

Targeted Savings & Investment Products:

Offer customized products to help Clusters 0 & 1 grow assets and transition toward Cluster 2 profiles.

Policy Collaboration:

Work with policymakers to design inclusive financial products that consider fear of credit denial as a barrier to access.
