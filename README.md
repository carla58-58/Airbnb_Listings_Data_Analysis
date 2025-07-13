# Airbnb_Listings_Data_Analysis

View the interactive notebook on Google Colab:  
[Open in Google Colab](https://colab.research.google.com/drive/1Hi8XXk1GVdXN4R78jDY3f2KZgaQLjjQz?usp=sharing)

1. Project Overview
Objective:

Explore and analyze Airbnb listings data to understand pricing, demand, and neighbourhood trends.

Answer key business questions:

What drives price variation?

Which neighbourhoods are most profitable?

Are there seasonal trends in reviews?

Dataset:

Source: listings.csv

Features include price, room type, neighbourhood, reviews, and availability.

2. Data Loading & Initial Inspection
Loaded data from listings.csv.

Inspected shape, columns, data types, and first few rows to understand the dataset structure.

3. Data Cleaning
Missing Values:

Filled missing values in reviews_per_month with 0.

Dropped rows missing critical information (price, neighbourhood, last_review).

Dropped columns with more than 50% missing data.

Duplicates:

Removed duplicate rows to ensure data integrity.

Data Types:

Converted last_review to datetime for accurate time-based analysis.

Text Cleaning:

Cleaned the name column by removing special characters, converting to lowercase, and trimming whitespace.

Standardized neighbourhood_group (if present) to lowercase.

Categorical Encoding:

Encoded room_type into numerical values for analysis.

4. Feature Engineering
Created a reviews_per_year feature by multiplying reviews_per_month by 12.

Removed price outliers above the 95th percentile to focus on typical listings.

5. Exploratory Data Analysis (EDA)
Price Distribution
Plotted histogram and boxplot to visualize the distribution of listing prices.

Used violin plot for a detailed look at price spread.

Price by Room Type
Boxplot showed how prices vary by room type, highlighting which types command higher prices.

Reviews Analysis
Boxplot of reviews per month by room type to identify which types receive more engagement.

Price vs. Demand
Scatter plots explored the relationship between price and number of reviews, as well as price and availability.

Neighbourhood Insights
Bar chart of number of listings by neighbourhood to reveal the most active areas.

Bar chart of average price by neighbourhood to identify the most lucrative locations.

Time Series Analysis
Checked the earliest and latest review dates in the dataset for time coverage.

Plotted monthly number of reviews for specific years (e.g., 2020 and 2024) to observe seasonal or annual trends.

Correlation Heatmap
Visualized correlations between key numerical features (price, minimum nights, number of reviews, reviews per month, availability) to uncover potential drivers of price or demand.

6. Export Cleaned Data
Saved the cleaned and processed dataset to Cleaned_Listings.csv for future use or sharing.
