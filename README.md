# OEM Plant Report

### Dashboard Image :
[OEM Plant Report.pdf](https://github.com/Soni-Sachin-94240/OEM-Plant-Report/files/15011330/OEM.Plant.Report.pdf)



## Problem Statement

Many retail businesses operate multiple stores, and analyzing store performance is crucial for making informed decisions. The current process of store analysis involves manual data collection, spreadsheets, and lacks a centralized, real-time reporting system. Over the next few fiscal years, the goal is to develop and implement a comprehensive "Store Analysis-Dashboard" that addresses these challenges and provides timely, accurate insights..

Design a user-friendly and visually appealing dashboard that allows stakeholders to easily interpret and interact with data.

And Identify and incorporate essential KPIs for store analysis, ensuring that the dashboard focuses on the metrics that matter most to the business.

### Datasource - PostgreSQL
For this dashboard I have used PostgreSQL database
 - Server: 192.%%%.1.74 , 192.%%%.1.26
 - Database: Lxon
 - Username: postgres
 - Password: admin

### Steps followed 

- Step 1: Create the necessary views for extracting data from the PostgreSQL database, such as Customer, Store, and Sales details.

  (a) Customer

   ![Customer](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/42b88a67-c475-4c8e-8cb1-5f6fcf9087aa)

  (b) Employee

  ![Employee](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/f9a13911-c1ff-47cc-ae47-9f8fa4c812d9)

  (c) Sales

  ![Sales](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/55dc2547-697c-4b00-a71e-b7a2818ba0c2)

  (d) Sales Details

  ![SalesDetails](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/f6ddf8e5-b0c6-4bd0-b5b6-1c5625469b3e)

  (e) Sales Dimension

  ![SalesDim](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/26aedac0-51a9-4ffd-af4c-93e958c7c6d4)

  (f) Store

  ![Store](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/797c8370-ce6f-455d-894c-6ab5daeea2c3)




- Step 2 : Load data into Power BI Desktop, dataset is from PostgreSQL database.

- Step 3 : Open power query editor & in view tab under Data preview section, check "column distribution", "column quality" & "column profile" options.

- Step 4 : Also since by default, profile will be opened only for 1000 rows so you need to select "column profiling based on entire dataset".

- Step 5 : It was observed that none of the columns contained errors or empty values. All the data in the table is directly fetched from the database through views, ensuring accurate column data types. Therefore, no further transformation is required.

- Step 6 : Include multiple slicers in the report to enable dynamic data reflection based on the selected slicer values. The Visual filters (Slicers) were added for four fields named "Financial Year", "Company", "Store" & "Customer"

  ![Slicers](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/a9bcb45c-651c-4a61-8da6-a0e32019967e)


- Step 7 : Create the necessary DAX measures for key performance indicators (KPIs), and attach snapshots with DAX queries for:

  (a) Total Sales

  ![Total Sales](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/4dd0f3dd-f497-418b-89ed-f99963f4deba)

  (b) Tax Amount

  ![Tax Amount](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/0e7912a4-8547-44ba-94f3-1e953ee6824c)

  (c) Total Paid Amount

  ![Total Paid Amount](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/84894d63-05f3-4c84-bb75-5fed8d318afc)

  (d) Average Sales per Company

  ![Avg Sales per Company](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/0afe696b-f4c3-418a-ac38-5ca075ba5786)

  (e) Average Sales per Store

  ![Avg Sales per Store](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/b7041eee-c4b9-41b1-b19e-bb0a96839bd1)

  (f) Average Sales per Customer

  ![Avg Sales per Customer](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/5952b300-3e9a-4e02-91b3-9c5ee549702d)

- Step 8 : Create the necessary visuals and charts to represent valuable or important key insights:

  (a) Total Sales by Fiscal Year (Selected) by Month : 

  The line chart clearly shows that the selected fiscal year (FY) 2022-23 had the highest sales in consecutive November, December, and January, while experiencing the lowest sales in March, April, and May

  ![1  Total Sales by Fiscal Year](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/64611bd6-94fc-4013-b891-37f204bc4ac6)


  (b) Finace Detail by Company : 

  The table visual includes the columns Company Name, Total Sales, Tax Amount, and Total Paid Amount

  ![2  Finance Detail by Company](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/441fd23f-9e65-403c-ab04-c97d2ae8481b)


  (c) Total Sales by States : 

  The Pie Chart represents that 'Hampshire' is the state with the highest sales, accounting for approximately 54% of the overall sales

  ![3  Total Sales by States](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/678a9995-41fa-41f0-bf50-c4099f3ad0a3)

  (d) Total Sales by Company : 

  The bar chart represents that 'Knights Pharmacy' is the company with the highest sales, accounting for approximately 7.4 million.

  ![4  Total Sales by Company](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/63c1cd3d-9b7f-4828-a398-03e194a13a22)


  (e) Total Sales by Stores : 

  The bar chart represents that 'Bristo Square' is the Store with the highest sales, accounting for approximately 0.40 million

  ![5  Total Sales by Store](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/9b9954d5-de28-4b30-8ee2-73b5ce770eb1)


  (f) Total Sales by Customer : 

  The bar chart represents that most customer details are not captured, which is why there is a blank customer with the highest sales, accounting for approximately 26 million

  ![6  Total Sales by Customer](https://github.com/Soni-Sachin-94240/Store_Analysis_Dashboard/assets/132342151/bfe477e1-0a63-4dc2-9172-53ea6ad78271)


### Conclusion 

In conclusion, the Store Analysis dashboard reveals valuable insights into the performance and trends within our store operations. Key takeaways include the identification of top-performing Company and Stores, notable sales patterns across different time periods, and a focus on high-performing regions or states. Additionally, the analysis points out areas for improvement, such as the need for better customer detail capture to enhance our understanding of sales distribution. These findings will inform strategic decisions to optimize sales, improve customer engagement, and ensure continued success in our retail operations.
