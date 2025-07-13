# 🚕 Week 8 – NYC Taxi Data PySpark Project

This project involves working with real-world NYC Yellow Taxi trip data to perform analytical queries using **PySpark** in a **Jupyter Notebook environment**. The task focuses on reading CSV data, transforming it, and running advanced DataFrame queries for insights.

## [Notebook](./week8.ipynb)

## 📁 Dataset

- Source: [NYC Taxi & Limousine Commission](https://www.kaggle.com/datasets/gauravpathak1789/yellow-tripdata-2020-01)
- File Used: `yellow_tripdata_2020-01.csv`
- Size: ~295 MB+
- Columns include fare, tips, tax, pickup/dropoff times and locations.



## ⚙️ Tech Stack

- Python
- PySpark (Spark 3.x)
- Jupyter Notebook
- Parquet file format



## 📌 Steps Performed

1. **Load CSV** into PySpark DataFrame from local path
2. **Data Cleaning**
   - Converted timestamp fields
   - Cast numeric columns to correct types
3. **Write Cleaned Data to Parquet**
   - Saved as optimized columnar storage format



## 🔍 Key Queries

| Query | Description |
|-------|-------------|
| Q1 | Add a `Revenue` column from multiple monetary fields |
| Q2 | Count total passengers by pickup area (`PULocationID`) |
| Q3 | Average fare & total earnings grouped by vendor |
| Q4 | Moving count of payments by `payment_type` |
| Q5 | Top 2 earning vendors on a specific date with passenger and distance stats |
| Q6 | Route with the most passengers (`PULocationID` → `DOLocationID`) |
| Q7 | Top pickup zones with most passengers in last 5–10 seconds (simulated streaming) |



## 📝 Output Format

- Final DataFrame saved as:
```

yellow\_taxi\_2020\_01\_parquet/

````

- You can read it back using:
```python
df = spark.read.parquet("yellow_taxi_2020_01_parquet/")
```

