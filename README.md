# Car Resale Exploratory Data Analysis (EDA)

## Overview
This project demonstrates an **Exploratory Data Analysis (EDA)** on a **car resale dataset**. The goal of the analysis is to clean the data, visualize trends, and derive insights regarding car prices, car types, mileage, and other features.

## Data Description
The dataset contains information about car listings for resale. The following are the key features in the dataset:
- **Car Age**: Age of the car in years, calculated based on the year of registration.
- **Car Price**: Resale price of the car.
- **Car Type**: Type of car (e.g., sedan, SUV, hatchback).
- **Mileage**: Distance driven by the car (in kilometers).
- **Fuel Type**: Type of fuel used (e.g., petrol, diesel, electric).
- **Gearbox Type**: Transmission type (e.g., automatic, manual).
- **Date Information**: Includes columns like `dateCreated`, `dateCrawled`, and `lastSeen`, representing various timestamps of the listing process.

The dataset is stored in the `data/` folder as `autos.csv`.

## Steps in the EDA Process

### 1. **Data Loading**
- The dataset is loaded into a **Pandas DataFrame** for manipulation and analysis.

### 2. **Data Cleaning**
- **Handling Missing Values**: We use forward and backward filling for categorical features and drop rows with missing key information (e.g., `price`, `power`).
- **Removing Outliers**: Extreme outliers in the `price` feature are filtered out using the **Interquartile Range (IQR)** method.
- **Date Conversion**: Convert date columns like `dateCreated`, `dateCrawled`, and `lastSeen` into **datetime** format for better time-based analysis.
- **Handling Invalid Data**: 
  - Ensure that `postalCode` contains exactly 4 digits.
  - Validate `monthOfRegistration` is between 1 and 12.

### 3. **Data Visualization**
- **Histograms**: 
  - Distribution of car prices, power (horsepower), and mileage.
- **Pie Charts**: 
  - Distribution of car types, fuel types, and gearbox types.
- **Boxplots**: 
  - Visualize the spread and outliers in the `price` feature.
- **Scatterplots**:
  - Relationship between car price and other features like `powerPS`, `yearOfRegistration`, and `kilometer`.
- **KDE Plots**: 
  - Density estimation for continuous features like `kilometer`.
- **Time Series Analysis**: 
  - Number of car listings over time based on `dateCreated`.

### 4. **Key Insights**
- **Price vs. Car Age**: Car age correlates negatively with price; older cars generally have a lower resale value.
- **Car Type Prevalence**: Certain car types (e.g., sedan, SUV) are more common in the dataset.
- **Fuel Type Distribution**: The dataset shows a diverse range of fuel types, with some being more prevalent than others.
- **Geographical Distribution**: There are variations in car prices based on the postal code (e.g., metropolitan areas may have higher prices).

## Installation & Setup


### Clone the Repository
To get started, clone the repository to your local machine:
```bash
git clone https://github.com/yourusername/car-resale-eda.git
cd car-resale-eda
