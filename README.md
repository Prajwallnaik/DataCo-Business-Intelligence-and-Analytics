# DataCo Supply Chain Analytics

## Project Overview
A comprehensive data analytics project focused on analyzing supply chain operations, sales performance, and delivery metrics for DataCo. This project combines exploratory data analysis, business intelligence dashboards, and actionable insights to optimize supply chain efficiency.

## Objectives
- Analyze sales trends and profitability across different markets and product categories
- Evaluate delivery performance and identify bottlenecks in the supply chain
- Provide data-driven insights for inventory management and customer satisfaction
- Create interactive dashboards for stakeholder decision-making

## Project Structure

```
DataCo/
├── dashboard/
│   └── dataCO.pbix                    # Power BI interactive dashboard
│
├── dataset/
│   ├── DataCoSupplyChainDataset.csv   # Raw supply chain data
│   └── powerbi_final_dataset.csv      # Processed dataset for visualization
│
├── images/
│   ├── finance.png                    # Financial metrics visualization
│   ├── income.png                     # Income analysis chart
│   ├── Presentation1.jpg              # Project presentation slide
│   ├── sales.png                      # Sales performance chart
│   └── supply-chain.png               # Supply chain flow diagram
│
├── notebooks/
│   └── DataCo.ipynb                   # Jupyter notebook with analysis
│
├── LICENSE                            # MIT License
└── README.md                          # Project documentation
```

## Key Features

### Data Analysis
- **Sales Performance**: Comprehensive analysis of revenue, profit margins, and sales trends
- **Customer Segmentation**: Insights into consumer, corporate, and home office segments
- **Product Analysis**: Category-wise performance evaluation
- **Geographic Analysis**: Market-specific trends and opportunities

### Supply Chain Metrics
- **Delivery Performance**: On-time delivery rates and delay analysis
- **Shipping Efficiency**: Comparison of actual vs. scheduled shipping times
- **Late Delivery Risk**: Predictive indicators for potential delays
- **Order Fulfillment**: Complete order lifecycle tracking

### Interactive Dashboard
- **Power BI Dashboard**: Real-time interactive visualizations
- **KPI Tracking**: Key performance indicators at a glance
- **Drill-down Capabilities**: Detailed analysis by region, product, and time period
- **Custom Filters**: Dynamic data exploration

## Dataset Overview

### DataCoSupplyChainDataset.csv
- **Records**: 5,996 transactions
- **Features**: 53 columns
- **Time Period**: 2018 data
- **Geographic Coverage**: Multiple markets (Pacific Asia, Europe, Americas, etc.)

### Key Metrics
| Metric | Value |
|--------|-------|
| Total Orders | 5,996 |
| Average Sales per Order | $184.80 |
| Average Profit per Order | $21.79 |
| Late Delivery Risk | 51.5% |
| Product Categories | 7+ categories |
| Markets Covered | 5+ regions |

## Tech Stack

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?style=for-the-badge&logo=jupyter&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=for-the-badge&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=for-the-badge&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557c?style=for-the-badge&logo=python&logoColor=white)
![Seaborn](https://img.shields.io/badge/Seaborn-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Power BI](https://img.shields.io/badge/Power_BI-F2C811?style=for-the-badge&logo=powerbi&logoColor=black)
![Git](https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)

## Technologies Used

### Core Technologies
| Technology | Version | Purpose |
|------------|---------|---------|
| Python | 3.10+ | Primary programming language |
| Jupyter Notebook | Latest | Interactive development environment |
| pandas | 2.0+ | Data manipulation and analysis |
| NumPy | 1.24+ | Numerical computing and array operations |
| Matplotlib | 3.7+ | Data visualization and plotting |
| Seaborn | 0.12+ | Statistical data visualization |

### Business Intelligence
| Technology | Purpose |
|------------|---------|
| Power BI Desktop | Interactive dashboard creation |
| DAX (Data Analysis Expressions) | Advanced calculations and aggregations |
| Power Query | Data transformation and ETL |

### Development Tools
| Tool | Purpose |
|------|---------|
| Git | Version control |
| GitHub | Code repository and collaboration |
| VS Code | Code editor (recommended) |
| Anaconda | Python distribution and package management |

## Installation

### Prerequisites
```bash
# Python 3.8 or higher
python --version

# Required packages
pip install pandas numpy matplotlib seaborn jupyter
```

### Setup
```bash
# Clone the repository
git clone https://github.com/yourusername/DataCo.git
cd DataCo

# Install dependencies
pip install -r requirements.txt

# Launch Jupyter Notebook
jupyter notebook notebooks/DataCo.ipynb
```

### Power BI Dashboard
1. Install [Power BI Desktop](https://powerbi.microsoft.com/desktop/)
2. Open `dashboard/dataCO.pbix`
3. Refresh data connections if needed
4. Explore interactive visualizations

## Analysis Workflow

### 1. Data Loading & Exploration
```python
import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns

# Load dataset
df = pd.read_csv('dataset/DataCoSupplyChainDataset.csv', encoding='latin-1')
```

### 2. Data Cleaning
- Handle missing values (Product Description, Order Zipcode)
- Convert date columns to datetime format
- Standardize numeric data types
- Remove outliers using IQR method

### 3. Feature Engineering
- **Shipping Delay**: `Days for shipping (real) - Days for shipment (scheduled)`
- **Profit Margin**: `Order Profit Per Order / Sales`
- **On-Time Delivery**: Binary indicator based on shipping delay
- **Temporal Features**: Year, Month, Quarter extraction

### 4. Visualization & Insights
- Sales distribution analysis
- Profit margin trends
- Delivery performance metrics
- Market-wise comparisons

## Key Insights

### Sales Performance
- **Distribution**: Right-skewed with most orders under $300
- **Range**: $9.26 to $1,417.50
- **Peak Sales**: Mid-range products ($100-$300)

### Profitability
- **Average Margin**: 11.5%
- **Loss-Making Items**: Identified products with negative margins
- **High-Profit Categories**: Specific product categories show superior performance

### Delivery Metrics
- **Late Delivery Risk**: 51.5% of orders at risk
- **Average Delay**: 0.47 days beyond schedule
- **On-Time Rate**: 48.5%

### Market Analysis
- **Top Markets**: Pacific Asia, Europe, LATAM
- **Growth Opportunities**: Identified underperforming regions
- **Seasonal Trends**: Q4 shows peak performance

## Dashboard Features

The Power BI dashboard (`dashboard/dataCO.pbix`) includes:

### Pages
1. **Executive Summary**: High-level KPIs and trends
2. **Sales Analysis**: Revenue breakdown by multiple dimensions
3. **Delivery Performance**: Shipping metrics and efficiency
4. **Product Insights**: Category and item-level analysis
5. **Geographic View**: Market-wise performance map

### Interactive Elements
- Date range slicers
- Product category filters
- Market selection
- Customer segment filters
- Dynamic drill-through capabilities

## Visualizations

### Sample Charts
![Sales Analysis](images/sales.png)
*Sales performance across different product categories*

![Supply Chain Flow](images/supply-chain.png)
*End-to-end supply chain process visualization*

![Financial Metrics](images/finance.png)
*Profitability and revenue trends*

![Income Analysis](images/income.png)
*Income distribution and patterns*

## Data Dictionary

### Critical Columns
| Column | Description | Type |
|--------|-------------|------|
| `Sales` | Total sales amount | Float |
| `Order Profit Per Order` | Profit per transaction | Float |
| `Delivery Status` | Shipping status category | String |
| `Late_delivery_risk` | Binary risk indicator | Integer |
| `Days for shipping (real)` | Actual shipping duration | Integer |
| `Days for shipment (scheduled)` | Planned shipping time | Integer |
| `Customer Segment` | Customer type | String |
| `Category Name` | Product category | String |
| `Market` | Geographic market | String |
| `Order Region` | Specific region | String |

## Business Recommendations

1. **Improve Delivery Performance**: Focus on reducing the 51.5% late delivery risk
2. **Optimize Inventory**: Stock high-margin products in key markets
3. **Customer Retention**: Target high-value customer segments
4. **Supply Chain Efficiency**: Reduce average shipping delays
5. **Product Mix**: Phase out loss-making items

## Future Enhancements

- Predictive modeling for delivery delays
- Customer lifetime value analysis
- Demand forecasting using time series
- Real-time dashboard with live data
- Automated reporting system
- Machine learning for inventory optimization
- Sentiment analysis from customer feedback

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.


## Author

**Prajwal L**
- Data Analyst & Business Intelligence Developer
- Focus: Supply Chain Analytics & Optimization

## Acknowledgments

- DataCo for providing the supply chain dataset
- Power BI community for dashboard inspiration
- Python data science community for excellent libraries

## Contact

For questions, suggestions, or collaboration opportunities, please open an issue in the repository.

---

**Project Status**: Active | **Last Updated**: February 2026
