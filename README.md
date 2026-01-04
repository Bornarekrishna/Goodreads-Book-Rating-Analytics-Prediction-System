# Goodreads-Book-Rating-Analytics-Prediction-System

## Project Overview
This project is an **end-to-end Data Science Capstone Project** completed as part of the **Internshala Data Science Training Program**.  
The objective of this project is to analyse Goodreads book data to understand the key factors influencing book ratings and to build a machine learning model capable of predicting book ratings using structured metadata.

The project follows the complete data science lifecycle, starting from **web scraping** and ending with **machine learning prediction and interactive visualisation using Power BI**, supported by AI-driven explainability.

---

## Introduction
Goodreads is one of the largest online platforms for book discovery, reviews, and ratings. Book ratings play a critical role in influencing reader decisions, book popularity, and sales performance. However, predicting how well a book will be received based on its attributes remains challenging.

This project addresses this challenge by applying data science techniques to analyze historical Goodreads data, identify rating drivers, and build a predictive model that estimates book ratings using measurable features such as genre, author reputation, book format, page count, and reader engagement.

---

## Project Objectives
- Collect real-world book data from Goodreads using web scraping
- Clean and preprocess raw data into an analysis-ready format
- Perform exploratory data analysis to uncover trends and patterns
- Engineer meaningful features for improved prediction
- Build and evaluate machine learning models
- Select the best-performing model based on evaluation metrics
- Create an interactive Power BI dashboard for business insights
- Provide AI-driven explainability for rating predictions

---

## Project Workflow & Tasks

### **Phase 1: Data Collection (Web Scraping)**
- Scraped book data from Goodreads (*Best Books Ever* list)
- Extracted attributes including:
  - Book name
  - Author
  - Genre List
  - Pages Format
  - First published year
  - Rating
  - Ratings count
  - score
  - Votes
  - Book URL

**Tools Used:** Python, Requests, BeautifulSoup

*Insight:*  
This phase enabled the creation of a real-world dataset in the absence of a public Goodreads API.

---

### **Phase 2: Data Cleaning & Preprocessing**
- Handled missing values and inconsistent formats
- Converted text-based numerical fields into numeric values
- Separated the number of pages and book format
- Standardised genre information
- Removed data leakage feature (`score`)
- Applied feature engineering:
  - Book Age
  - Pages Category (Short, Medium, Long, Very Long)
  - Log transformation for engagement metrics
  - Target encoding for authors (high cardinality feature)

*Insight:*  
Proper cleaning and feature engineering significantly improved data quality and model performance.

---

### **Phase 3: Exploratory Data Analysis (EDA)**
- Analyzed rating distribution
- Studied genre-wise and book-format-wise rating trends
- Examined the relationship between reader engagement and ratings
- Analyzed rating trends across publication years
- Performed correlation analysis on numerical features

*Key Findings:*
- Fantasy and Comics genres consistently achieved higher ratings
- Hardcover and Kindle formats performed better
- Reader engagement positively correlates with ratings
- Medium to very long books showed higher rating stability

---

### **Phase 4: Machine Learning Model Building & Evaluation**
- Built and evaluated the following models:
  - Linear Regression
  - Random Forest Regressor
- Models were compared using:
  - MAE (Mean Absolute Error)
  - RMSE (Root Mean Squared Error)
  - R² Score

**Model Performance Summary:**

| Model | MAE | RMSE | R² Score |
|------|-----|------|---------|
| **Linear Regression** | **0.062** | **0.097** | **0.83** |
| Random Forest | 0.067 | 0.104 | 0.81 |

*Final Model Selected:* **Linear Regression**  
Reason: Best generalization, lowest error, high interpretability.

---

### **Phase 5: Interactive Dashboard (Power BI)**

- Developed an interactive Power BI dashboard featuring:
![Business Insights Dashboard](Dashboard%20Image/Business_Insights_Dashboard.png) 
  - KPI cards (Average Rating, Total Books, Engagement)
  - Genre-wise rating comparison
  - Book format analysis
  - Rating trends over publication years
  - Reader engagement vs rating scatter plot
  - Dynamic slicers for user-driven exploration
  - Detailed book-level table

*Insight:*  
The dashboard enables non-technical users to explore insights and support data-driven decisions.

- Implemented Power BI AI visuals:
![Business Insights Dashboard](Dashboard%20Image/AI_%26_Prediction_Insights.png) 
  - Key Influencers
  - Decomposition Tree
 
*Key Insight:*  
Very long books and the Fantasy genre emerged as the strongest drivers of higher ratings, validating EDA and ML findings.

---

## Final Outcome
- Successfully built an end-to-end data science solution
- Predicted Goodreads book ratings with **83% accuracy (R² Score)**
- Delivered explainable insights using AI visuals
- Created a business-ready interactive dashboard

---

## Key Learnings
- Real-world data requires extensive preprocessing
- Feature engineering is critical for model performance
- Simple models like Linear Regression can outperform complex models
- Combining ML with BI tools enhances business value
- AI explainability improves trust in data-driven decisions

---

## Recommendations
- Focus on high-performing genres such as Fantasy and Comics
- Invest in richer, long-form content for suitable genres
- Prioritize premium and digital book formats
- Use predictive analytics before book launches
- Integrate dashboard insights into regular business workflows
- Continuously retrain models with updated data

---

## Tools & Technologies Used
- Python (Pandas, NumPy, Scikit-learn)
- BeautifulSoup, Requests
- Machine Learning (Regression Models)
- Power BI
- AI Visuals for Explainability

---
