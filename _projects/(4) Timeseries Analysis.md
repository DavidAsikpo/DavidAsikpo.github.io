---
name: Time Series Forecasting of Childhood Upper Respiratory Tract Infections (URTI)
tools: [Python, Predictive Analysis]
image: https://res.cloudinary.com/dn5snxslw/image/upload/v1769857882/Timeseries_xh4eue.webp
description: This project performs a **time series analysis of monthly reported cases of Childhood Upper Respiratory Tract Infections (URTI) of children under the age of 14 at General Hospital, Ikot Ekpene from January 2010 to June 2025.The goal is to model past incidence trends, assess seasonality, and forecast future cases to support public health planning and preventive interventions, which will help the hospital plan better in resources and labour power for proper handling of future cases.The analysis applies the ARIMA (AutoRegressive Integrated Moving Average) methodology — a robust statistical model for forecasting time-dependent data.
---

### Project Overview

This project applies **time series analysis and forecasting** to model monthly reported cases of **Childhood Upper Respiratory Tract Infections (URTI)** among children aged 0 to 14 years at **General Hospital, Ikot Ekpene**.

Using over **15 years of epidemiological data**, I built, evaluated, and validated an **ARIMA forecasting model** to uncover historical trends, seasonal patterns, and generate reliable short-term forecasts. The outcomes support **public health planning**, enabling improved allocation of **healthcare resources, staffing, and preventive interventions**.

---

## Problem Statement

Hospital administrators often rely solely on historical case counts, which limits their ability to:

- Anticipate periods of increased infection rates
- Plan staffing levels and medical supplies in advance
- Implement proactive public health interventions

This project addresses these challenges by introducing a **data-driven forecasting framework** for childhood URTI incidence.

---

## Objectives

- Analyze long-term trends and seasonal patterns in childhood URTI cases
- Test and achieve stationarity of the time series
- Identify and fit an optimal ARIMA model
- Forecast future URTI cases to support operational planning
- Translate statistical findings into actionable public health insights

---

## Data Description

- **Granularity:** Monthly case counts  
- **Population:** Children aged 0 to 14 years  
- **Study Period:** January 2010 to June 2025  
- **Observations:** 186 months  

**Key Variables**
- Month
- Year
- Number of reported URTI cases

---

## Exploratory Data Analysis (EDA)

### Analysis Performed

- Long-term trend analysis
- Seasonal variation across months
- Distribution, volatility, and spread of infection counts

### Key Findings

- **Seasonality:** Higher URTI incidence during dry season months (January to March)
- **Decline:** Reduced cases during wet season months (April to August), likely due to increased humidity and improved air quality
- **Recovery:** Gradual rise in cases from September through December

### Descriptive Statistics (Highlights)

- Mean monthly cases: **88.48**
- Standard deviation: **58.83**
- Maximum monthly cases: **250**
- Positive skewness (**1.12**), indicating occasional outbreak spikes

---

## Stationarity Testing

To prepare the data for ARIMA modeling, I applied the **Augmented Dickey-Fuller (ADF) test**.

- **Null Hypothesis (H₀):** The series is non-stationary
- **ADF Statistic:** -4.12
- **p-value:** 0.01

✅ After differencing, the series was confirmed to be **stationary**, satisfying ARIMA assumptions.

---

## Model Identification and Selection

Multiple ARIMA models were evaluated using **Akaike Information Criterion (AIC)** and **Bayesian Information Criterion (BIC)**.

| Model | AIC | BIC |
|------|-----|-----|
| ARIMA(1,1,1) | 1875.21 | 1886.42 |
| ARIMA(2,1,0) | 1873.56 | 1884.31 |
| **ARIMA(3,1,0)** | **1870.30** | **1883.05** |

### Final Model Choice

**ARIMA(3,1,0)** was selected due to:
- Lowest AIC and BIC values
- Stable parameter estimates
- Well-behaved residuals
- Strong short-term forecasting performance

---

## Model Diagnostics

Model adequacy was validated through residual diagnostics:

- Residual ACF and PACF within confidence bounds
- Ljung-Box test p-value greater than 0.05
- No evidence of serial correlation

✅ Residuals behaved like **white noise**, confirming a good model fit.

---

## Forecasting and Validation

### Short-Term Validation (January to June 2025)

Forecasted values closely matched actual reported cases, demonstrating **strong predictive accuracy**.

### Extended Forecast (12 Months)

Based on validation results, a **12-month forecast** was generated to support hospital planning.

**Key Insight**
- Forecasts indicate a **gradual increase in URTI cases throughout 2025**
- Highlights the need for proactive staffing and medical supply planning

---

## Tools and Technologies

- **Programming Language:** Python 3.10
- **Data Analysis:** pandas, numpy
- **Time Series Modeling:** statsmodels
- **Visualization:** matplotlib
- **Model Evaluation:** ADF Test, AIC/BIC, Residual Diagnostics

---

## Key Achievements

- Built a **production-ready ARIMA forecasting model**
- Applied rigorous statistical testing and validation techniques
- Identified seasonal and long-term infection patterns
- Delivered actionable forecasts for healthcare decision-making
- Demonstrated applied **time series analysis in a real-world public health setting**

---

## Business and Public Health Value

- Enables **early preparedness** for infection surges
- Supports efficient allocation of **staff, medication, and hospital resources**
- Provides a reusable forecasting framework for future epidemiological studies
- Bridges statistical modeling with **practical operational impact**

Explore the full analysis, ARIMA modeling workflow, and forecasting results on GitHub  
[View Project on GitHub](https://github.com/DavidAsikpo/Upper-Respiratory-Tract-Infections-Forecasting)

