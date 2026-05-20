# Equipment Recommendation Prototype

## Overview

This project demonstrates a basic machine learning workflow for golf equipment R&D. The notebook uses launch monitor-style and biomechanics-style variables to predict clubhead speed and generate a simple equipment recommendation.

## Purpose

The goal is to show how player testing data can be cleaned, engineered, modeled, and converted into practical recommendations for equipment evaluation.

## Dataset

The project uses a simulated golf testing dataset with variables including pelvis angular velocity, thorax angular velocity, X-Factor peak timing, ground reaction force, launch angle, spin, ball speed, carry, clubhead speed, loft, and shaft flex.

## Methods

A Python/Colab workflow was built to generate sample data, clean variables, engineer features, train a Random Forest regression model, evaluate prediction accuracy, visualize feature importance, and export prediction summaries.

## Technical Stack

- Python
- Google Colab
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Random Forest regression
- Feature engineering
- Model evaluation

## Outputs

- sample_data.csv
- predictions_summary.csv
- equipment_recommendation_model.joblib
- actual vs. predicted clubhead speed plot
- feature importance plot
- simple equipment recommendation rule

## Applied Value

This project shows how golf testing data can be turned into a repeatable machine learning pipeline. While the dataset is simulated, the structure mirrors how player testing data could be used to support prototype evaluation, club fitting, and product-performance decisions.

## Portfolio Relevance

This project demonstrates my ability to connect biomechanics, golf performance, and data science in a clean R&D-style workflow.
