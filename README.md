# DataCo Supply Chain Analytics

> A comprehensive data analytics project focused on analyzing supply chain operations, sales performance, and delivery metrics for DataCo.

[![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=flat-square&logo=python&logoColor=white)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=flat-square&logo=jupyter&logoColor=white)](https://jupyter.org/)
[![Power BI](https://img.shields.io/badge/Power_BI-Dashboard-F2C811?style=flat-square&logo=powerbi&logoColor=black)](https://powerbi.microsoft.com/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square)](https://opensource.org/licenses/MIT)

---

## Table of Contents

- [Overview](#overview)
- [Key Features](#key-features)
- [Dataset Information](#dataset-information)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Installation & Setup](#installation--setup)
- [Analysis Workflow](#analysis-workflow)
- [Key Insights](#key-insights)
- [Dashboard Features](#dashboard-features)
- [Data Dictionary](#data-dictionary)
- [Business Recommendations](#business-recommendations)
- [Future Enhancements](#future-enhancements)
- [Contributing](#contributing)
- [License](#license)
- [Author](#author)

---

## Overview

This project combines exploratory data analysis (EDA), business intelligence dashboards, and actionable insights to optimize supply chain efficiency and drive data-driven decision-making.

### Project Objectives

- Analyze sales trends and profitability across different markets and product categories
- Evaluate delivery performance and identify bottlenecks in the supply chain
- Provide data-driven insights for inventory management and customer satisfaction
- Create interactive dashboards for stakeholder decision-making

---

## Key Features

### Data Analysis Capabilities

| Feature | Description |
|---------|-------------|
| **Sales Performance** | Comprehensive analysis of revenue, profit margins, and sales trends |
| **Customer Segmentation** | Insights into consumer, corporate, and home office segments |
| **Product Analysis** | Category-wise performance evaluation and profitability tracking |
| **Geographic Analysis** | Market-specific trends and regional opportunities |

### Supply Chain Metrics

| Metric | Description |
|--------|-------------|
| **Delivery Performance** | On-time delivery rates and delay analysis |
| **Shipping Efficiency** | Comparison of actual vs. scheduled shipping times |
| **Late Delivery Risk** | Predictive indicators for potential delays |
| **Order Fulfillment** | Complete order lifecycle tracking from placement to delivery |

### Interactive Dashboard

- **Power BI Dashboard**: Real-time interactive visualizations
- **KPI Tracking**: Key performance indicators at a glance
- **Drill-down Capabilities**: Detailed analysis by region, product, and time period
- **Custom Filters**: Dynamic data exploration and filtering

---

## Dataset Information

### DataCoSupplyChainDataset.csv

| Attribute | Details |
|-----------|---------|
| **Total Records** | 5,996 transactions |
| **Features** | 53 columns |
| **Time Period** | 2018 data |
| **Geographic Coverage** | Multiple markets (Pacific Asia, Europe, Americas, LATAM, etc.) |

### Key Metrics Summary

| Metric | Value |
|--------|-------|
| Total Orders | 5,996 |
| Average Sales per Order | $184.80 |
| Average Profit per Order | $21.79 |
| Late Delivery Risk | 51.5% |
| Product Categories | 7+ categories |
| Markets Covered | 5+ regions |

---

## Technology Stack

### Data Analysis & Visualization

| Technology | Version | Purpose |
|------------|---------|---------|
| **Python** | 3.10+ | Primary programming language |
| **Jupyter Notebook** | Latest | Interactive development environment |
| **pandas** | 2.0+ | Data manipulation and analysis |
| **NumPy** | 1.24+ | Numerical computing and array operations |
| **Matplotlib** | 3.7+ | Data visualization and plotting |
| **Seaborn** | 0.12+ | Statistical data visualization |

### Business Intelligence

| Technology | Purpose |
|------------|---------|
| **Power BI Desktop** | Interactive dashboard creation and reporting |
| **DAX** | Advanced calculations and aggregations |
| **Power Query** | Data transformation and ETL processes |

### Development Tools

| Tool | Purpose |
|------|---------|
| **Git** | Version control system |
| **GitHub** | Code repository and collaboration platform |
| **VS Code** | Recommended code editor |
| **Anaconda** | Python distribution and package management |

---

## Project Structure

```
DataCo/
│
├── dashboard/
│   └── dataCO.pbix                    # Power BI interactive dashboard
│
├── dataset/
│   ├── DataCoSupplyChainDataset.csv   # Raw supply chain data (5,996 records)
│   └── powerbi_final_dataset.csv      # Processed dataset for visualization
│
├── notebooks/
│   └── DataCo.ipynb                   # Jupyter notebook with complete analysis
│
├── LICENSE                             # MIT License
└── README.md                           # Project documentation
```

---

## Installation & Setup

### Prerequisites

Ensure you have the following installed:

```bash
# Python 3.8 or higher
python --version

# pip package manager
pip --version
```

### Installation Steps

**1. Clone the Repository**

```bash
git clone https://github.com/Prajwallnaik/DataCo.git
cd DataCo
```

**2. Install Python Dependencies**

```bash
# Install required packages
pip install pandas numpy matplotlib seaborn jupyter

# Or use requirements.txt (if available)
pip install -r requirements.txt
```

**3. Launch Jupyter Notebook**

```bash
# Start Jupyter Notebook server
jupyter notebook notebooks/DataCo.ipynb
```

### Power BI Dashboard Setup

1. Download & Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/) (Free)
2. Open Dashboard: Navigate to `dashboard/dataCO.pbix`
3. Refresh Data: Update data connections if needed
4. Explore: Interact with visualizations and filters

---

## Analysis Workflow

### Step 1: Data Loading & Exploration

```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv('dataset/DataCoSupplyChainDataset.csv', encoding='latin-1')

# Initial exploration
print(f"Dataset Shape: {df.shape}")
print(f"Columns: {df.columns.tolist()}")
df.info()
df.describe()
```

### Step 2: Data Cleaning

- Handle missing values (Product Description, Order Zipcode)
- Convert date columns to datetime format
- Standardize numeric data types
- Remove outliers using IQR (Interquartile Range) method
- Validate data integrity and consistency

### Step 3: Feature Engineering

| Feature | Formula | Purpose |
|---------|---------|---------|
| **Shipping Delay** | `Days for shipping (real) - Days for shipment (scheduled)` | Measure delivery efficiency |
| **Profit Margin** | `Order Profit Per Order / Sales` | Calculate profitability percentage |
| **On-Time Delivery** | Binary indicator based on shipping delay | Track delivery performance |
| **Temporal Features** | Extract Year, Month, Quarter, Day of Week | Enable time-series analysis |

### Step 4: Visualization & Insights

- Sales distribution analysis
- Profit margin trends over time
- Delivery performance metrics
- Market-wise comparisons and benchmarking

---

## Key Insights

### Sales Performance

| Metric | Finding |
|--------|---------|
| **Distribution** | Right-skewed with most orders under $300 |
| **Sales Range** | $9.26 to $1,417.50 |
| **Peak Sales** | Mid-range products ($100-$300) dominate |
| **Average Order Value** | $184.80 |

### Profitability Analysis

| Metric | Finding |
|--------|---------|
| **Average Margin** | 11.5% |
| **Loss-Making Items** | Identified products with negative margins requiring attention |
| **High-Profit Categories** | Specific product categories show superior performance (15%+ margins) |
| **Profit Optimization** | Opportunity to increase margins by 3-5% through strategic pricing |

### Delivery Metrics

| Metric | Value | Status |
|--------|-------|--------|
| **Late Delivery Risk** | 51.5% | Needs Improvement |
| **Average Delay** | 0.47 days | Above Target |
| **On-Time Rate** | 48.5% | Below Industry Standard |
| **Target On-Time Rate** | 95% | Goal |

### Market Analysis

| Market | Performance | Opportunity |
|--------|-------------|-------------|
| **Pacific Asia** | Top Performer | Maintain market share |
| **Europe** | Strong Growth | Expand product lines |
| **LATAM** | Moderate | Increase marketing efforts |
| **Africa** | Underperforming | Strategic review needed |
| **Seasonal Trends** | Q4 Peak | Optimize inventory for holidays |

---

## Dashboard Features

The Power BI dashboard (`dashboard/dataCO.pbix`) provides comprehensive analytics through multiple interactive pages.

### Dashboard Pages

| Page | Description |
|------|-------------|
| **Executive Summary** | High-level KPIs, trends, and performance overview |
| **Sales Analysis** | Revenue breakdown by category, region, and customer segment |
| **Delivery Performance** | Shipping metrics, delays, and efficiency tracking |
| **Product Insights** | Category and item-level profitability analysis |
| **Geographic View** | Interactive map showing market-wise performance |

### Interactive Elements

- **Date Range Slicers**: Filter data by custom time periods
- **Product Category Filters**: Analyze specific product lines
- **Market Selection**: Compare regional performance
- **Customer Segment Filters**: Consumer, Corporate, Home Office
- **Dynamic Drill-through**: Deep-dive into specific metrics

---

## Data Dictionary

### Critical Columns

| Column Name | Description | Data Type | Example |
|-------------|-------------|-----------|---------|
| `Sales` | Total sales amount for the order | Float | 184.80 |
| `Order Profit Per Order` | Profit generated per transaction | Float | 21.79 |
| `Delivery Status` | Current shipping status | String | "Shipped", "Delivered" |
| `Late_delivery_risk` | Binary indicator (0=On-time, 1=Risk) | Integer | 0, 1 |
| `Days for shipping (real)` | Actual shipping duration in days | Integer | 5 |
| `Days for shipment (scheduled)` | Planned shipping time in days | Integer | 4 |
| `Customer Segment` | Type of customer | String | "Consumer", "Corporate" |
| `Category Name` | Product category | String | "Technology", "Furniture" |
| `Market` | Geographic market region | String | "Pacific Asia", "Europe" |
| `Order Region` | Specific regional location | String | "Central Asia", "Western Europe" |

---

## Business Recommendations

Based on comprehensive data analysis, here are actionable recommendations:

### Priority Actions

| Priority | Recommendation | Impact | Effort |
|----------|----------------|--------|--------|
| **1** | **Improve Delivery Performance** | High | Medium |
|       | Focus on reducing the 51.5% late delivery risk through route optimization and carrier partnerships | | |
| **2** | **Optimize Inventory** | High | Low |
|       | Stock high-margin products in key markets to maximize profitability | | |
| **3** | **Customer Retention** | Medium | Medium |
|       | Target high-value customer segments with personalized offers | | |
| **4** | **Supply Chain Efficiency** | High | High |
|       | Reduce average shipping delays by 50% through process improvements | | |
| **5** | **Product Mix Optimization** | Medium | Low |
|       | Phase out loss-making items and focus on high-margin products | | |

---

## Future Enhancements

### Planned Features

- **Predictive Modeling**: Machine learning models for delivery delay prediction
- **Customer Lifetime Value**: CLV analysis for retention strategies
- **Demand Forecasting**: Time series forecasting using ARIMA/Prophet
- **Real-time Dashboard**: Live data integration with streaming analytics
- **Automated Reporting**: Scheduled email reports for stakeholders
- **ML Inventory Optimization**: AI-driven inventory management
- **Sentiment Analysis**: Customer feedback analysis using NLP
- **Web Application**: Interactive web-based analytics platform

---

## Contributing

Contributions are welcome and appreciated. Here's how you can contribute:

### How to Contribute

1. Fork the repository
2. Create a feature branch
   ```bash
   git checkout -b feature/AmazingFeature
   ```
3. Commit your changes
   ```bash
   git commit -m 'Add some AmazingFeature'
   ```
4. Push to the branch
   ```bash
   git push origin feature/AmazingFeature
   ```
5. Open a Pull Request

### Contribution Guidelines

- Follow PEP 8 style guide for Python code
- Add comments and documentation for new features
- Update README.md if necessary
- Test your changes thoroughly before submitting

---

## License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---

## Author

**Prajwal L**  
Data Analyst & Business Intelligence Developer  
Specialization: Supply Chain Analytics & Optimization

[![GitHub](https://img.shields.io/badge/GitHub-Prajwallnaik-181717?style=flat-square&logo=github)](https://github.com/Prajwallnaik)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0077B5?style=flat-square&logo=linkedin)](https://linkedin.com/in/yourprofile)

---

## Contact

For questions, suggestions, or collaboration opportunities:

- **Issues**: Open an issue in the repository
- **Discussions**: Use GitHub Discussions for general questions
- **Bug Reports**: Submit detailed issue reports
- **Feature Requests**: Share your ideas through issues

---

## Acknowledgments

- **DataCo** for providing the comprehensive supply chain dataset
- **Power BI Community** for dashboard design inspiration and best practices
- **Python Data Science Community** for excellent libraries and documentation
- **Open Source Contributors** for making data analytics accessible to everyone

---

**Project Status**: Active | **Last Updated**: February 2026
