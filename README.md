# Big Data Systems: PySpark Recommender & MapReduce Analytics

## Overview

This project was developed during my Erasmus in University of Latvia, fall semester as part of a Big Data module.  
It demonstrates scalable data processing using two distributed paradigms:

- **PySpark** for building a content-based recommendation system
- **MapReduce** for large-scale aggregation over structured datasets

The objective was not only to implement the solutions, but to critically evaluate scalability, design decisions, and limitations.

---

## Task 1 – Content-Based Recommendation System (PySpark)

**Dataset:** Vehicle CO2 Emissions (Kaggle)

### Key Steps
- Data cleaning and preprocessing
- Exploratory Data Analysis (CO2 trends by engine size, fuel type, vehicle class)
- Feature engineering pipeline:
  - StringIndexer
  - OneHotEncoder
  - StandardScaler
- Feature vector assembly
- Similarity search using **Locality Sensitive Hashing (LSH)**

### Why Content-Based?

The dataset contains no user interactions or ratings.  
Therefore, collaborative filtering (e.g., ALS) was not suitable.  
Similarity was computed based on vehicle technical characteristics.

### Evaluation

- Qualitative similarity validation
- Analysis of CO2 coherence among recommended vehicles
- Discussion of limitations (no user feedback, feature sensitivity)

---

## Task 2 – Large-Scale Aggregation with MapReduce

**Dataset:** Powerlifting Database (~380k rows)

### Implemented MapReduce Tasks

1. Number of participants per competition
2. Competition summary (name, country, year, participants)
3. Total weight lifted per athlete across competitions

### Approach

- Map phase: emit key-value pairs
- Shuffle/Group phase: group by key
- Reduce phase: aggregate counts or sums

### Insights

- Demonstrates scalable aggregation logic
- Highlights strengths of batch processing
- Shows trade-offs vs Spark for iterative analytics

---

## Technologies Used

- PySpark
- Spark ML Pipeline
- Locality Sensitive Hashing (LSH)
- MapReduce paradigm
- Python
- Pandas

---

## Key Learnings

- Choosing the correct distributed model depending on the problem structure
- Trade-offs between Spark (flexibility, in-memory) and MapReduce (robust batch processing)
- Importance of feature engineering in similarity-based systems
- Scalability considerations in large datasets

---

## Project Structure
notebooks/
!- task1_pyspark_recommender.ipynb
|- task2_mapreduce_powerlifting.ipynb

report/
|- big_data_project_report.pdf

