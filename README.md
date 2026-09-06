# Building an Interactive Excel Dashboard for E-commerce Product Analysis: Jumia Products Excel Project.

## Project Overview

This project focuses on analyzing Jumia e-commerce product data using Microsoft Excel.

The project involved cleaning raw product data, performing analysis, creating PivotTables and PivotCharts, and building an interactive dashboard to present key findings and business insights.

The analysis focused mainly on product prices, discounts, customer reviews, and ratings.

---

## Project Objectives

The main objectives of this project were to:

- Clean and prepare raw Jumia product data.
- Convert text-based values into usable numerical data.
- Analyze product prices, discounts, reviews, and ratings.
- Identify relationships between discounts and customer engagement.
- Compare product prices with customer ratings.
- Identify highly rated and highly reviewed products.
- Categorize products based on price, rating, and discount.
- Build an interactive Excel dashboard.
- Generate business insights and recommendations for Jumia sellers.

---

## Dataset

The dataset contains information about products listed on Jumia.

The main fields include:

Products, Current Price, Old Price, Discount,Reviews, Rating.

---

## Workbook Structure

The Excel workbook contains the following worksheets:

### 1. Raw Data

Contains the original dataset.

The raw data was preserved without overwriting it so that the original information could always be referenced.

### 2. Cleaned Data

Contains the cleaned and prepared dataset.

Additional columns were created for analysis, including:

- Rating Category
- Price Category
- Discount Category

The cleaned data was converted into an Excel Table named `TblProducts`.

### 3. Analysis

Contains the main analysis and business findings.

The analysis includes:

- Descriptive analysis
- Trend analysis
- Product performance analysis
- Rating analysis
- Pricing analysis
- Recommendations

### 4. Pivot Tables

Contains PivotTables used to summarize the data and support the dashboard visualizations.

### 5. Dashboard

Contains the final interactive dashboard with:

- Key Performance Indicators (KPIs)
- Charts
- Product category breakdowns
- Trend analysis

### 6. Data Dictionary

Contains descriptions of the dataset fields, assumptions, data quality checks, and cleaning procedures.

---

# Data Cleaning and Preparation

Before analyzing the data, several data quality issues were identified and addressed.

## Price Cleaning

Some prices contained text such as:

`KSh 1,525`

These values needed to be converted into numerical values before calculations could be performed.

The following Excel formula was used:

=VALUE(SUBSTITUTE(SUBSTITUTE(B2,"KSh ",""),",",""))

## Handling Price Ranges
ome products contained price ranges such as:

KSh 1,620 - KSh 1,980

Instead of deleting these records, the midpoint of the price range was used for analysis.

For example:

(1620 + 1980) / 2 = 1800

## Rating Cleaning.
Ratings were converted into numerical values so that they could be analyzed and compared.

The ratings were evaluated on a scale of 0 to 5.

## Review Cleaning
The review column was checked for invalid values, including negative review counts.

Negative review values were identified before correction so that the data-quality issue could be documented.

## Rating Categories.

A new column called Rating Category was created.

Products were classified as:

Poor: Rating below 3
Average: Rating from 3 to 4.5
Excellent: Rating above 4.5

The formula used was:
=IF(F2<3,"Poor",IF(F2<=4.5,"Average","Excellent"))

## Price Ctegories.

A Price Category column was created using the current product price.

The categories used were:

Low Price: KSh 500 or below
Medium Price: KSh 501–1,500
High Price: Above KSh 1,500
The formula used was:
=IF(B2<=500,"Low Price",IF(B2<=1500,"Medium Price","High Price"))

##Discount Categories.

A Discount Category column was also created.

The categories were:

Low Discount: 0–20%
Medium Discount: 21–40%
High Discount: Above 40%

The formula used was:
=IF(D2<=20%,"Low Discount",IF(D2<=40%,"Medium Discount","High Discount"))

# Analysis Performed.
Several analyses were performed using Excel formulas, sorting, filtering, PivotTables, and charts.

## Trend Analysis

The following relationships were analyzed:

## Discount vs Reviews

This analysis examined whether products with higher discounts received more customer reviews.

## Rating vs Reviews

This analysis examined whether highly rated products received more customer reviews.

## Price vs Rating

This analysis compared product ratings across different price categories

# Business Insights.
The analysis was used to answer important business questions, including:

Do higher discounts lead to higher customer engagement?

The relationship between discount percentage and customer reviews was analyzed to determine whether higher discounts were associated with increased customer engagement.

Finding:
No Relations.

Do highly rated products have higher or lower prices?

Average ratings were compared across the Low, Medium, and High Price categories.

Finding:
No Relation.

Which products are performing best?

Products with high review counts and strong ratings were considered strong performers.

Finding:
No Relation.

Which products may need improved pricing strategies?

Products with high prices and low engagement, or high discounts and low engagement, were identified for further investigation.
Finding:
No Relations.

# Recommendations

Based on the analysis, the following recommendations can be made to Jumia sellers:

1.Use discounts strategically rather than assuming that larger discounts always lead to higher customer engagement.
2.Monitor customer ratings and investigate products that receive many reviews but have average or low ratings.
3.Review pricing strategies for expensive products that receive relatively low customer engagement.
4.Promote strong-performing products that have both high ratings and high numbers of reviews.
5.Monitor the effectiveness of discounts by comparing discounts with customer engagement and ratings.
