# New York City Taxi and Limousine Commission Fare Prediction

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.x-blue?style=for-the-badge&logo=python" alt="Python Badge">
  <img src="https://img.shields.io/badge/Pandas-Data%20Analysis-green?style=for-the-badge&logo=pandas" alt="Pandas Badge">
  <img src="https://img.shields.io/badge/Scikit%20Learn-Machine%20Learning-orange?style=for-the-badge&logo=scikitlearn" alt="Scikit Learn Badge">
  <img src="https://img.shields.io/badge/Status-Completed-success?style=for-the-badge" alt="Status Badge">
</p>

## Overview

This project builds a machine learning model to predict taxi fare amount using New York City Taxi and Limousine Commission trip data.

The work covers complete data science flow from domain understanding to data cleaning, exploratory data analysis, feature engineering, model building, hyperparameter tuning, and model saving.

The main idea is to estimate how much a taxi ride should cost from trip related details. This can support fare estimation and also help in identifying overcharge cases.

## Problem Statement

The goal of this project is to build a regression model that can predict taxi fare amount from ride information such as trip distance, ride duration, passenger count, pricing type, and ride timing.

## Business Use Case

This project is useful for more than only prediction.

A good fare prediction model can help in:

1. fare estimation before analysis
2. overcharge detection
3. anomaly identification
4. pricing pattern understanding
5. quality monitoring of taxi trip records

If predicted fare and actual fare are very different, it may indicate:

1. meter issue
2. route inefficiency
3. fare recording problem
4. exceptional pricing case

## Dataset Summary

The notebook analysis shows the following dataset details:

| Item | Value |
| --- | --- |
| Total rows | 22,699 |
| Total columns | 18 |
| Time coverage | 2017 |
| Data type | Trip level taxi records |

### Important Columns

| Column Name | Description |
| --- | --- |
| `VendorID` | Taxi provider code |
| `tpep_pickup_datetime` | Pickup date and time |
| `tpep_dropoff_datetime` | Dropoff date and time |
| `passenger_count` | Number of passengers |
| `trip_distance` | Distance travelled in miles |
| `RatecodeID` | Fare category |
| `store_and_fwd_flag` | Whether record was stored before sending |
| `payment_type` | Payment method |
| `fare_amount` | Target variable |
| `tip_amount` | Tip paid after ride |
| `total_amount` | Final charged amount |

## Project Structure

```text
New York City Taxi and Limousine Commission (TLC)/
│
├── Model/
│   ├── New York TLC.ipynb
│   ├── model.pkl
│   └── pipe.pkl
│
└── requirement.txt

