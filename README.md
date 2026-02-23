# Global Retail BI Application

**Business Intelligence Application - Winter Term 2025/2026**

---

## Project Overview

This repository contains a comprehensive Business Intelligence application developed for a global retail company. The project focuses on providing management with deep, actionable insights into sales performance across three international markets: **USA, Germany, and Japan**.

The solution handles raw transactional data through a fully automated ETL pipeline, ensuring a scalable and data-driven reporting environment.

---

## Key Features & Requirements

The application delivers:

- **Automated ETL Pipeline**: Data cleaning and transformation performed entirely within Power Query (M) without modifying raw files.
- **Star Schema Architecture**: Optimized data model featuring a central Fact Table (`F_Sales`) and dimensions for Geography, Products, Manufacturers, and Time.
- **Revenue Gap Analysis**: Strategic framework comparing *Realized Revenue* vs. *Possible Revenue* to identify efficiency leaks.
- **Geographical Intelligence**: Detailed drill-down capabilities from country and city levels to specific ZIP codes.
- **Advanced Visualization**: Integration of specialized ArcGIS Heat Maps and AI-powered Decomposition Trees for root-cause analysis.

---

## Technical Deep Dive

### Data Modeling (Star Schema)

The model is built on a single central gateway (`MasterSource`) to ensure data consistency and high refresh performance.

- **Fact Table**: Consolidates transactional data from USA, Germany, and Japan.
- **D_Date**: Dedicated calendar table (2014-2017) supporting Time Intelligence calculations.
- **Hierarchies**: Implemented Time (Y-Q-M), Product (Category-Type), and Geography (Country-State-City-ZIP) hierarchies for intuitive navigation.

### Analytical Measures (DAX)

Key metrics developed to evaluate business trajectory and growth:

- **Realized Revenue**: Total actual income.
- **Revenue Opportunity Gap %**: Efficiency ratio flagging performance below a 10% tolerance threshold.
- **Historical Comparisons**: Year-to-Date (YTD), Year-over-Year (YoY), and cumulative progress vs. previous year baselines.

---

## Repository Structure

```text
├── docs/               # Technical Documentation (PDF)
├── src/                # Power BI Project files (.pbip format)
├── .gitignore          # Configured to exclude raw data
└── README.md           # Project summary and overview
```

