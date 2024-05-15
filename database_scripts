CREATE SCHEMA raksha_pipes;
USE raksha_pipes;

CREATE TABLE Categories (
    CategoryID INT PRIMARY KEY,
    CategoryName VARCHAR(255),
    Description TEXT
);

CREATE TABLE Products (
    ProductID INT PRIMARY KEY,
    Name VARCHAR(255),
    Description TEXT,
    CategoryID INT,
    UnitPrice DECIMAL(10, 2),
    StockQuantity INT
);

CREATE TABLE Customers (
    CustomerID INT PRIMARY KEY,
    CustomerName VARCHAR(255),
    ContactName VARCHAR(255),
    Address TEXT,
    Phone VARCHAR(50),
    Email VARCHAR(255)
);

CREATE TABLE Orders_details (
   order_id INT PRIMARY KEY,
    product_id INT,
	customer_id INT,
    quantity int,
    OrderDate DATE
);

CREATE TABLE Sales (
    SaleID INT AUTO_INCREMENT PRIMARY KEY,
    TotalSales DECIMAL(10, 2),
    SalesByCategory VARCHAR(255),
    SalesByProduct VARCHAR(255),
    SalesByRegion VARCHAR(255),
    SalesByCity VARCHAR(255)
);

CREATE TABLE InventoryManagement (
    InventoryID INT AUTO_INCREMENT PRIMARY KEY,
    ProductID INT,
    CurrentStockLevels INT,
    InventoryTurnoverRate DECIMAL(10, 2),
    StockAlerts VARCHAR(50)
);

CREATE TABLE FinancialMetrics (
    MetricID INT AUTO_INCREMENT PRIMARY KEY,
    Revenue DECIMAL(10, 2),
    Costs DECIMAL(10, 2),
    GrossMargin DECIMAL(10, 2),
    ProfitabilityByProductCategory VARCHAR(255)
);

CREATE TABLE Employees (
    EmployeeID INT PRIMARY KEY,
    EmployeeName VARCHAR(255) NOT NULL,
    Positions VARCHAR(50),
    Department VARCHAR(50),
    HireDate DATE,
    Phone VARCHAR(50),
    CustomerID INT,
    MetricID INT
);
CREATE TABLE Orders (
    OrderID INT PRIMARY KEY,
    CustomerID INT,
    ProductID INT,
    OrderDate DATE,
    Quantity INT,
    TotalPrice DECIMAL(10, 2),
    Status VARCHAR(50),
    SaleID  int
);
