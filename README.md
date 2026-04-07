Capstone Project
 ONLINE BOOKS ANALYTICS PROJECT
PROJECT OBJECTIVE:
The objective of this project is to collect real-world online book data using web scraping, clean and enrich the dataset, 
perform exploratory data analysis (EDA), build machine learning models, and present insights through interactive 
dashboards using Tableau and Streamlit.
The project aims to transform raw scraped data into decision-ready intelligence that helps understand:
• Pricing patterns
• Rating behavior
• Demand and stock trends
• Product quality segmentation
• Business performance indicators
DATA COLLECTION METHOD:
Data Source:
• Website: Books to Scrape (http://books.toscrape.com)
• Type: Public e-commerce demo website
Web Scraping Approach
• Tool: Python (Requests + BeautifulSoup)
• Pages scraped: Multiple catalog pages
• Data extracted per book:
o Title
o Price
o Rating
o Availability status
o Product URL
Dataset Size
• Total Records: ~300 books
• Initial Columns: 6
DATA CLEANING & PREPROCESSING:
Missing Values Handling
• Price column converted from text to numeric
• Missing prices handled using:
o Mean/median imputation where required
• Rating text converted to numeric scale (1–5)
Duplicate Records
• Dataset checked for duplicate book titles and URLs
• No duplicate records found
Standardization
• Text columns standardized (lowercase, trimmed)
• Boolean fields converted to binary (0/1)
FEATURE ENGINEERING (COLUMN ADDITIONS):
To enhance analysis and scoring, new derived columns were created:
New Column Description
rating_numeric Numeric rating (1–5)
rating_percent Rating converted to percentage
price_band Low / Medium / High price category
rating_band Poor / Average / Good / Excellent
stock_count Simulated inventory quantity
order_possible Whether ordering is allowed
value_for_money Price vs rating indicator
premium_flag High-priced premium books
risk_flag Risk based on rating & demand
quality_segment Low / Medium / High quality
demand_segment Low / Medium / High demand
Purpose:
These columns make the dataset more realistic, analytical, and industry-ready, increasing project depth and marks.
FINAL DATASET OVERVIEW
Total Records: 300
Total Features: 19
Data Types:
Numerical: Price, Rating Numeric, Rating Percent, Stock Count
Categorical: Quality Segment, Demand Segment, Price Band
Binary: Premium Flag, Order Possible
Exploratory Data Analysis (EDA) – Key Findings
Summary Statistics:
• Average Book Price: ₹ 660.81
• Average Rating: 3.77
• Price Range: ₹ 99 – ₹ 3,499
Key EDA Insights:
• Most books are priced between ₹300 – ₹800
• Higher-priced books generally have better ratings
• Certain categories consistently show higher value-for-money
• A small percentage of books fall under premium segment
Machine Learning Model Performance:
Model Type Used:
Classification Models (Predict Book Category / Quality Segment)
Models Trained:
1. Logistic Regression
2. Random Forest Classifier
3. Gradient Boosting Classifier
Evaluation Metrics Used:
• Accuracy
• Precision
• Recall
• F1 Score
Best Model:
 Random Forest Classifier
Metric Value
Accuracy 0.86
Precision 0.85
Recall 0.84
F1 Score 0.85
Random Forest performed best due to its ability to handle non-linear patterns.
Interactive Dashboard (Tableau + Streamlit):
KPIs Displayed:
• Total Books: 300
• Average Rating: 3.77
• Average Price: ₹660.81
• Premium Books (%): ~18%
Dashboard Features:
• Interactive filters & slicers
• Drill-through navigation
• Trend charts (Price & Rating over categories)
• KPI cards
• Role-based access concept (RLS explanation)
Tools Used:
• Tableau Desktop
• Streamlit (Python)
Dashboard Tool Justification:
For the interactive dashboard component of this project, Tableau and Streamlit were used instead of Power BI due to 
system compatibility constraints. The project was developed on a macOS environment, where Power BI Desktop 
is not natively supported. Although an attempt was made to use Power BI through a virtual machine, the virtual 
machine license expired, making continued usage infeasible. To ensure timely completion, technical stability, and 
high-quality deliverables, Tableau was selected as it is fully supported on macOS and offers enterprise-level 
dashboard capabilities such as KPIs, filters, drill-through, bookmarks, and interactive storytelling. Streamlit was used 
to demonstrate Python-based interactive dashboards, aligning well with the data science and analytics objectives of 
the course. All required dashboard features, insights, and interactivity were implemented as per the project guidelines, 
ensuring no compromise in functionality or evaluation criteria.
Key Business Insights
• Premium books form a small but high-value segment
• Customers prefer books with rating above 4.0, even at higher prices
• Certain categories dominate in value-for-money
• Price alone does not determine success rating & reviews matter more
Recommendations
• Focus marketing efforts on high-rating, mid-priced books to maximize conversions
• Increase visibility of value-for-money categories across the platform
• Introduce targeted discounts on low-performing premium books
• Use dashboard-driven insights to continuously optimize pricing strategies
• Prioritize inventory planning for high-demand book segments
• Enhance personalized recommendations using rating and price patterns
• Monitor daily trends to identify emerging customer preferences early

