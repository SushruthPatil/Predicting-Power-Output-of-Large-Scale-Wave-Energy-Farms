# Predicting Power Output of Large-Scale Wave Energy Farms

A data science project investigating whether the spatial positions of wave energy converters (WECs) can predict the total power output of a large-scale wave energy farm off the Sydney coast.

## Problem Statement

Determining the optimal placement of wave energy converters is one of the key challenges in developing large-scale wave energy farms. 
This project explores whether spatial coordinate data alone can predict total farm power output - enabling layout evaluation without physical deployment.

## Research Questions

1. Can total power output be predicted using spatial coordinates of wave energy converters?
2. How does the spatial arrangement of WECs influence overall power generation?
3. Which converter locations contribute most significantly to total power output?

## Dataset

- Source: UCI Machine Learning Repository: Large-scale Wave Energy Farm (WEC_Sydney_49.csv)
- 17,964 raw records -> 4,816 unique records after duplicate removal
- 149 columns: 98 spatial coordinates (X1–X49, Y1–Y49), 49 individual power outputs, qW efficiency metric, Total Power
- Target variable: Total Power (MW)

## Key Findings

- 73.2% of raw data were exact duplicates - removed before modelling
- Total power distribution is approximately bell-shaped, centred around 3.99 MW with low variance (±150 kW)
- Spatial heatmap revealed hot zones at farm edges and corners, cold zones in the centre - consistent with hydrodynamic interaction effects
- No single coordinate dominated predictions - full 98-feature spatial matrix required
- qW was excluded as a feature due to data leakage (derived directly from power outputs)

## Approach

Supervised regression task using 98 spatial coordinate features 
to predict Total Power. Stage 1 covers data understanding and EDA. 
Stage 2 will proceed with:

- 80/10/10 train/validation/test split
- Baseline dummy regressor
- Tree-based ensemble methods (Random Forest, Gradient Boosting)
- Hyperparameter tuning via cross-validation
- Evaluation using RMSE, R² and MAE
- Feature importance analysis

## Project Structure

- `Stage_1_Code.ipynb` - EDA and data preparation notebook
- `Stage_1_Report.pdf` - Stage 1 project report

## Tech Stack

Python, pandas, numpy, matplotlib, seaborn - Google Colaboratory

## Subject

36100 Data Science for Innovation  
Master of Data Science and Innovation  
University of Technology Sydney

## ⚠️ Academic Integrity

This project was completed as part of UTS 36100 assessment.  
Shared for portfolio purposes only. Please do not copy or submit  any part of this work as your own.

## Author

Sushruta Gangadhar Patil  
Master of Data Science and Innovation  
University of Technology Sydney
