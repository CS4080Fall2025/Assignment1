# Comparison of Linear Regression and Random Forest Regression Models on YouTube Data

**Created by:** John Stewart  
**Date:** 09/09/2025  
**Course:** CS4680 – Assignment 1  

---

## Overview
This project analyzes YouTube video data to predict view counts and determine whether a video is considered “Trending”.

The project:
1. Cleans the data and removes unwanted inputs
3. Trains two models: **Linear Regression** and **Random Forest Regression**.
4. Compares performance using Mean Absolute Error and R².
5. Produces a final table with **actual views, predicted views, and trending status**.

---

## Target & Features
- **Target Variable:** `views`
- **Features Used:**
  - `category_id`
  - `publish_hour`
  - `publish_weekday`
  - `num_tags`
  - `likes`
  - `dislikes`
  - `comment_count`
  - `description_len`

---

## Dataset
- **Source:** [YouTube Trending Dataset on Kaggle](https://www.kaggle.com/datasets/datasnaek/youtube-new/data)  
- **File Used:** `CAvideos.csv`  
- **Size:** 45,803 entries  

---

## Models

### Linear Regression
- Assumes relationship between features and target is linear  
- Easy to interpret  
- Trains quickly  
- **Weakness:** highly sensitive to outliers  

### Random Forest Regression
- Handles **non-linear** and more complex feature interactions  
- Robust against outliers  
- **Weakness:** harder to interpret compared to linear regression  

---

## Analysis & Results
- **Linear Regression**: simple, but struggled with outliers.  
  - Example: a video with **17,340 actual views** was predicted as **169,000 views**.  
- **Random Forest Regression**: produced much closer predictions.  
  - Example: same video predicted at **50,000 views** (much more reasonable).  
- **Performance Metrics:**
  - Random Forest had a **lower MAE** (errors were smaller on average).
  - Random Forest had a **higher R²** (closer to 1, meaning better fit).  

**Conclusion:**  
Both models were suitable for the task, but **Random Forest Regression** clearly outperformed Linear Regression, making it the better choice for this dataset.

---
