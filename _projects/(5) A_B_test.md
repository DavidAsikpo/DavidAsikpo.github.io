---
name: A/B Testing Ad Campaign Analysis
tools: [Python, Statistical Analysis]
image: https://res.cloudinary.com/dn5snxslw/image/upload/v1769858325/A_b_test_d8wip3.webp
description: This project presents an interactive dashboard for analyzing online advertising campaigns.It compares campaigns (e.g., Facebook Ads vs AdWords Ads) across key metrics such as Click-Through Rate (CTR), Conversion Rate, and Cost Per Click, identifying statistically significant differences using A/B testing methodology.The primary goal is to provide actionable insights into campaign performance and support data-driven decision-making for ad spend optimization.
---


## Project Summary
![A/B Testing Dashboard](/assets/image/AB_test.webp)

This project delivers an interactive analytics dashboard designed to evaluate and compare online advertising campaigns using **A/B testing methodology**. The analysis focuses on measuring and validating performance differences between **Facebook Ads** and **Google AdWords** across key marketing KPIs such as **Click-Through Rate (CTR)**, **Conversion Rate**, and **Cost per Click (CPC).

Rather than relying on surface-level comparisons, the project applies formal statistical testing to determine whether observed performance differences are statistically significant, enabling confident and data-driven advertising spend decisions.

---

## Objective

- Compare advertising campaign performance across platforms
- Identify statistically significant differences using hypothesis testing
- Support optimization of marketing spend with actionable insights
- Present results in an interactive, executive-friendly dashboard

---

## Data Overview

The dataset represents daily advertising performance across multiple campaigns and includes:

- Campaign date and advertising platform (Facebook Ads or Google AdWords)
- Ad impressions, clicks, and conversions
- Advertising spend
- Derived performance metrics including CTR, Conversion Rate, and CPC

Each record represents a single campaign-day observation, enabling both time-based analysis and robust statistical comparison.

---

## Project Workflow & What I Did

### 1. Data Cleaning & Preparation

- Assessed data quality by identifying missing values and duplicates
- Standardized column names and data types for consistency
- Merged multiple campaign datasets into a unified analytical structure
- Ensured each row represented a single campaign session to support accurate aggregation and testing

**Outcome:** A clean, analysis-ready dataset suitable for statistical testing and dashboard development.

---

### 2. Feature Engineering & Metric Design

Core performance metrics were derived directly from raw campaign data to ensure transparency and analytical accuracy:

- **CTR:** Clicks divided by impressions
- **Conversion Rate:** Conversions divided by clicks
- **Cost per Click (CPC):** Advertising cost divided by clicks

Metrics were calculated at the session level and later aggregated to support trend analysis and KPI reporting.

**Outcome:** Business-aligned KPIs that accurately reflect campaign performance.

---

### 3. Statistical Analysis (A/B Testing)

To validate performance differences between advertising platforms, I applied formal hypothesis testing techniques:

- **CTR and Conversion Rate**
  - Evaluated using a **two-sample proportion Z-test**
  - Appropriate due to large sample sizes and binomial outcome structure
- **Cost per Click**
  - Compared using **Welch’s t-test** to account for unequal variances between campaigns

**Hypotheses**

- **Null Hypothesis (H₀):** No performance difference between campaigns
- **Alternative Hypothesis (H₁):** A statistically significant performance difference exists

**Sample Result**

- CTR Z-statistic: **79.33**
- P-value: **≈ 0.00**
- Interpretation: **Highly statistically significant difference**

**Outcome:** Confirmed that observed performance differences were not due to random variation.

---

### 4. Results Interpretation & Business Impact

- Identified the top-performing advertising platform based on statistically significant CTR and conversion outcomes
- Calculated effect sizes to quantify the magnitude of performance differences
- Translated statistical findings into **clear, actionable marketing recommendations**

**Outcome:** Data-backed insights that directly inform ad budget allocation and campaign optimization.

👉 **View the full Python analysis notebook:** [A_B_testing.ipynb](/assets/image/A_B_testing.ipynb)

---

### 5. Dashboard Development

An interactive dashboard was designed and built using **Tableau** to communicate insights effectively to stakeholders.

**Key Features**

- Monthly CTR and Conversion Rate trends
- Year-over-year performance comparisons
- Average CTR and Conversion Rate with percentage change indicators
- Campaign-level advertising spend analysis
- KPI cards for total impressions, clicks, and conversions
- Dynamic filters by year and campaign

**Outcome:** A decision-ready dashboard that updates seamlessly as new data becomes available.

---

## Tools & Technologies

- **Tableau** for interactive dashboard design
- **Statistical Testing:** Two-sample proportion Z-test and Welch’s t-test
- **Data Preparation & Analysis:** Data cleaning and feature engineering
- **A/B Testing Methodology**
- **Data Visualization and Insight Storytelling**

---

## Key Achievements

- Applied rigorous **statistical hypothesis testing** beyond descriptive comparisons
- Bridged **marketing analytics and experimental design**
- Designed an executive-friendly dashboard focused on clarity and insight
- Delivered defensible, data-driven recommendations for ad spend optimization

---

## Why the Z-Test Was Used

CTR and Conversion Rate are proportional metrics derived from impressions, clicks, and conversions. These metrics follow a **binomial distribution**, and given the large sample sizes involved, the **two-sample proportion Z-test** is the statistically appropriate method for determining whether differences between campaigns are significant.

---

## Future Enhancements

- Segment performance by device type, region, or audience demographics
- Introduce forecasting for CTR and Conversion Rate trends
- Implement automated alerts for abnormal campaign performance
- Extend testing to multivariate and multi-arm experiments
