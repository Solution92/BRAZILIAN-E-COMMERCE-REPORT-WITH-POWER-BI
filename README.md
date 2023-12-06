# BRAZILIAN-E-COMMERCE-REPORT-WITH-POWER-BI

### Table of Content
- [Project Objective](#project-objective)
- [Data Source](#data-source)
- [Tools Used](#tools-used)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Exploratory Data Analysis (EDA)](#exploratory-data-analysis-eda)
- [Data Analysis](#data-analysis)
- [The Dashboard](#the-dashboard)
- [Result and Findings](#result-and-findings)
- [Recommendation](#recommendation)
- [Limitation](#limitation)
- [Reference](#reference)



### Project Objective

To review and understand best-selling Products through customer Review analysis and do product sales prediction.

### Data Source

The dataset was provided in a CSV file format by the client which I am not permitted to disclose.

### Tools Used

- Power BI — Data Cleaning, Transformation, Analysis, and Creating Reports.

### Data Cleaning and Preparation

The Dataset has nine (9) different tables — Olist Customer Dataset, Olist geolocation Dataset, Olist Order items Dataset, Olist Order payment, Order review, Orders Dataset, products Dataset, sellers Dataset, and product Category name translation.

The dataset has information on 100k orders (according to the information given) from 2016 to 2018 made at multiple marketplaces in Brazil. Its features allow viewing orders from multiple dimensions: from order status, price, payment, and freight performance to customer location, product attributes, and finally reviews written by customers.

There is also a released geolocation dataset that relates Brazilian zip codes to lat/lng coordinates. This is real commercial data.

To successfully Analyze these different tables I loaded the different Datasets to Power query editor and merged all with their unique primary keys.

Created a Conditional Column to represent Customer Review Category levels;

Thus; 5 — Very Good, 4 — Good, 3 — Average, 2 — Poor, and, 1 — Very Poor.

Created a new custom column to Calculate the days from the purchase date and delivery date — Average Delivery Time: with column name “Delivery Day(s)” and the result was in hours, minutes, and seconds (hms). So, to achieve my goal of how many days (s) it took to deliver the goods to a customer I had to convert the column to Day by highlighting the column then from the “Add Column” pane click on the “Duration” pane and it created another column with the number of days which is named Average Delivery Day(s).

Replaceed a lot of ‘null’ values with zero which could hamper data standardization. Cleaning and removing some major errors which brought my Dataset to about 32 Columns and over 10,000 rows.

### Exploratory Data Analysis (EDA)

I have generated the following key Performance Indicators (KPIs) and insights:

KPIs

- Total Orders
- Total Products
- Total Sales
  
INSIGHTS
- Product Review
- Product Delivery by Customer City
- Ordered Products by Year
- Order Purchase by Day
- Order Purchase by Status
- % of Product Delivered by Year
- Commonly Purchased Products by Customer City
- Customer Review Score

### Data Analysis

- Total Orders = SUM(‘Brazilian_E-Commerce’[order_purchase_Year])
- Total Products = DISTINCTCOUNT(‘Brazilian_E-Commerce’[product_category_name_english])
- Total Sales = SUM(‘Brazilian_E-Commerce’[payment_value])

### The Dashboard

![Screenshot_146](https://github.com/Solution92/BRAZILIAN-E-COMMERCE-REPORT-WITH-POWER-BI/assets/144762124/b02f2bf8-5d30-4b2b-bca0-8c3a796e9e7f)

### Result and Findings

- At 55,657, Very Good had the highest Count of product_category_name and was 26,403.33% higher than 0, which had the lowest Count of product_category_name at 210.  Very Good accounted for 57.69% of Count of product_category_name.  Across all 6 Review_Categories, Count of product_category_name ranged from 210 to 55,657.  
- Additionally, at 11,297, August had the highest Count of customer_city and was 175.74% higher than September, which had the lowest Count of customer_city at 4,097.  August accounted for 11.71% of Count of customer_city.  Across all 12 Month, Count of customer_city ranged from 4,097 to 11,297.  
 Count of product_category_name trended up, resulting in a 20,220.22% increase between 2016 and 2018.  Count of product_category_name started trending up on 2016, rising by 20,220.22% (54,999) in 2 years.  Count of product_category_name jumped from 272 to 55,271 during its steepest incline between 2016 and 2018.  
- Count of Order_Purchase_Month for delivered (96,465) was higher than canceled (6).  Delivered accounted for 99.99% of Count of Order_Purchase_Month.  
- Count of product_category_name was highest for Sao Paulo at 15,111, followed by rio de janeiro and belo horizonte.  Sao Paulo accounted for 15.66% of Count of product_category_name.  Across all 4,082 customer_city, Count of product_category_name ranged from 1 to 15,111.  
- Finally, at 15,703, Monday had the highest Count of product_category_name and was 48.77% higher than Saturday, which had the lowest Count of product_category_name at 10,555. Monday accounted for 16.28% of Count of product_category_name.  Across all 7 Order_Purchase_Day, Count of product_category_name ranged from 10,555 to 15,703.

### Recommendation

- Based on the analysis, it is evident that the product category "Very Good" dominates with the highest count, suggesting its popularity. 
- August appears to be a peak month for customer activity, while Mondays show higher engagement compared to Saturdays. 
- The trend in product category count has experienced a significant increase from 2016 to 2018. 
- Considering these patterns, it is recommended to focus marketing efforts on promoting the "Very Good" category, capitalize on the heightened activity in August and on Mondays, and maintain a strategic approach to product offerings to align with the observed trends over the years.

### Limitation

- The table has limitations due to the absence of key contextual details, such as specific product attributes and customer demographics. 
- The lack of financial data and information on marketing channels restricts a comprehensive understanding of business performance and customer acquisition strategies. 
- Additionally, the dataset's relatively short time frame (2016 to 2018) may not capture long-term trends, and the focus on Brazilian transactions limits insights into global market dynamics. 
- Addressing these limitations by incorporating more comprehensive data sources would enhance the depth and accuracy of the analysis.


### Reference

Refer to Kaggle for all related datasets

Gracias

#data #powerbi #ecommerce #communication #teamwork #brazilian #analysis #analytics #dashboard #visualizasion #salesreport 















