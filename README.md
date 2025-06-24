# Coffee-Sales-Report
## 📘 README: Coffee Shop Sales Dashboard (Power BI Project)
## 🧭 Objective
This project aims to evaluate a coffee shop's sales performance by analyzing business dimensions such as product types, categories, store locations, and sales trends — broken down by months and days. The goal is to uncover patterns, compare performance across timeframes and variables, and support data-driven decision-making through interactive dashboards.

## 📌 Stakeholder Requirements
The project was guided by a clear set of KPI and Chart Visualization requirements provided by the stakeholders. These were essential to ensure the dashboard delivered relevant and actionable insights.

## ✅ KPI Requirements
## The stakeholders outlined the following metrics to be tracked and visualized month by month:
1. Total Sales Analysis
Calculate the total sales for each respective month.
Determine the month-over-month (MoM) increase or decrease in sales.
Calculate the difference in sales between the selected month and the previous month.
2. Total Orders Analysis
Calculate the total number of orders for each respective month.
Determine the MoM increase or decrease in the number of orders.
Calculate the difference in order count between the selected month and the previous month.
3. Total Quantity Sold Analysis
Calculate the total quantity sold for each respective month.
Determine the MoM increase or decrease in the total quantity sold.

 ## 📊 Chart Requirements
## To ensure visual clarity and business impact, stakeholders requested the following chart-based deliverables:
1. Calendar Heat Map
Implement a calendar heatmap that dynamically adjusts based on the selected month via slicer.
Use color gradients to represent sales volume (darker = higher sales).
Add tooltips showing detailed metrics (Sales, Orders, Quantity) when hovering over a specific date.
2. Sales Analysis by Weekdays and Weekends
Segment the data into weekdays vs weekends to examine sales performance.
Provide a clear view of how sales patterns vary across these timeframes.
3. Sales Analysis by Store Location
Display sales figures broken down by individual store locations.
Include MoM difference metrics for each location based on the selected month.
Highlight stores with sales increases or declines to spot regional trends.

## 🗃️ Data Collection
The dataset for this project was sourced from Kaggle and came in the form of an Excel(.xlsx) file. It contains simulated retail data representing the sales of a coffee shop over  six months in 2023.
## Key fields in the dataset include:
  1. Transaction Date
  2. Store Location
  3.  Product Name
  4. Product Category
  5. Product Type
  6. Order Quantity
  7. Sales Value
This structured dataset enabled analysis of business performance by time, product types, categories, and geographic locations.

 ## 🧹 Data Cleaning & Preparation
 To prepare the dataset for analysis, several cleaning and transformation steps were  performed using Power Query in Power BI:
  1. The transaction date, originally stored as text, was converted to the correct date/time data type to support time-based analysis.
  2 .New calculated columns were added, such as Sales Per Month, to enable trend evaluation.
  3. A thorough quality check was conducted for each column to assess data completeness and structure.
  4. Blank or null values were carefully reviewed. Only the values deemed unnecessary or irrelevant were removed, preserving the integrity of the            dataset.
  5. Once data validation was completed and no null values remained, the cleaned data was loaded    into Power BI Desktop for further analysis and visualization.

 ## ⚙️ Data Processing / Feature Engineering
  Several new columns and calculated fields were created to enhance the analytical depth of      the dataset, particularly with a focus on date granularity for      sales reporting:

  A new Total Sales column was calculated by multiplying quantity by unit price (if not already provided).
  Hour of Sale was extracted from the datetime field to analyze time-based buying behavior.
  A Date Table was generated using DAX formulas to support time intelligence and reporting. 
  ## This table includes:
    1. Day Name
    2. Day Number
    3. Month Name
    4. Week Number
    5. Weekday/Weekend Flag
  These enhancements were essential for analyzing monthly performance, order trends, and sales volume with more precision.
## 🧠 Sales Analysis Logic
  To summarize and evaluate sales performance effectively, a set of Key Performance Indicators (KPIs) were implemented in line with stakeholder requirements.        These KPIs were     calculated using DAX measures and calculated columns in Power BI.
  ![Dashboard KPI](https://github.com/sangralArsha/Coffee-Sales-Report/blob/main/Coffee%20Sales%20KPI.png)

## The following metrics were developed:
  1. Total Sales – total revenue for the selected month
  2. Total Orders – number of transactions completed in the month
  3. Total Quantity Sold – total units/products sold during the month
  4. Each of these metrics was designed to meet the stakeholder requirements, including:
  5. Calculating values month by month
  6. Computing Month-over-Month (MoM) performance: showing how each KPI changed compared to the previous month
  7. Displaying the difference in raw values between the selected month and the previous one
## These KPIs are prominently shown at the top of the dashboard using card visuals with:
  
  1. Clear numbers (e.g., $157K total sales)
  2. Percentage change vs. last month (e.g., +31.8%)
  3. Small sparklines to indicate the trend line or seasonality pattern throughout the month
  4. These visual and analytical elements align directly with the stakeholder's request to monitor:
  5. Month-to-month growth or decline
  6. Fluctuations in volume and revenue
  7. Summary differences between selected and previous periods
     
## 📊 Dashboard Design
The Power BI dashboard consists of a single interactive page that provides a comprehensive snapshot of coffee shop sales for a selected month (e.g., May 2023). It’s designed to be both visually engaging and insight-rich.
![Dashboard KPI](https://github.com/sangralArsha/Coffee-Sales-Report/blob/main/Coffee%20Sales%20Dashboard.png)

## Key Features:
## Slicers for filtering by:
    
    1. Month/Year
    2. Calendar day selection
    
## KPIs with Sparklines:
    
    1. Total Sales ($157K)
    2. Total Orders (33,527)
    3. Total Quantity Sold (48,233)
    
## Each KPI also displays percentage change compared to the last month (LM)
## Visual Components:
    1. Bar chart for daily sales trend
    2. Doughnut chart for weekday vs weekend contribution
    
## Bar charts for:
    1. Product category sales
    2. Product type sales
    3. Store-wise sales (with MoM comparison)
    4. Heatmap for hourly sales by weekday
    
## User Interactivity:
    1. Hovering over visuals reveals precise values
    2. Slicers allow dynamic filtering across all visuals
    3. Color coding helps in spotting performance gaps and highlights
    
    This layout offers clear visibility into what sells, where, and when, making it an ideal tool for stakeholders to identify sales drivers and take data-           informed actions.

## 📈 Key Insights
## Here are the most valuable findings from the sales analysis of May 2023:

  1. Total Sales reached $157K, showing a +31.8% increase compared to the last month, along with   similar growth in total orders (+32.3%) and quantity sold.
   Weekdays contributed the majority of sales with $117K (74.41%), while weekends accounted for only $40K (25.59%).
  2. The top-performing store location was Hell's Kitchen with $52.60K in sales, followed closely by Astoria and Lower Manhattan — all showing over +30% growth       vs last month.
  
  In terms of products:
  1. Coffee was the highest selling category at $60.36K, followed by Tea ($44.5K) and Bakery items ($18.5K).
  2. Barista Espresso and Brewed Chai Tea were the best-selling product types.
  3. Sales peaked during the morning hours (8–10 AM), especially around 9 AM which alone contributed $20K in sales for the month.

## 🧩 Challenges & Lessons Learned
  This project offered valuable learning experiences, particularly in data visualization and DAX logic. Some key lessons and challenges included:
  1. Understanding how matrix visuals can be used as heatmaps in Power BI was a major learning     breakthrough. It helped in identifying patterns like peak sales hours across weekdays.
  2.  Writing different DAX measures to calculate KPIs and support time-based analysis was initially challenging but highly rewarding.
  3. Designing a clean, well-structured dashboard that tells a clear and intuitive data story was one of the most time-consuming but important parts of the project.
  4. These experiences strengthened skills in data modeling, visual storytelling, and user-focused design thinking.
     
## 💡Future Improvements
  With additional time and resources, I would enhance the project by adding a Forecasting & Projections dashboard page. This would use Power BI’s built-in analytics capabilities to predict future sales trends and provide strategic foresight.
  Planned visuals would include:
  1. Forecast Line Chart showing predicted sales for upcoming months based on historical data   

## ✅ Conclusion
  This project successfully met its goal of analyzing and visualizing coffee shop sales data using Power BI. I’m proud of how the dashboard turned out — not only because it is visually clean, but also because it tells a meaningful story using real business KPIs. Throughout the process, I strengthened my skills in DAX, Power Query, and time-based analysis. Most importantly, I learned how to structure insights in a way that helps stakeholders make data-driven decisions. This was a valuable hands-on experience in building a complete business intelligence solution from raw data to interactive reporting.
    
  
      
