---
name: Portfolio Performance & Risk Analytics Dashboard
tools: [Advanced Excel,Statistical Analysis]
image: https://res.cloudinary.com/dn5snxslw/image/upload/v1769802403/excel_e3xo1c.webp
description: An advanced, fully formula-driven Portfolio Performance and Risk Dashboard built in Microsoft Excel (no VBA). The project applies Power Query, dynamic formulas, pivot tables, and interactive visuals to analyze an equally weighted multi-asset portfolio from 2018 to 2025. It delivers actionable insights into performance, risk, diversification, correlation, and seasonality, demonstrating Excel’s capability as a powerful business intelligence and analytics tool.!
---

## Portfolio Performance & Risk Dashboard | Excel BI Project

### Project Overview
![Potfolio Dashboard](assets/image/excel_main.webp)

This project delivers a fully formula driven Portfolio Performance and Risk Dashboard built entirely in Microsoft Excel with no VBA required. It provides interactive analytics for an equally weighted portfolio of six securities (AAPL, GLD, MSFT, ^GSPC, TLT, EMM) covering the period from 2018 to 2025. The dashboard enables users to monitor portfolio performance, assess risk, evaluate diversification, and identify seasonality trends, supporting informed and data driven investment decisions.

### Workflow and Statistical Analysis

The workflow began with data collection and cleaning of historical daily adjusted close prices sourced from Yahoo Finance. Using native Excel functions, Power Query, and pivot tables, key metrics were calculated, including:

- **Daily and cumulative returns** for individual assets and the overall portfolio  
- **Annualized volatility** to measure portfolio risk over time  
- **Correlation matrices** to analyze inter asset relationships  
- **Quantitative diversification score** calculated as 100 × (1 minus average absolute correlation) to evaluate diversification effectiveness beyond sector exposure  

![Diversitification Dashbaord](assets/image/Diversitification.png)
The dashboard incorporates advanced performance and risk analytics through:

- **Monthly volatility trends** and risk classification to highlight high risk periods such as the 2022 market stress  
- **Correlation heat maps** using conditional formatting to visualize asset relationships  
- **Top performer identification** and contribution analysis to track assets driving portfolio growth  
- **Seasonality analysis** to uncover recurring patterns such as early year drawdowns and late year recoveries  

### Goals and Business Value

- **Performance Tracking:** Identify assets contributing most to portfolio growth, with AAPL accounting for approximately 32.7 percent of portfolio value by 2025  
- **Risk Management:** Detect periods of elevated volatility and correlation spikes to inform portfolio adjustments  
- **Diversification Optimization:** Measure true diversification strength and guide allocation decisions to reduce overall risk  
- **Strategic Recommendations:** Statistical insights support increasing defensive assets such as TLT and GLD to a combined range of 22 to 27 percent to reduce volatility by an estimated 150 to 200 basis points

![Potfolio overview](assets/image/portfolio_overview.png)

### Impact and Results

- A hypothetical initial investment of 1,000,000 grew to approximately 3.48 million by 2025, representing a 247.81 percent cumulative return and about 9.24 percent annualized growth  
- Demonstrates how advanced, formula driven Excel dashboards can deliver institutional grade insights without macros or external analytics tools  

### Technical Stack

Microsoft Excel 365 and 2021+, dynamic arrays, LET functions, Power Query, Pivot Tables, and native Excel formulas
