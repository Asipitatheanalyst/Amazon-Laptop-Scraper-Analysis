# Amazon Laptop Scraping Analysis

## Table of Contents
1. [Project Overview](#project-overview)
2. [Data Source](#data-source)
3. [Tools](#tools)
4. [Data Cleaning & Preparation](#data-cleaning--preparation)
5. [Objectives of the Project](#objectives-of-the-project)
6. [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
7. [Data Analysis](#data-analysis)
8. [Results and Findings](#results-and-findings)
9. [Recommendations and Conclusion](#recommendations-and-conclusion)

---

## Project Overview
This project involves scraping laptop listings from **Amazon** using **BeautifulSoup** in Python. The goal is to extract key details such as **brand**, **model**, **price**, **ratings**, and **category**. The data is cleaned and analyzed to derive insights into laptop trends, such as **total brands**, **average price**, **average rating**, and more.

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
  
