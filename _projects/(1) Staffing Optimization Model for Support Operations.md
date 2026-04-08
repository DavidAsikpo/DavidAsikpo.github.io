---
name: Staffing Optimization Model for Support Operations
tools: [Python, SQL, Power BI, Data Modeling]
image: https://res.cloudinary.com/dn5snxslw/image/upload/v1775649243/dash_1_main_sztdkm.png
description: Developed a workforce planning and operations analytics model using 200K+ support tickets to optimize staffing levels and improve SLA performance in a high-volume Care Support environment. Identified that stable demand (~160–220 daily tickets) masked execution gaps, with 70%+ SLA breaches driven by delayed response (31+ hrs) and low resolution capacity. Built forecasting and simulation framework linking demand, agent productivity, and SLA constraints to determine optimal headcount and workload distribution. Modeled cost vs service trade-offs, identifying staffing thresholds that could improve SLA compliance by 25%+ while reducing backlog growth. Designed automated KPI dashboards and presented insights to operations leadership, influencing decisions on resource allocation, performance benchmarking, and workflow optimization.
---


# Staffing Optimization Model for Support Operations

> 🚀 **Reduced projected SLA breaches by 25%+ by identifying execution inefficiencies and optimizing staffing levels in a high-volume support environment**

---

## 🚨 Executive Summary

Customer support operations are often assumed to struggle due to high demand.  
This analysis challenges that assumption.

Using **200,000+ support tickets**, this project uncovers a critical insight:

> ❗ **The problem is not demand — it is execution**

Despite stable ticket volume, the system consistently underperforms due to:
- Low resolution output  
- Delayed response times  
- Poor SLA adherence  

➡️ Result: **Systematic backlog growth and service inefficiency**

---

## 🎯 Business Problem

Organizations lack visibility into how **demand, resolution capacity, and agent behavior interact**.

### Key Risks:
- Growing backlog  
- SLA violations  
- Poor customer experience  
- Inefficient resource utilization  

---

## ❓ Key Questions

- Is demand increasing or stable?  
- Are we resolving tickets at the same rate as intake?  
- What drives SLA breaches?  
- Where do delays occur in the lifecycle?  
- How does agent performance impact outcomes?  

---

## 🧱 Dataset Overview

| Attribute | Description |
|----------|------------|
| Records | 200,000+ tickets |
| Time Range | 3 years |
| Structure | Operational support dataset |
|  Key Fields | status, priority, category, timestamps, SLA |


## ⚙️ Approach

### 🔹 Workflow  
## ⚙️ Workflow

| Stage | Description | Link |
|------|------------|------|
| 📥 Raw Data | Original dataset used for analysis | [View Data](./data/) |
| 🧹 Cleaning | Data preprocessing and transformation | [View Code](./notebooks/data_cleaning.ipynb) |
| 🔧 Feature Engineering | Time features and SLA logic creation | [View Code](./notebooks/feature_engineering.ipynb) |
| 🧮 SQL Analysis | KPI calculations and aggregation queries | [View SQL](./sql/analysis.sql) |
| 🔮 Forecasting | Demand forecasting using ARIMA | [View Model](./notebooks/forecasting.ipynb) |
| 📊 Dashboard | Power BI dashboard and visuals | [View Dashboard](./dashboard/) |
| 💡 Insights | Final business insights and recommendations | [View Summary](./reports/insights.md) |

**Tech Stack:** 
![Power BI](https://img.shields.io/badge/Power%20BI-Data%20Visualization-blue?logo=power-bi&logoColor=white) 
![Power Query](https://img.shields.io/badge/Power%20Query-M-blue?logo=microsoft-powerquery&logoColor=white)
![DAX](https://img.shields.io/badge/DAX-Analysis-blue?logo=tableau&logoColor=white)
![Data Modeling](https://img.shields.io/badge/Data%20Modeling-Database-blue)
![Data Visualization](https://img.shields.io/badge/Visualization-Reports-blue)

