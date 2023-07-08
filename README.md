# **Airline Customers Value Analysis with K-mean**

This team project was conducted as the completion of an assignment from Rakamin Academy Data Science Bootcamp.

# Deskripsi Dataset

This dataset contains costumers data of an Airline Company and some features that can describe the value of the customer. Each row represents a customer, each column contains customers attribute. The dataset can be downloaded [here](https://drive.google.com/file/d/14G4xOWK5e-QQ9S7GmBwULChNdeJZXs2U/view?usp=drive_link)

- `MEMBER_NO-b` : ID Member
- `FFP_DATE` : Frequent Flyer Program Join Date
- `FIRST_FLIGHT_DATE` : First Flight Date
- `GENDER` : Gender
- `FFP_TIER` : Frequent Flyer Program Tier
- `WORK_CITY` : Hometown
- `WORK_PROVINCE` : Home Province
- `WORK_COUNTRY` : Native Country
- `AGE` : Age of Customer
- `LOAD_TIME` : Data Retrieved Date
- `FLIGHT_COUNT` : Customer Flight Count
- `BP_SUM` : Travel Plan
- `SUM_YR_1` : Fare Revenue
- `SUM_YR_2` : Votes Prices
- `SEG_KM_SUM` : Flight Distance(km) in total that have been carried out
- `LAST_FLIGHT_DATE` : Most Recent Flight Date
- `LAST_TO_END` : The distance between the last flight and the last booked flight
- `AVG_INTERVAL` : Average time gap
- `MAX_INTERVAL` : Maximum time gap
- `EXCHANGE_COUNT` : Amount of Exchange
- `avg_discount` : The average discount that the customer gets
- `Points_Sum` : The number of points earned by the customer
- `Point_NotFlight` : points that are not used by members

# Content

By using the dataset above, our objective is to find the most appropriate marketing strategy according to different types of customer clusters behavior.

# Formulation of the Problem

1. How is the characteristic of each clustered customer?
2. What is the best business strategy for each clustered customer?

# Processes

- **Exploratory Data Analysis (EDA)** includes descriptive analysis, univariate analysis, multivariate analysis, and data preprocessing.
- **Feature Engineering** 
- **Modelling & Evaluation** includes clustering and visualization using PCA and Scatterplot by Loyalty, Recency, Frequency, Monetary, Cabin (LRFMC) model.
- **Model Interpretation & Recommendation** includes interpretation and Business Strategy

# Modelling / Evaluation

#### **Elbow Method**

![image.png](attachment:1f755509-ddbd-4fc8-a597-ffef0cd040e7.png)

#### **"Silhouette Score"** using **"Elbow Method"**

The optimal amount of clusters is 4 clusters. Otherwise, then the reduction of inertia value won't be significant.

![image.png](attachment:40924391-20c9-4f1f-87f0-e167bb1f9643.png)

## Clustering Using PCA

![image.png](attachment:205f220e-1c66-40cc-944f-6edbf302e754.png)
![image.png](attachment:2140a39e-98d4-4dbf-bbcd-ccd3fd2eda79.png)

## Silhouette Score Plot

![image.png](attachment:7448cbef-1f12-4108-90d6-012dfb352854.png)

# Model Interpretation and Recommendation

## Cluster Interpretation  

By using K-means, hence we found the LRFMC statistical mean and median of each feature of each cluster.

![image.png](attachment:ddace344-93b1-4ab7-87e0-0c8693fbf009.png)
![image.png](attachment:b120a3de-c137-44a3-9d2e-10e2241bb6e0.png)

## Cluster Description

- Cluster 0 : More than 7 years lifetime customers, rarely do flights and flight total distance is not too plenty.

- Cluster 1 : Nearly 5 years lifetime customers, actively enough in using flight services and often do a long-distance trip. (High_Value Customer)

- Cluster 2 : Around 2 years lifetime customers(relatively new), oftentimes doing flights and fair travel distance. (potential customer)

- Cluster 3 : Around 3 years lifetime customers(relatively new), but seldomly doing flights and short travel distance once using. (low_value customer)

## Business Reccomendation

1. Focus on intensifying the marketing strategies for belonging to cluster 1. To increase flights amount which is still low and hasn't had a flight for a long time, the marketing strategy can be carried out by giving discount promo or partnership with a travel agent to provide attractive vacation package promo, so that these customers will be interested to have a flight again using this airline.

2. Focus on retaining customers belonging to cluster 2 by offering premium airline memberships. 
