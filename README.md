# Coupon Acceptance Analysis

Exploratory data analysis of the UCI in-vehicle coupon recommendation dataset, examining what drives drivers to accept or decline different types of coupons offered while driving.

## Overview

This project analyzes survey data collected via Amazon Mechanical Turk, where respondents were presented with various driving scenarios (destination, weather, time of day, passengers, etc.) and asked whether they would accept a coupon under those conditions. The analysis covers data cleaning, exploratory visualization, and hypothesis testing to identify the strongest predictors of coupon acceptance.

## Data Cleaning

- Removed 74 duplicate rows
- Dropped the `car` column (over 99% missing values)
- Dropped rows with missing values in frequency-of-visit columns (Bar, CoffeeHouse, CarryAway, RestaurantLessThan20, Restaurant20To50)

## Key Findings

**Bar coupons:**
- Drivers who visit bars more than once a month and are over 25 accept coupons at roughly 2x the rate of everyone else (68.98% vs. 33.73%)
- Passenger type and occupation also meaningfully affect acceptance rates

**Coffee house coupons:**
- Age, passenger type, time of day, and weather are the strongest combined predictors of acceptance (64.16% vs. 45.70% for drivers matching key conditions)
- Income shows a real but modest effect, weaker than the other factors

## Tools

Python, pandas, matplotlib, seaborn, in a Jupyter notebook

## Contents

- `prompt.ipynb` — full analysis notebook
- `data/coupons.csv` — dataset
- `images/` — supporting images referenced in the assignment
