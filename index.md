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

[View Project →](https://github.com/your-username/nppes-project)

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
```

**Project Highlights:**
- ✅ Implemented RESTful API integration with authentication, rate limiting, and error handling
- ✅ Used Pandas for data cleaning and merging (Inner Join)
- ✅ Implemented 6-layer data validation with DuckDB
- ✅ Adopted columnar storage (Parquet), achieving 10x query speed improvement
- ✅ Fully containerized (Docker + Dev Container)

**Business Application:**
This pipeline can analyze weather impacts on restaurant business, such as:
- How much does customer traffic decrease on rainy days?
- What weather conditions maximize outdoor seating utilization?
- How to adjust staffing based on weather forecasts?

---

## 🎯 From Restaurants to Code: My Unique Perspective

As someone transitioning from hospitality, I've found many parallels between the two fields:

| Restaurant Management | Data Engineering |
|----------------------|------------------|
| Ingredient procurement | Data ingestion (API + Database) |
| Food preparation | Data cleaning (Pandas) |
| Recipe standardization | Data transformation (Schema design) |
| Quality control | Data validation (DuckDB) |
| Plating & serving | Data delivery (Parquet + Reports) |

This background makes me particularly attentive to:
- **Data quality** (like checking ingredient freshness)
- **Process optimization** (like improving kitchen efficiency)
- **User needs** (like understanding customer preferences)

---

## 💡 Key Takeaways from Two Months

### Technical Side

**1. Understanding the Essence of ETL**
```
Extract (Extraction)  → Acquire data from various sources
Transform (Transformation) → Clean, merge, standardize
Load (Loading)     → Store in target location
```

**2. Mastering Data Format Conversion**
```
JSON (raw data)  →  Pandas (processing)  →  Parquet (storage)
```
Why? Because different stages have different needs:
- JSON is human-readable for debugging
- Pandas is powerful for data manipulation
- Parquet is optimized for large-scale queries

**3. Learning Systems Thinking**
Not just "making code work," but:
- Error handling (What if the API fails?)
- Logging (Can trace issues)
- Containerization (Others can run it)
- Documentation (I can understand it 3 months later)

### Mindset Shifts

**From "Completing Tasks" to "Building Systems"**
- Before: Write a Python script to export data
- Now: Design a repeatable, maintainable, scalable data pipeline

**From "I Can Use Tools" to "I Understand Principles"**
- Before: Know that Pandas can merge data
- Now: Understand Inner Join vs Left Join, and when to use which

---

## 🚧 Challenges I've Faced

### 1. **Path vs pathlib - The File Path Confusion**
**Problem**: Windows uses `\`, Mac uses `/`, code breaks across platforms

**Solution**: Learning to use `pathlib.Path`
```python
# Old way (error-prone)
filepath = 'data\\raw\\weather.json'

# New way (cross-platform)
from pathlib import Path
filepath = Path('data') / 'raw' / 'weather.json'
```

### 2. **Parquet Format - Why Not Use CSV?**
**Confusion**: CSV is so simple, why learn a new format?

**Understanding**: 
- CSV: 100MB, 3 seconds to read, human-readable
- Parquet: 10MB, 0.3 seconds to read, machine-optimized

In big data scenarios, Parquet saves 90% space and queries 10x faster!

### 3. **Docker Dev Container - Why Containerize?**
**Question**: My local environment works, why Docker?

**Understanding**: 
- My environment: Python 3.12 + Windows 11
- Classmate's environment: Python 3.9 + Mac M1
- Result: Code doesn't run on their computer!

**Dev Container Solution**: Everyone uses the same environment!

---

## 🎓 Advantages of a Non-Traditional Background

Many ask me: "Can you learn data engineering without a CS degree?"

**My answer: Absolutely! And you have unique advantages.**

**My hospitality background gave me:**

✅ **Real Business Understanding**
- I know what restaurant owners actually need from data
- I understand why "average check size" matters more than "total revenue"

✅ **Problem-Solving Ability**
- Restaurants face daily crises, developing quick adaptability
- Debugging code is like handling kitchen emergencies

✅ **Customer-Oriented Thinking**
- Writing code isn't about writing code—it's about solving problems
- The "customers" of data pipelines are data analysts and business teams

---

## 📈 Learning Methods I Use

### 1. **Learn Through Projects, Not Just Tutorials**
- ❌ Watch 100 Pandas tutorials
- ✅ Do 1 real project, look up docs when stuck

### 2. **Analogy Learning**
Use familiar concepts to understand new ones:
- ETL = Restaurant supply chain
- API = Food delivery platform ordering
- Database = Warehouse
- Cache = Prep station

### 3. **Document Everything**
- Errors encountered and solutions
- New concepts learned
- "Aha moments" (sudden understanding)

### 4. **Don't Fear "Dumb Questions"**
"What's the difference between Path and pathlib?" isn't dumb—it's a great question!

---


## 📬 Contact Me

**Currently seeking Data Analyst / BI Analyst positions (Nashville, graduating May 2025)**

- 📧 Email: [your-email@example.com]
- 💼 LinkedIn: [linkedin.com/in/your-profile]
- 🐙 GitHub: [github.com/your-username](https://github.com/your-username)
- 📍 Location: Franklin, Tennessee

---

## 💭 Final Thoughts

Two months ago, I knew nothing about "ETL." Today, I can confidently say: **I am a data engineer** (still learning, of course).

If you're also from a non-traditional background, if you're considering a career change to tech, I want to tell you:
- **Age is not a barrier** (I have a child and I'm still learning)
- **Background is not a barrier** (I studied hospitality management)
- **Starting point is not a barrier** (I came to the US at 16, worked while getting my GED)

**The only question is: Are you willing to start?**

I started two months ago, and today I have my own tech blog.  
Where will you be two months from now?

Let's connect! I'm happy to share my learning experience and look forward to hearing your story.

---

*Last updated: December 16, 2024*

---

