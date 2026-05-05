---
layout: default
title: Home
---

## 👋 About Me

I'm **Jing You**, transitioning from hospitality management to data engineering.

**My Background:**
- 🎓 Hospitality Management degree from RIT
- 🏠 Former Airbnb host & owner of Appliances 4 Less Nashville
- 📊 5 years of experience in e-commerce digital marketing
- 💻 Currently: Data Engineering Apprentice at Nashville Software School (Graduating May 2025)

**Why the Transition?**

While running my restaurant, I found myself spending countless hours in Excel analyzing customer data and optimizing Facebook ad campaigns. I realized: **I love solving problems with data**. As an immigrant who came to the US at 16, I've always believed that education and skills are the keys to changing one's destiny. After completing a Data Analytics bootcamp, I decided to go further—to learn Data Engineering.

---

## 🚀 My Two-Month Learning Journey

### Timeline
- **October 2024**: Started Data Engineering program
- **November 2024**: Completed first ETL project
- **December 2024**: Successfully built API data pipeline

### Tech Stack
**Proficient:**
- **Languages**: Python, SQL
- **Data Processing**: Pandas, Polars
- **Databases**: PostgreSQL, DuckDB
- **Tools**: Docker, Git, VS Code
- **Cloud**: AWS (S3, Lambda)

**Currently Learning:**
- dbt (data build tool)
- Apache Airflow
- Data modeling

---

## 🛠️ Technical Skills

**Programming Languages**
- Python (Pandas, Polars, Requests)
- SQL (PostgreSQL, DuckDB)

**Data Engineering**
- ETL Pipeline Development
- API Integration & REST APIs
- Data Validation & Quality Assurance
- Batch Processing

**Tools & Technologies**
- Docker & Containerization
- Git & Version Control
- AWS (S3, Lambda)
- VS Code & Dev Containers

**Data Formats**
- JSON, Parquet, CSV
- Structured & Semi-structured Data

---

## 💼 Project Portfolio

### Project 1: NPPES Medical Provider Data Pipeline
**Tech Stack**: Python, AWS S3, PostgreSQL, Docker

Processed 8.7 million medical provider records, building a complete batch ETL pipeline.

**Key Learnings:**
- Handling large-scale datasets (8.8M records)
- Automating processes with Lambda functions
- Implementing structured logging systems

[View Project →](https://github.com/JingYou-data/NPPES)

---

### Project 2: Weather Data Integration Pipeline ⭐ *Latest*
**Tech Stack**: Python, REST API, Pandas, PostgreSQL, DuckDB, Docker

Built a multi-source data integration pipeline that combines real-time weather data from OpenWeatherMap API with PostgreSQL weather station information.

**Core Features:**
```python
# API Integration with Rate Limiting
@rate_limit(max_per_second=2)
def fetch_weather(city, lat, lon):
    response = requests.get(url, params=params)
    return response.json()

# Data Transformation
merged = weather_df.merge(stations_df, on='city', how='inner')
merged.to_parquet('weather_clean.parquet')

# Data Validation with DuckDB
con.execute("""
    SELECT COUNT(*) as null_count
    FROM weather WHERE temperature_f IS NULL
""")
