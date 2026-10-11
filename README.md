# Customer Shopping Behavior Analysis

## Project Overview

This project analyzes customer shopping behavior to understand purchasing patterns, spending trends, product preferences, and customer loyalty. Using Python, PostgreSQL, and Power BI, the project transforms raw transaction data into meaningful business insights and actionable recommendations.

The analysis focuses on understanding how customer demographics, subscription status, discounts, shipping preferences, and purchase frequency relate to shopping behavior.

## Objectives

* Analyze customer purchasing patterns and spending behavior.
* Compare purchase amounts across customer demographics.
* Examine subscription status, discount usage, and shipping preferences.
* Identify highly rated products and customer preferences.
* Segment customers based on age and purchasing behavior.
* Develop data-driven recommendations for customer retention and marketing strategies.

## Tools and Technologies

* **Python:** Data preprocessing and analysis.
* **Pandas:** Data manipulation, cleaning, and feature engineering.
* **Jupyter Notebook:** Interactive data analysis and documentation.
* **PostgreSQL:** Storage and database integration for the processed dataset.
* **SQLAlchemy:** Connecting Python to PostgreSQL and loading data into database tables.
* **Power BI:** Dashboard development and visualization.

## Dataset Overview

The dataset contains **3,900 purchase records and 18 original columns**, covering customer demographics, products, transaction amounts, shopping preferences, and purchase frequency.

Key attributes include:

* Customer demographics: Age and Gender
* Product information: Item Purchased, Category, Size, Color, and Season
* Transaction details: Purchase Amount, Discount Applied, and Promo Code Used
* Customer behavior: Previous Purchases, Subscription Status, and Frequency of Purchases
* Shopping experience: Review Rating, Shipping Type, Payment Method, and Location

## Project Workflow

### 1. Data Loading and Exploration

* Imported the CSV dataset using Pandas.
* Inspected the dataset structure, data types, summary statistics, and missing values.
* Identified missing values in the Review Rating column.

### 2. Data Cleaning and Preprocessing

* Imputed missing review ratings using the median rating within each product category.
* Standardized column names by converting them to lowercase and replacing spaces with underscores.
* Renamed the purchase amount column for easier analysis.
* Removed the Promo Code Used column after checking that its values matched Discount Applied in the dataset.

### 3. Feature Engineering

* Created an `age_group` feature by dividing customer ages into four quantile-based groups: Young Adult, Adult, Middle-aged, and Senior.
* Created `purchase_freq_days` by mapping purchase-frequency categories to approximate day intervals.
* Prepared the dataset for further analysis and visualization.

### 4. PostgreSQL Integration

* Connected Python to PostgreSQL using SQLAlchemy and the PostgreSQL database driver.
* Loaded the processed dataset into a database table named `customer`.
* Prepared the data for database-based exploration and reporting.

### 5. Power BI Dashboard and Business Analysis

Developed a dashboard to explore key areas of customer shopping behavior, including:

* Revenue comparison by gender
* High-value customers using discounts
* Top-rated products
* Average purchase amounts by shipping type
* Subscription behavior and customer spending
* Customer segmentation and loyalty
* Business recommendations based on observed patterns

## Key Findings

The analysis and accompanying presentation highlight the following observations:

* **Gender and revenue:** Female customers generated slightly higher total revenue than male customers.
* **Discount usage:** Customers who use discounts while spending above average represent a potential high-value customer segment.
* **Product ratings:** Blouse and Dress received strong ratings, while Shirt also showed positive customer feedback.
* **Shipping preferences:** The presentation reports an average purchase amount of $65 for Express Shipping compared with $58 for Standard Shipping.
* **Subscription behavior:** The presentation reports higher spending among subscribers and identifies subscription customers as an important revenue segment.
* **Customer segmentation:** The presentation divides customers into Loyal, Returning, and New segments, with an emphasis on converting first-time buyers into repeat customers.

These findings are descriptive and indicate opportunities for further investigation; they do not establish that a particular shopping preference causes higher spending.

## Business Recommendations

* **Improve customer retention:** Introduce loyalty rewards and targeted engagement campaigns.
* **Grow subscriptions:** Promote subscriber benefits and evaluate subscription conversion opportunities.
* **Personalize marketing:** Target customer segments based on purchasing behavior and spending patterns.
* **Promote highly rated products:** Use customer ratings to inform product recommendations and marketing campaigns.
* **Evaluate shipping preferences:** Investigate whether express shipping is associated with higher purchase amounts and customer value.

## Project Files

* `Customer_Shopping_Behaviour_Analysis.ipynb` — Python data cleaning, exploratory inspection, and feature engineering.
* `customer_shopping_behavior.csv` — Original customer shopping dataset.
* `customer_behavior_dashboard.pbix` — Power BI dashboard file.
* `Customer-Shopping-Behavior-Analysis.pptx` — Project presentation summarizing insights and recommendations.

## How to Run

1. Clone or download this repository.

2. Install the required Python libraries:

   ```bash
   pip install pandas sqlalchemy psycopg2-binary jupyter
   ```

3. Open `Customer_Shopping_Behaviour_Analysis.ipynb` in Jupyter Notebook.

4. Ensure the CSV file is available at the path specified in the notebook.

5. Configure PostgreSQL with an appropriate database and update the connection settings.

6. Run the notebook cells in order to reproduce the data preparation and database-loading workflow.

7. Open `customer_behavior_dashboard.pbix` in Power BI Desktop to explore the dashboard.

**Note:** Configure database credentials through environment variables or another secure configuration method rather than committing passwords to GitHub.

## Conclusion

This project demonstrates a practical data analytics workflow, from raw data exploration and preprocessing to feature engineering, database integration, dashboard reporting, and business recommendations. It showcases how data analytics tools can help organizations better understand customer behavior and identify opportunities to improve marketing, engagement, and retention.
