# Customer Lifetime Prediction Value

This repository contains code for predicting customer lifetime value (LTV) using a machine learning model. The goal is to identify different customer behavior patterns, segment customers, and predict their LTV. The prediction is based on recency, frequency, and monetary (RFM) clustering, as well as feature engineering and a machine learning model.

## Table of Contents

- [Introduction](#introduction)
- [Lifetime Value Prediction](#lifetime-value-prediction)
  - [Deciding the Timeframe](#deciding-the-timeframe)
  - [Identifying Features](#identifying-features)
  - [Recency](#recency)
    - [Assigning a Recency Score](#assigning-a-recency-score)
    - [Ordering Clusters](#ordering-clusters)
  - [Frequency](#frequency)
    - [Frequency Clusters](#frequency-clusters)
  - [Revenue](#revenue)
    - [Revenue Clusters](#revenue-clusters)
  - [Overall Score based on RFM Clustering](#overall-score-based-on-rfm-clustering)
- [Customer Lifetime Value](#customer-lifetime-value)
  - [Feature Engineering](#feature-engineering)
- [Machine Learning Model for Customer Lifetime Value Prediction](#machine-learning-model-for-customer-lifetime-value-prediction)
- [Final Clusters for Customer Lifetime Value](#final-clusters-for-customer-lifetime-value)

## Introduction

In business, understanding customer lifetime value (LTV) is crucial for making informed decisions on customer acquisition, retention, and marketing strategies. This code aims to predict the LTV of customers using a machine learning model. By analyzing recency, frequency, and monetary metrics, we segment customers and predict their future value.

## Lifetime Value Prediction

### Deciding the Timeframe

The LTV calculation involves selecting an appropriate time window, such as 3, 6, 12, or 24 months. This code focuses on a 6-month timeframe to predict future LTV for customers.

### Identifying Features

RFM scores (Recency, Frequency, Monetary) are used as features for prediction. These scores are calculated for each customer based on their purchase history.

### Recency

Recency refers to the time since a customer's last purchase. Customers are clustered based on their recency scores, and the clusters are ordered to represent levels of inactivity.

#### Assigning a Recency Score

The K-means algorithm is applied to assign recency clusters, categorizing customers based on their inactivity.

#### Ordering Clusters

The recency clusters are ordered to reflect the level of inactivity, with cluster 0 being the most inactive.

### Frequency

Frequency represents how often a customer makes purchases. Similar to recency, customers are clustered based on their purchase frequency.

#### Frequency Clusters

The K-means algorithm is used to create frequency clusters, categorizing customers based on their purchase frequency.

### Revenue

Revenue is calculated by multiplying the unit price with the quantity of items purchased. Similar to recency and frequency, customers are clustered based on their revenue.

#### Revenue Clusters

The K-means algorithm is applied to create revenue clusters, categorizing customers based on their revenue.

### Overall Score based on RFM Clustering

An overall score is calculated by summing the recency, frequency, and revenue clusters. This score represents the customer's overall value.

## Customer Lifetime Value

Customer Lifetime Value (LTV) is calculated using the total gross revenue generated by a customer. The LTV clusters are determined based on the calculated LTV for each customer.

## Machine Learning Model for Customer Lifetime Value Prediction

A machine learning model (XGBoost) is built to predict the LTV clusters of customers. The model is trained on features derived from recency, frequency, and monetary metrics.

## Final Clusters for Customer Lifetime Value

The trained machine learning model is used to predict LTV clusters for customers. These clusters categorize customers into different segments based on their predicted future value.

For more details and step-by-step explanations of the code, please refer to the Jupyter Notebook provided.

