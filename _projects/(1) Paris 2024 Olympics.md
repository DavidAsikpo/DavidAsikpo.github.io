---
name: Paris 2024 Olympics Dashboard
tools: [Power BI, Data Modeling]
image: https://postimg.cc/PCckbb4c
description: nteractive Power BI dashboard for the Paris 2024 Olympic Games, leveraging Data Modeling, DAX, and Data Visualization to analyze athlete participation, demographics, country representation, gender distribution, and medal performance. Explores insights for 11,110 athletes across 206 countries, enabling dynamic filtering by country, age group, gender, and medal type using optimized measures and a scalable star-schema model. Data sourced from Kaggle.
---


## Project Workflow & Impact

![Live Dashbaord](/assets/image/DASH_1.jpg)
### 1. Data Sourcing & Preparation

- Collected raw Paris 2024 Olympic datasets from **Kaggle**.
- Cleaned and standardized athlete, medal, and country data using **Power Query (M)**.
- Created derived fields such as **age groups**, gender flags, and medal categories to support analysis.

### 2. Data Modeling (Key Differentiator)

- Designed a **star schema data model** optimized for performance and scalability.
- Built clear relationships between **Athletes, Medalists, Countries, and supporting dimension tables**.
- Centralized all KPIs in a dedicated **Measures table**, improving model clarity and reusability.
- Reduced redundancy and ensured accurate cross-filtering across dashboards.

![Data Model](/assets/image/Data_model.png)

### 3. DAX & Analytics

- Developed custom **DAX measures** for:
  - Total athletes, teams, and countries
  - Gender-based participation and medal counts
  - Medal distribution by country and medal type
  - Age-group analysis across athletes and medalists
- Applied consistent calculation logic to ensure metric reliability across reports.
## Project DAX Scripts

You can view all the DAX formulas used in this project [here](https://github.com/DavidAsikpo/DavidAsikpo.github.io/blob/master/assets/image/Dax).


### 4. Dashboard Design & Interactivity

- Built **two complementary dashboards** (Olympics Overview & Athletes Overview) for both executive and analytical use.
- Implemented interactive filters for **country, gender, age group, and medal type**.
- Used maps, bar charts, and KPI cards to support **clear data storytelling**.
- Maintained a clean, modern design for strong visual hierarchy and usability.

![Live Dashbaord](/assets/image/Dash_2jpeg.jpeg)

### 5. Key Outcomes & Value Delivered

- Enabled quick comparison of **male vs female participation and medal performance**.
- Revealed **country-level strengths** across medal types.
- Highlighted athlete **age distribution trends** and medalist demographics.
- Delivered a scalable Power BI model that can be extended to future Olympic editions.

---

### What Makes This Project Stand Out

- Strong focus on **dimensional data modeling**, not just visuals
- Clean separation of **facts, dimensions, and measures**
- Performance-optimized Power BI model
- Business-ready insights presented through intuitive dashboards

**Tech Stack:** 
![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-blue?logo=power-bi&logoColor=white) 
![Power Query](https://img.shields.io/badge/Power%20Query-M-blue?logo=microsoft-powerquery&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Analysis-blue?logo=tableau&logoColor=white)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Database-blue)
![Data Visualization](https://img.shields.io/badge/Visualization-Reports-blue)

