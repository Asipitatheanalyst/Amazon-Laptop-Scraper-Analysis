# Amazon Laptop Scraping Analysis

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Source](#data-source)
3. [Tools](#tools)
4. [Data Cleaning & Preparation](#data-cleaning--preparation)
5. [Objectives of the Project](#objectives-of-the-project)
6. [Data Analysis](#data-analysis)
7. [Results and Findings](#results-and-findings)
8. [Recommendations and Conclusion](#recommendations-and-conclusion)

---

## Project Overview
This project involves scraping laptop listings from **Amazon** using **BeautifulSoup** in Python, cleaned in **Excel** and **Python**, then analyzed  using **Excel**. The goal is to extract key details such as **brand**, **model**, **price**, **ratings**, and **category**. The data is cleaned and analyzed to derive insights into laptop trends, such as **total brands**, **average price**, **average rating**, and more.

---

## Data Source
The data was scraped from **Amazon's laptop category**,  which includes:
- **Title**
- **Price**
- **Rating**
- **Category**
- **Image URL**
  
---

## Tools
- **Python** (for scraping, cleaning, and analysis)
- **BeautifulSoup** (for web scraping)
- **Requests** (for making HTTP requests)
- **Pandas** (for data manipulation)
- **Regular Expressions (Regex)** (for text cleaning)
- **Excel** (for pivot table and visualization)

---

## Data Cleaning & Preparation
### **Steps Taken:**
1. **Regex Extraction:** Used a pattern to extract the **brand**, **model**, and **RAM** from the title column: This pattern was apply to title column to extract the brand, model and RAM.
   ```python
   import pandas as pd
   import re

   pattern = r"(?P<brand>\b[A-Za-z]+)\s(?P<model>[A-Za-z0-9\-]+)"
   df[['brand', 'model']] = df['title'].str.extract(pattern)
2.  **Removing Irrelevant Columns**
3.  **Data Type Conversion (Brand, Price)**

---
## Objectives of the Project
- Identify total unique laptop brands.
- Calculate average laptop price.
- Determine average rating.
- Find the most sold laptop brand.
- Identify the most expensive and cheapest brands.
- Analyze top-rated and lowest-rated brands.
- Explore relationship between price and rating.

---
## Data Analysis
The cleaned dataset was imported into Excel, where KPIs, measures, and visualizations were created to analyze trends.

Key Metrics & Insights from Excel Dashboard

KPIs (Key Performance Indicators)

The Excel dashboard highlights the following KPIs:

- Average Price: $545 – The typical cost of laptops in the dataset.
- Average Rating: 4 – The overall average customer rating across all laptops.
- Total Laptops : 31 – The number of laptops included in this analysis.
- Total Sales : $173K – The combined price of all laptops analyzed.

### Dashboard Features
- Key Metrics Displayed:
- Average Price, Number of Brands, Total Sales, Average Rating
- Expensive and Cheapest Brands
- Most Sold laptop
- Top and Low Rated brand
- Price vs. Rating Trends

![amazon dashboard](https://github.com/user-attachments/assets/99a58ec2-335c-4ddb-8e02-eb55a40f4ea8)

## Results and Findings
1.  **Total Brands & Sales Performance**:
- A total of 31 different brands are available in the dataset.
- HP is the most sold brand, with 58 units, followed by ASUS (38 units) and Lenovo (35 units).
- Some brand names appear to be general terms like "Laptop" and "Inch," which may require data cleaning.
2.  **Pricing Analysis**:
- The average laptop price is $545, indicating a mid-range pricing segment.
- The most expensive brand is MSI ($2,296), followed by ASUS ($2,099) and LG ($1,800).
- The cheapest brands include INCH and ANDROID, both at $65, with several other brands selling for under $100.
3.  **Rating Distribution & Trends**:
- The average rating across all brands is 4 stars.
- Some brands, like CENERIUS, COOLBY, and CORSAIR, have perfect 5-star ratings, while others, like YODOIT and WINDOWS, have 4-star ratings.
- This suggests a generally positive user experience but room for improvement in lower-rated brands.
4.  **Relationship Between Price & Rating**:
- Higher-priced brands do not necessarily have higher ratings.
- Some budget-friendly brands ($256-$821) maintain solid ratings, proving that price alone doesn't determine customer satisfaction.
- A notable drop in price is seen between mid-range and premium brands.

## Recommendations and Conclusion
1.  **Data Cleaning**: Remove or refine ambiguous brand names like "Laptop" and "Inch" for accurate insights.
2.  **Improve Low-Rated Brands**: Brands with 4-star ratings should analyze customer feedback to enhance product quality.
3.  **Target High-Performing Budget Brands**: Since some low-cost laptops have high ratings, promoting them effectively can drive sales.
4.  **Strategic Pricing Adjustments**: Mid-range laptops with high ratings may benefit from better visibility or promotional offers.





  
