---
name: Paris 2024 Olympics Dashboard
tools: [Power BI, Data Modeling]
image: ![Paris 2024 Dashbaord](/assets/image/display_paris.png)
description: This project presents an interactive Power BI analysis, encomprising of Data Modeling, Dax and Data Visualization on the **Paris 2024 Olympic Games**, focusing on athlete participation, country representation, age demographics, gender distribution, and medal performance. The dashboard provides insights into **11,110 athletes across 206 countries**, enabling users to explore Olympic data by **country, gender, age group, and medal type** through intuitive and visually engaging reports, data was retrieved from kaggle.
---


## Project Workflow & Impact

![Live Dashbaord](/assets/image/DASH_1.png)
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

![Live Dashbaord](/assets/image/Dash_2.png)

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

