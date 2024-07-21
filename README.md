# Extreme-Whether-Event-Prediction

## Project Overview

This project aims to predict extreme weather events with a focus on wildfires. Wildfires are significant natural disasters that cause extensive damage to the environment, property, and human life. Accurate prediction of wildfires can help in planning and mitigating these risks.

## Dataset Sources

We are using publicly available wildfire datasets. Below are two reliable sources where the same dataset can be accessed:

1. [National Interagency Fire Occurrence - Sixth Edition (1992-2020) on Data.gov](https://catalog.data.gov/dataset/national-interagency-fire-occurrence-sixth-edition-1992-2020-feature-layer)
2. [Kaggle - US Wildfire Records (6th Edition)](https://www.kaggle.com/datasets/behroozsohrabi/us-wildfire-records-6th-edition)

## Setup Instructions

1. Download the dataset from one of the sources above.
2. Save the dataset as `data.csv` in the project directory.

## Libraries Needed

- `pandas` for data manipulation and analysis
- `matplotlib` for plotting and visualization
- `seaborn` for statistical data visualization

## Steps and Progress

### Exploratory Data Analysis (EDA)

We start with EDA to understand the structure and characteristics of the dataset.

#### Data Loading and Overview

- Load the dataset into a Pandas DataFrame.
- Display the first few rows.
- Print a summary of the dataset.

#### Data Cleaning and Processing

- Handle missing values.
- Remove duplicate rows.
- Ensure data consistency by converting columns to appropriate data types.
  - Convert `DISCOVERY_DATE` and `CONT_DATE` to datetime format.
  
#### Exploratory Data Analysis (EDA)
- Fire Count by Year: Analyzed the yearly trend of fire counts from 1992 to 2020.
- Fire Count by State: Identified the states with the highest number of fires.
- Fire Size Classification: Examined the distribution of fires based on size classification.