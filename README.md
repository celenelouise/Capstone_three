# Capstone_three
Springboard repo for Capstone Three

## Data Wrangling & Cleaning

## EDA
View the notebook here to see Plotly visualizations [https://nbviewer.org/github/celenelouise/Capstone_three/blob/main/EDA.ipynb]
# Capstone Three: [Project Title]

## Overview

This project focuses on leveraging geographical customer segmentation to enhance targeted marketing efforts. By analyzing customer data and identifying regional patterns, the goal is to optimize marketing strategies, improve customer engagement, and drive sales. The project utilizes clustering techniques to segment customers based on their geographical locations and purchasing behaviors, enabling stakeholders to tailor marketing campaigns to specific regions and demographics. In today’s competitive market, businesses must ensure their marketing efforts are directed toward the right audience. Geographical segmentation allows companies to divide their customer base into regions with similar characteristics, enabling more personalized and effective marketing strategies. The goal of this project is to perform geographical customer segmentation using clustering algorithms to identify distinct customer groups based on location and behavior. These insights will help stakeholders design targeted marketing campaigns that resonate with specific regions and demographics.


## Dataset

This dataset contains sales history from Caring Transitions of Southern Arizona Ctbids online auction platform from July 2024 through end of December 2024. The dataset contains 8153 rows and 27 columns, with features such as: Customer_ID: Unique identifier for each customer, Location: Geographical information (city, state, zip code), Purchase_Amount: Total amount spent by the customer
and Age, Gender, Income: Demographic information. The data challenges included missing values in the demographic fields, inconsistent formatting of the geographocal data, and outliers in the purchase amounts.


## Methodology

There was modifications in the dataframe which focused mainly on changing the dtypes to work with them more easily and incorporate in additional dataset that mapped zip codes to city/state/latitude and longitude: Missing Values (NANs): When the datasets were merged we did have 167 missing values, which only made up 2% of the dataset so we went ahead and dropped those. Duplicates: There were no duplicates in this df. Divided the variables into 2 categories: Numerical and categorical as below: Numerical Variables: 'Sale Price', 'Buyers Premium', 'Reserve Price', 'Number of Views', 'Tax', 'Number of Bids' Categorical Variables: 'Zip', 'Invoice Status', 'IRM', 'Status', 'Category Name'. Created new features such as an engagement score, distance metrics, and binning zip codes by frequency. Scaled numeric features using StandardScaler, and OneHotEncoder for categorical features. Used K-Means Clustering to segment customers based on geographical and behavioral features. Determined the optimal number of clusters using the Elbow Method. Evaluated the quality of clusters using KMeans. Used PCA for better visualization. 


Pearson Correlation Matix was used to visualize Numerical Features and a combination of scatterplot, boxplot and correlation matrix Chi-Square Statistic, along with scatterplots and bar plots were used to visualize the relationships between the Categorical features. Created interactive maps to display customer segments.
Generated bar charts and heat maps to highlight regional purchasing trends.
Used Principal Component Analysis (PCA) to reduce dimensionality and better visualize. 



## Results

Customer Segments
The clustering algorithm identified 3 distinct customer segments:
Cluster 0: High-demand areas with significant interest and competition. Characteristics: located in diverse geographical areas, high number of bids and views
Cluster 1: Mid-range auction participation, balanced bidding behavior (not aggressive, not passive), more price-conscious buyers.
Cluster 2: Budget-conscious segment with low competition. Characteristics: less frequent bidding, lower sale price tolerance, likely to be new or cautious buyers.


Key Insights & Recommendations
Cluster 0 makes up 39.77% of total revenue, with Cluster 1 contributing to revenue second most.
Cluster 0 (High-Engagment, High-Bids, High Sale Price) → Exclusive Auctions & VIP Access, Personalized Recommendations, Loyalty Perks, Urgency & FOMO.
Cluster 1 (Moderate demand, Mid-price) → Price-Match & Discount Alerts, Auction Bundles, Social Proof & Reviews, Segmented Email Campaigns.
Cluster 2 (Low-interest, Low-price) → First-Time Buyer Incentives, Educational Content, Referral Bonuses, Flash Sales & Clearance Events.


## Conclusion

This project successfully demonstrated the value of geographical customer segmentation for targeted marketing. By identifying distinct customer groups and their preferences, stakeholders can allocate resources more effectively and design campaigns that resonate with specific regions. Future work could include incorporating additional data sources, such as online behavior, to further refine segmentation.


