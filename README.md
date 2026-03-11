# Customer Shopping Behavior Analysis

## 📊 Project Overview

This project analyzes consumer shopping behavior for a leading retail company to uncover trends, optimize marketing strategies, and improve customer engagement. Through data preparation, MySQL analysis, and interactive visualizations, we identify key drivers of consumer decisions and repeat purchases.

### Business Question
**"How can the company leverage consumer shopping data to identify trends, improve customer engagement, and optimize marketing and product strategies?"**

---

## 🎯 Project Objectives

- Understand purchasing patterns across demographics, product categories, and sales channels
- Identify factors driving consumer decisions (discounts, reviews, seasons, payment preferences)
- Uncover patterns in repeat purchases and customer loyalty
- Provide actionable insights for marketing and product optimization
- Enable data-driven decision making through interactive dashboards

---

## 📁 Repository Structure

```
CUSTOMER BEHAVIOUR/
│
├── Business_Problem_Document.pdf               # Original business problem statement
├── customer_shopping_behavior.csv              # Raw dataset
├── customer_behavior_cleaned.csv               # Cleaned dataset for analysis
├── customer_behavior.ipynb                     # Python analysis and data cleaning
├── customer_behavior_dashboard.pbix            # Power BI interactive dashboard
│
└── README.md                                    # Project documentation
```

---

## 🛠️ Technologies Used

- **Python 3.x**: Data cleaning, transformation, and exploratory analysis
  - pandas (data manipulation & CSV to SQL conversion)
  - numpy
  - matplotlib
  - seaborn
  - sqlalchemy (database connectivity)
  - pymysql (MySQL connector)
  
- **MySQL**: Data structuring and business intelligence queries

- **Power BI**: Interactive dashboard creation and visualization

- **Jupyter Notebook**: Analysis documentation and code execution

---

## 🔄 Workflow

1. **Data Preparation (Python/Pandas)**
   - Load raw CSV data (`customer_shopping_behavior.csv`)
   - Clean and validate data
   - Handle missing values and outliers
   - Feature engineering
   - Export cleaned data (`customer_behavior_cleaned.csv`)

2. **Database Setup (Pandas → MySQL)**
   - Convert cleaned CSV to SQL using pandas `.to_sql()` method
   - Load data into MySQL database
   - Create appropriate indexes and relationships

3. **Data Analysis (MySQL)**
   - Execute SQL queries for business insights
   - Perform customer segmentation
   - Analyze purchase patterns and trends
   - Calculate loyalty and retention metrics

4. **Visualization (Power BI)**
   - Connect Power BI to MySQL database
   - Build interactive dashboards
   - Create data-driven insights and visualizations

---

## 📈 Key Features

### 1. Data Preparation & Modeling (Python)
- Data cleaning and quality assessment
- Handling missing values and outliers
- Feature engineering and transformation
- Exploratory Data Analysis (EDA)
- CSV to MySQL conversion using pandas

### 2. Data Analysis (MySQL)
- Customer segmentation analysis
- Purchase pattern identification
- Loyalty and retention metrics
- Revenue and product performance analysis
- Complex queries for business intelligence

### 3. Visualization & Insights (Power BI)
- Interactive dashboard with key performance indicators
- Customer demographic analysis
- Product category performance
- Seasonal trends and patterns
- Real-time data connectivity to MySQL database

---

## 🚀 Getting Started

### Prerequisites
```bash
Python 3.8+
Jupyter Notebook
MySQL Server
Power BI Desktop
```

### Installation

1. **Clone the repository**
```bash
git clone https://github.com/yourusername/customer-behavior-analysis.git
cd customer-behavior-analysis
```

2. **Install Python dependencies**
```bash
pip install pandas numpy matplotlib seaborn jupyter sqlalchemy pymysql
```

3. **Set up MySQL Database**
```bash
# Start MySQL server and create database
mysql -u root -p
CREATE DATABASE customer_behavior;
```

4. **Run the Analysis**
```bash
# Open Jupyter Notebook
jupyter notebook customer_behavior.ipynb

# The notebook includes:
# - Data cleaning and transformation
# - CSV to MySQL database conversion using pandas
# - SQL queries execution via MySQL
```

5. **Open Power BI Dashboard**
- Open `customer_behavior_dashboard.pbix` in Power BI Desktop
- Update MySQL data source connections as needed
- Refresh data to load latest insights

---

## 📊 Dataset Description

The dataset contains customer shopping behavior with the following attributes:

| Column | Description |
|--------|-------------|
| Customer ID | Unique identifier for each customer |
| Age | Customer age |
| Gender | Customer gender |
| Item Purchased | Product name |
| Category | Product category |
| Purchase Amount (USD) | Transaction value |
| Location | Customer location |
| Size | Product size |
| Color | Product color |
| Season | Season of purchase |
| Review Rating | Product review (1-5 scale) |
| Subscription Status | Subscription membership status |
| Shipping Type | Delivery method |
| Discount Applied | Whether discount was applied |
| Promo Code Used | Whether promo code was used |
| Previous Purchases | Number of previous purchases |
| Payment Method | Payment method used |
| Frequency of Purchases | Purchase frequency category |

---

## 💻 Technical Implementation

### Python to MySQL Pipeline

The project uses pandas to seamlessly convert CSV data to MySQL:

```python
import pandas as pd
from sqlalchemy import create_engine

# Read cleaned CSV
df = pd.read_csv('customer_behavior_cleaned.csv')

# Create MySQL connection
engine = create_engine('mysql+pymysql://username:password@localhost/customer_behavior')

# Export to MySQL
df.to_sql('customer_transactions', con=engine, if_exists='replace', index=False)
```

### Key SQL Analyses

- Customer lifetime value calculation
- Cohort analysis for retention tracking
- RFM (Recency, Frequency, Monetary) segmentation
- Product affinity analysis
- Seasonal trend identification

---

## 🔍 Key Insights

*This section will be populated with findings from the analysis, including:*

- **Customer Segmentation**: Demographics and behavior patterns
- **Purchase Drivers**: Impact of discounts, reviews, and seasonality
- **Product Performance**: Top-performing categories and items
- **Channel Analysis**: Online vs. offline purchasing trends
- **Loyalty Patterns**: Factors influencing repeat purchases
- **Revenue Optimization**: Recommendations for pricing and promotions

---

## 📌 Business Recommendations

*Key recommendations based on analysis:*

1. **Marketing Strategy**: Target specific customer segments with personalized campaigns
2. **Product Optimization**: Focus on high-performing categories and items
3. **Pricing Strategy**: Optimize discount strategies based on customer sensitivity
4. **Inventory Management**: Align stock with seasonal demand patterns
5. **Loyalty Programs**: Design retention strategies for high-value customers
6. **Channel Strategy**: Enhance digital or physical presence based on preferences

---

## 📄 Deliverables

- ✅ Cleaned and transformed dataset
- ✅ Python analysis notebook with comprehensive EDA
- ✅ MySQL database with structured customer data
- ✅ SQL queries for business intelligence
- ✅ Interactive Power BI dashboard
- ✅ Project report with findings and recommendations
- ✅ Stakeholder presentation

---

## 📝 License

This project is licensed under the MIT License

---


## 🔄 Future Enhancements

- [ ] Implement machine learning models for customer churn prediction
- [ ] Add real-time dashboard capabilities with live MySQL connection
- [ ] Expand analysis to include customer lifetime value (CLV) modeling
- [ ] Integrate with CRM systems for automated insights
- [ ] Develop recommendation engine for personalized marketing
- [ ] Add predictive analytics for inventory forecasting

---

**Last Updated**: March 2026
