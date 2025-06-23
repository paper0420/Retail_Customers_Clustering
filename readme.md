# Customer Segmentation Using RFM and KMeans

This project applies unsupervised machine learning to segment retail customers using transactional data. By transforming raw sales data into RFM (Recency, Frequency, Monetary) metrics and applying KMeans clustering, we identify distinct customer segments that can be used for personalized marketing strategies.

# Objective

## Help retailers:

Understand customer behavior
Improve retention and loyalty
Increase marketing ROI
by identifying key customer groups through clustering analysis.

## Data Preprocessing

Removed invalid or missing CustomerIDs and transactions with negative quantity/price (e.g., returns, cancellations).
Filtered out non-product stock codes and bad debt invoices.
Final dataset retained 77% of the original data, ensuring high-quality input for analysis.

## Feature Engineering

Created SalesLineTotal = Quantity × Price
Aggregated by customer to compute:
Recency (days since last purchase)
Frequency (number of purchases)
Monetary (total spend)
Identified and separated outliers using IQR method.
Applied StandardScaler for normalization before clustering.

## KMeans Clustering

Evaluated optimal clusters (K) using Elbow Method and Silhouette Score
Selected K = 4 as optimal number of segments
Used 3D scatter plots and violin plots to visualize and interpret clusters

## Cluster Insights

Cluster Label Description Action Recommendation
0 Retail High spend, frequent but less recent buyers Loyalty programs, re-engagement
1 Re-Engage Low-value, inactive customers Discounts, reminder campaigns
2 Nurture Recent but low-frequency/spending buyers Onboarding and education
3 Reward Frequent, recent, high-spending buyers VIP offers, exclusive rewards

## Outcome

Successfully segmented customers using data-driven methods, delivering actionable business insights for strategic marketing. This project showcases data cleaning, feature engineering, clustering, and result visualization—all in a real-world retail context.
