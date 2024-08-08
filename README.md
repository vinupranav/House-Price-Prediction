# Bengaluru House Prices Prediction

![Project Banner](https://user-images.githubusercontent.com/48794028/148332938-4e66d4ca-2d16-474f-8482-340aef6a48d0.png)

This project focuses on predicting house prices in Bengaluru, India, using a dataset containing details about various properties. The dataset includes features such as location, size, total square feet, number of bathrooms, and price. The goal is to clean the data, engineer features, and build a model to predict house prices.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Description](#data-description)
3. [Data Cleaning and Preprocessing](#data-cleaning-and-preprocessing)
4. [Feature Engineering](#feature-engineering)
5. [Outlier Detection and Removal](#outlier-detection-and-removal)
6. [Model Building](#model-building)
7. [Usage](#usage)
8. [Contributing](#contributing)
9. [License](#license)

## Project Overview

The project involves the following main tasks:
- Loading and exploring the dataset
- Cleaning and preprocessing the data
- Performing feature engineering
- Handling outliers and errors
- Building a predictive model for house prices

## Data Description

The dataset `bengaluru_house_prices.csv` contains the following columns:
- `area_type`: Type of the area (e.g., Super built-up Area, Built-up Area)
- `availability`: Availability status of the property
- `location`: Location of the property
- `size`: Size of the property (e.g., 2 BHK, 3 BHK)
- `society`: Name of the society
- `total_sqft`: Total square feet of the property
- `bath`: Number of bathrooms
- `balcony`: Number of balconies
- `price`: Price of the property

## Data Cleaning and Preprocessing

The dataset undergoes the following preprocessing steps:
1. **Dropping Unnecessary Columns**: Columns such as `area_type`, `society`, `balcony`, and `availability` are dropped.
2. **Handling Missing Values**: Rows with missing values are dropped.
3. **Converting `size` to `bhk`**: Extract the number of bedrooms from the `size` column.
4. **Handling Range Values in `total_sqft`**: Convert range values to the average of the range.
5. **Feature Engineering**: Calculate `price_per_sqft` as a new feature.

## Feature Engineering

- **Feature Engineering**: Created new features such as `price_per_sqft` to better capture the relationship between price and square footage.

## Outlier Detection and Removal

- **Outlier Removal**:
  - Removed properties with unrealistic `total_sqft` and `price_per_sqft`.
  - Removed properties where the number of bathrooms significantly exceeds the number of bedrooms.
  - Addressed anomalies where the price of larger properties was lower than that of smaller properties with fewer bedrooms.

## Model Building

- **Encoding Categorical Variables**: Applied one-hot encoding to the `location` column.
- **Training Data**: The cleaned and processed dataset is used to train machine learning models.

## Usage

To use this project:
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/bengaluru-house-prices.git
