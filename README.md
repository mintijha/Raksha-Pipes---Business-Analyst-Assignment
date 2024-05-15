# Raksha-Pipes---Business-Analyst-Assignment

Step -1 in python

Objective:

The objective of this task was to simulate the operations of Raksha Pipes by generating synthetic data that represents various aspects of the business, such as product inventory, customer interactions, sales transactions, employee information, and financial metrics. so,created a dataset that can be used for testing, analysis, and database development purposes.

Steps:-

Data Generation: You've used the faker library in Python to generate synthetic data for various entities such as products, customers, orders, employees, sales, inventory management, financial metrics, and categories.

Data Organization: The generated data has been organized into separate Pandas DataFrames for each entity, making it easier to manage and analyze.

Exporting to CSV: You've exported each DataFrame to a CSV file, enabling easy storage, sharing, and integration with database systems.

ERD Diagram: You've created an Entity-Relationship Diagram (ERD) to visualize the relationships between different entities in the database schema. This helps in understanding the structure of the database and the connections between various tables.


![ERD Diagram](https://github.com/mintijha/Raksha-Pipes---Business-Analyst-Assignment/assets/123978172/36eeba12-7f81-4b4d-8a54-d1908baa41ea)

Step -2 in my sql

Database Creation: 

 Rationale: The creation of a MySQL database is essential to store and manage the generated data in a structured and organized manner. 


 Purpose: The database serves as a central repository for Raksha Pipes' operational data, facilitating efficient data retrieval, manipulation, and analysis. 


Approach: Using SQL commands (CREATE SCHEMA and USE), a new database named "raksha_pipes_" was created, providing a dedicated environment for storing Raksha Pipes' data. 

Tables:-

Categories: This table stores information about product categories, including CategoryID, CategoryName, and Description.

Products: Stores details about products, such as ProductID, Name, Description, CategoryID (foreign key referencing Categories table), UnitPrice, and StockQuantity.

Customers: Contains details of customers, including CustomerID, CustomerName, ContactName, Address, Phone, and Email.

Orders_details: This table captures the details of each order, including order_id, product_id (foreign key referencing Products table), customer_id (foreign key referencing Customers table), quantity, and 
OrderDate.

Sales: Stores information related to sales transactions, such as SaleID, TotalSales, SalesByCategory, SalesByProduct, SalesByRegion, and SalesByCity.

InventoryManagement: Tracks inventory-related metrics, including InventoryID, ProductID (foreign key referencing Products table), CurrentStockLevels, InventoryTurnoverRate, and StockAlerts.

FinancialMetrics: Stores financial metrics data, such as MetricID, Revenue, Costs, GrossMargin, and ProfitabilityByProductCategory.

Employees: Contains information about employees, including EmployeeID, EmployeeName, Positions, Department, HireDate, Phone, CustomerID (foreign key referencing Customers table), and MetricID (foreign key referencing FinancialMetrics table).

Orders: This table captures order-related information, including OrderID, CustomerID (foreign key referencing Customers table), ProductID (foreign key referencing Products table), OrderDate, Quantity, TotalPrice, Status, and SaleID

imported CSV files into these tables that were exported from Python. This step helps populate the database with synthetic data generated using the Python script created a comprehensive database structure that mirrors the operations of Raksha Pipes, allowing for efficient data management and analysis.

Step 3 - in power bi

Connect Power BI to SQL Database 

Why: Connecting Power BI to the SQL database allows you to import data directly from your database into Power BI for analysis and visualization
Create Relationships in power bi  

·        Step: Define relationships between tables in Power BI's data model, based on common key columns, to enable cross-table analysis. 

·        Why: Establishing relationships ensures data integrity and enables seamless navigation and exploration of related data across multiple tables in your dashboard. 

Dashboarding in power bi  

·        Why: Power BI Desktop provides a user-friendly interface for designing and building insightful dashboards with data from various sources, including SQL databases. 

 ![Dashboard](https://github.com/mintijha/Raksha-Pipes---Business-Analyst-Assignment/assets/123978172/437d4ade-5845-42e6-9795-b64b489ec264)

Chart-1 sum of quantity by stauts 
Insights:

Highest Quantity: Cancelled orders have the highest sum of quantities, indicating a potential issue in the order fulfillment process that requires investigation.

Shipping Efficiency: Shipped orders closely follow Cancelled orders in quantity, suggesting efficient shipping processes or a high volume of orders in transit.

Order Fulfillment Rate: Delivered orders have a slightly lower sum of quantities compared to Cancelled and Shipped orders, indicating that a portion of orders are fulfilled but not yet delivered.

Pending Orders: Pending orders have the lowest sum of quantities, signaling potential delays or issues in processing these orders, which could impact customer satisfaction.

Overall Order Status Distribution: The distribution of order statuses suggests a need for optimization in the order management process to reduce cancellations, streamline shipping, and expedite order fulfillment to improve customer satisfaction and retention.

Business Insights:

Operational Efficiency: Understanding the reasons behind the high volume of cancelled orders can help identify operational inefficiencies, enabling targeted improvements to reduce cancellations and improve overall order processing efficiency.

Customer Experience: Analyzing the distribution of order statuses can provide insights into customer satisfaction levels. By addressing issues related to pending and delayed orders, businesses can enhance the customer experience and foster loyalty.

chart-2 sum of gross margin by profitability by product category

Insights:

Profitability Variation: PVC-U (unplasticised PVC) has the highest sum of gross margin, indicating it may be the most profitable product category among the listed PVC types.
Consistency in Profit Margins: There is a relatively consistent range of gross margins across the PVC product categories, with C-PVC, PVC-O, and Modified PVC following closely behind PVC-U.
Business Insights:

Product Performance Analysis: Understanding the profitability of each PVC product category allows businesses to evaluate the performance of their product lines. It provides insights into which categories contribute most significantly to overall profitability and where to focus resources for growth.

Strategic Decision-Making: Armed with insights into profitability by product category, businesses can make informed decisions regarding resource allocation, pricing strategies, and product development initiatives. They can prioritize investments in high-margin categories and optimize operations to maximize profitability.

chart -3 Sum of TotalSales by SalesByCity

Insights:

Highest Sales: Williamshire has the highest sum of total sales among the listed cities, indicating it is a significant market for the business.
Sales Disparity: There is a notable disparity in total sales between Williamshire and the other cities, suggesting that Williamshire may be a major economic hub or that the business has a strong presence or strategic focus in that area.

Business Insights:

Market Analysis: Analyzing sales data by city provides insights into regional market dynamics and customer preferences. Businesses can use this information to tailor marketing strategies, product offerings, and sales approaches to better meet the needs of customers in each city.

Expansion Opportunities: Identifying cities with high sales potential, such as Williamshire, can guide strategic decisions regarding expansion efforts. Businesses may consider allocating resources to capitalize on growth opportunities in these key markets or replicating successful strategies in other cities to drive sales growth.

chart - 4 Sum of TotalPrice by CustomerName

Insights:

Top Spenders: Zuniga, Perez and Jones are the top spenders among the listed customers, with the highest sum of total purchase amounts.

Variability in Spending: There is variability in total purchase amounts among customers, indicating differences in purchasing behavior and spending habits.

Business Insights:

Customer Segmentation: Identifying top-spending customers allows businesses to segment their customer base effectively. By understanding the needs and preferences of high-value customers like Zuniga, Perez and Jones, businesses can tailor marketing strategies and personalized offers to enhance customer satisfaction and loyalty.

Retention Strategies: Focusing on retaining and nurturing relationships with top-spending customers can yield significant returns. Businesses can invest in loyalty programs, exclusive perks, and exceptional customer service to strengthen relationships with these valuable customers and encourage repeat purchases.

chart - 5 Sum of SaleID by SalesByProduct

Top Selling Products: Plumbing Product has the highest sum of SaleIDs, indicating it is the top-selling product among the listed products.

Product Performance: There is variability in the number of SaleIDs among different products, suggesting differences in demand and popularity across product categories.

Business Insights:

Product Focus: Identifying top-selling products like Plumbing Product allows businesses to focus their resources and efforts on promoting these high-demand items. It enables them to optimize inventory management, production, and marketing strategies to capitalize on the popularity of these products and maximize sales revenue.

Diversification Opportunities: While Plumbing Product may be the top-selling item, businesses should also explore opportunities to diversify their product offerings. By analyzing sales data across product categories, they can identify emerging trends, niche markets, or underperforming products that warrant attention. Diversification can help mitigate risks associated with over-reliance on a single product and expand the customer base.

chart -6 Sum of StockQuantity by StockAlerts

Stock Quantity Distribution: The majority of products have a stock alert status of "Normal," with a significantly higher sum of stock quantities compared to those with a "Low" stock alert status. Business 

Insights:

Inventory Management: The higher sum of stock quantities with a "Normal" stock alert status suggests that the majority of products are adequately stocked to meet demand. However, products with a "Low" stock alert status may require immediate attention to avoid stockouts and potential revenue loss. Businesses should prioritize replenishing low-stock items to maintain optimal inventory levels and ensure product availability to meet customer demand.


***video link**
