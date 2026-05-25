# Internshala Internship Data Analysis

# Overview

This project combines **Web Scraping**, **Data Cleaning**, **Feature Engineering**, and **Exploratory Data Analysis (EDA)** to analyze internship trends from the Internshala platform.

Using Python libraries like **Requests**, **BeautifulSoup**, and **Pandas**, internship listings were extracted across multiple pages and transformed into a structured dataset for analysis.

The project identifies:

* Internship market trends
* Stipend distribution
* IT vs Non-IT opportunities
* Duration analysis
* Location-wise internship patterns
* Career-oriented insights

# Business Problem

Students and job seekers often struggle to understand:

* Which internship domains pay higher stipends
* Current internship market trends
* Duration vs stipend relationships
* Demand for IT and Non-IT roles
* Location-wise internship opportunities

This project solves the problem by collecting and analyzing real-world internship data directly from Internshala.

# Objectives

* Build a complete web scraping pipeline
* Extract internship data from multiple web pages
* Clean and preprocess raw HTML data
* Perform exploratory data analysis
* Identify internship market patterns
* Generate career-oriented business insights

# Dataset Information

| Attribute     | Details          |
| ------------- | ---------------- |
| Pages Scraped | 130              |
| Total Records | 5,210            |
| Features      | 9 Columns        |
| Domain        | Career Analytics |
| Data Source   | Internshala      |

# Technologies Used

## Python Libraries

```python id="5u4bh7"
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
import requests
from bs4 import BeautifulSoup
import re
```

# Web Scraping Workflow

```text id="m0e8rz"
Send Request
      ↓
Fetch HTML Content
      ↓
Parse HTML using BeautifulSoup
      ↓
Extract Internship Details
      ↓
Store Structured Data
      ↓
Create DataFrame
      ↓
Data Cleaning & Transformation
      ↓
EDA & Visualization
      ↓
Business Insights
```

# Data Extraction

The scraper extracted:

* Internship Title
* Company Name
* Location
* Stipend
* Duration
* Skills Required
* Internship Type
* Start Date
* Application Deadline

# Data Cleaning

## Cleaning Techniques Used

* Removed duplicate rows
* Handled missing values using fillna()
* Standardized duration formats
* Cleaned stipend columns
* Removed unreliable features
* Converted text-based numerical values

# Feature Engineering

## Implemented Features

* Stipend range extraction using Regex
* IT vs Non-IT classification
* Duration conversion to weeks
* Numerical stipend standardization
* Internship categorization

# Exploratory Data Analysis (EDA)

## Univariate Analysis

* Internship distribution
* Stipend distribution
* Duration analysis

## Bivariate Analysis

* IT vs Non-IT stipend comparison
* Location-wise opportunities
* Duration vs stipend trends

## Multivariate Analysis

* Heatmap analysis
* Correlation analysis
* Grouped category analysis

# Visualizations Used

* Histograms
* Bar Charts
* Pie Charts
* Scatter Plots
* Violin Plots
* Heatmaps
* Boxplots
* Grouped Bar Charts

# Sample Code Snippets

## Sending Request

```python id="7xmrpv"
response = requests.get(url)
```

## Parsing HTML

```python id="9ng4zb"
soup = BeautifulSoup(response.text, "html.parser")
```

## Extracting Internship Data

```python id="ckzdfk"
titles = soup.find_all("h3")
```

## Data Cleaning

```python id="3c5l7g"
df.drop_duplicates(inplace=True)
```

# Key Insights

## Internship Market Insights

* 91.2% internships belonged to Non-IT domains
* IT internships offered higher average stipends
* ₹5,000–₹10,000 was the most common stipend range
* Duration showed weak correlation with stipend levels

## Career Insights

* Technical internships generally paid higher stipends
* Metro cities had more internship opportunities
* Most internships preferred short-duration commitments

# Business Impact

This project helps:

* Students identify high-paying internship domains
* Job seekers understand market trends
* Career platforms optimize recommendations
* Recruiters analyze hiring patterns

# Challenges Faced

* Pagination handling across multiple pages
* HTML structure inconsistencies
* Missing data values
* Cleaning unstructured stipend formats
* Rate limiting and request handling

# Project Workflow

```text id="wdq1wl"
Web Scraping
      ↓
Data Collection
      ↓
Data Cleaning
      ↓
Feature Engineering
      ↓
EDA
      ↓
Visualization
      ↓
Insight Generation
```

# Skills Demonstrated

* Web Scraping
* Data Cleaning
* Exploratory Data Analysis
* Feature Engineering
* Data Visualization
* Python Programming
* Problem Solving
* Analytical Thinking

# Future Improvements

* Real-time automated scraping pipeline
* Dashboard integration using Power BI/Tableau
* Internship recommendation engine
* NLP-based skill analysis
* Machine learning salary prediction

# Tools & Technologies

* Python
* BeautifulSoup
* Requests
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Regex
* Jupyter Notebook
