---
layout: post
title: "Building My First Data Pipeline: Weather API Integration"
date: 2024-12-16
categories: data-engineering projects
tags: python api docker etl
---

# Building My First Data Pipeline

## Project Overview

Two months into my data engineering journey, I successfully built a multi-source ETL pipeline that integrates real-time weather data with PostgreSQL database information.

**Project:** Weather Data Integration Pipeline  
**Tech Stack:** Python, Pandas, PostgreSQL, DuckDB, Docker  
**Timeline:** 1 week  
**Status:** Completed ✅

---

## The Challenge

The goal was to build a data pipeline that:
1. Fetches real-time weather data from OpenWeatherMap API
2. Extracts weather station information from PostgreSQL
3. Merges the data using Pandas
4. Validates data quality with DuckDB
5. Stores optimized results in Parquet format

---

## Technical Architecture

### Data Flow
```
OpenWeatherMap API  →  JSON  →  Pandas  →  Parquet  →  DuckDB
        +                         ↓
PostgreSQL         →  JSON  →  Merge  →  Validation
```

### Key Components

**1. API Integration (`weather_api.py`)**
```python
@rate_limit(max_per_second=2)
def fetch_weather(city, lat, lon):
    """Fetch weather with rate limiting"""
    response = requests.get(url, params=params, timeout=10)
    return response.json()
```

**2. Data Transformation (`clean_data.py`)**
```python
# Inner join on city name
merged = weather_df.merge(
    stations_df, 
    on='city', 
    how='inner'
)
merged.to_parquet('weather_clean.parquet')
```

**3. Data Validation (`validate_data.py`)**
```python
# Check for nulls with DuckDB
con.execute("""
    SELECT 
        SUM(CASE WHEN temperature_f IS NULL THEN 1 ELSE 0 END) 
    FROM weather_stations
""")
```

---

## Key Learnings

### 1. Rate Limiting is Essential
Initially, I didn't implement rate limiting and got blocked by the API. Learning: always respect API limits!

**Solution:** Created a decorator for automatic rate control
```python
@rate_limit(max_per_second=2)
```

### 2. Parquet vs CSV: The Performance Difference
- **CSV:** 100MB file, 3 seconds to read
- **Parquet:** 10MB file, 0.3 seconds to read

**10x improvement in both storage and query speed!**

### 3. Inner Join Reduced Data
Started with 10 weather stations, ended with 4 records after joining with API data.

**Why?** Inner join only keeps matching records. This was intentional - we only wanted stations with current weather data.

### 4. Docker Saved Me Hours
My classmate's code didn't run on my Windows machine. Docker solved this instantly.

---

## Challenges & Solutions

### Challenge 1: Path Issues on Windows
**Problem:** Code used hardcoded paths like `data/raw/file.json`  
**Solution:** Used `pathlib.Path` for cross-platform compatibility
```python
from pathlib import Path
filepath = Path('data') / 'raw' / 'weather.json'
```

### Challenge 2: Understanding Data Format Trade-offs
**Confusion:** Why not just use CSV for everything?  
**Learning:** 
- JSON: Human-readable, good for debugging
- Parquet: Machine-optimized, better for analysis
- Use the right tool for the right stage!

### Challenge 3: Validating Data Quality
**Problem:** How do I know my data is clean?  
**Solution:** Implemented 6-layer validation with DuckDB
- Null checks
- Duplicate detection
- Range validation
- Referential integrity
- Data type verification
- Summary statistics

---

## Results

**Deliverables:**
- ✅ Fully functional ETL pipeline
- ✅ Clean, validated dataset (4 cities)
- ✅ Containerized development environment
- ✅ Comprehensive documentation

**Data Quality:**
- 0 null values in critical columns
- 0 duplicates
- 100% data type consistency
- All validation checks passed

**Business Application:**
This pipeline can answer questions like:
- How does weather affect restaurant traffic?
- Should we adjust staffing on rainy days?
- When is outdoor seating most utilized?

---

## What I'd Do Differently

1. **Add Error Notifications:** Currently logs errors, but should send alerts
2. **Implement Caching:** Reduce API calls for frequently requested data
3. **Add Incremental Loading:** Right now it's full refresh, should only load new data
4. **Create dbt Models:** Next step is building analytics layer with dbt

---

## Code Repository

📂 **GitHub:** [github.com/jingyou-data/lab-2-ingestion](https://github.com/jingyou-data/lab-2-ingestion)

---

## Next Steps

- [ ] Add Apache Airflow for scheduling
- [ ] Build dbt analytics layer
- [ ] Create real-time dashboard
- [ ] Deploy to AWS Lambda

---

## Reflections

Two months ago, I didn't know what ETL meant. Today, I built a complete data pipeline from scratch.

**Key takeaway:** The best way to learn is by building. Not watching tutorials, not reading docs—actually writing code and breaking things.

My hospitality background helped me think about data quality the way I thought about food quality: it matters at every step.

---

**What project should I tackle next? Let me know your thoughts!**

---

*Posted on December 16, 2024 | 5 min read*

**Tags:** #DataEngineering #Python #ETL #API #Docker
