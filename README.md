# **Airline Customers Value Analysis with K-mean**

This team project was conducted as the completion of an assignment from Rakamin Academy Data Science Bootcamp.

# Dataset Description

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

![image](https://github.com/mpythree/Airline-Customers-Value-Analysis-with-Kmeans/assets/86466306/dcc7c424-6ea2-4c50-a130-3137b00e0ca4)

#### **"Silhouette Score"** using **"Elbow Method"**

The optimal amount of clusters is 4 clusters. Otherwise, then the reduction of inertia value won't be significant.

![image](https://github.com/mpythree/Airline-Customers-Value-Analysis-with-Kmeans/assets/86466306/ab998728-32c5-4f0a-9774-e5b69fcac13a)

## Clustering Using PCA

![image](https://github.com/mpythree/Airline-Customers-Value-Analysis-with-Kmeans/assets/86466306/b781406f-d482-4d3a-8415-b07c54c1c238)
![image](https://github.com/mpythree/Airline-Customers-Value-Analysis-with-Kmeans/assets/86466306/99cc4a5c-b257-4694-844e-84d871024380)

## Silhouette Score Plot

![image](https://github.com/mpythree/Airline-Customers-Value-Analysis-with-Kmeans/assets/86466306/d552960d-9f41-4bad-9ddf-35f781116c4c)

# Model Interpretation and Recommendation

## Cluster Interpretation  

By using K-means, hence we found the LRFMC statistical mean and median of each feature of each cluster.

![image](https://github.com/mpythree/Airline-Customers-Value-Analysis-with-Kmeans/assets/86466306/e9b9a648-e47e-4915-9d58-357adf77ed5f)
![image](https://github.com/mpythree/Airline-Customers-Value-Analysis-with-Kmeans/assets/86466306/b40eadfe-1f42-4cc1-82f6-8ebc40fb67df)

## Cluster Description

- Cluster 0 : More than 7 years lifetime customers, rarely do flights and flight total distance is not too plenty.

- Cluster 1 : Nearly 5 years lifetime customers, actively enough in using flight services and often do a long-distance trip. (High_Value Customer)

- Cluster 2 : Around 2 years lifetime customers(relatively new), oftentimes doing flights and fair travel distance. (potential customer)

- Cluster 3 : Around 3 years lifetime customers(relatively new), but seldomly doing flights and short travel distance once using. (low_value customer)

## Business Reccomendation

1. Focus on intensifying the marketing strategies for belonging to cluster 1. To increase flights amount which is still low and hasn't had a flight for a long time, the marketing strategy can be carried out by giving discount promo or partnership with a travel agent to provide attractive vacation package promo, so that these customers will be interested to have a flight again using this airline.

2. Focus on retaining customers belonging to cluster 2 by offering premium airline memberships. 
