Create the Customer Table
CREATE TABLE Customer (
CustomerID INT PRIMARY KEY,
FirstName VARCHAR(50),
LastName VARCHAR(50),
Email VARCHAR(100),
Phone VARCHAR(15),
Address VARCHAR(255),
City VARCHAR(100),
State VARCHAR(50),
ZIPCode VARCHAR(15),
Country VARCHAR(100),

RegistrationDate DATE, LastPurchaseDate DATE
);


Create the Product Table
CREATE TABLE Product (
ProductID INT PRIMARY KEY, ProductName
VARCHAR(255), Description TEXT,
Category VARCHAR(50), Price DECIMAL(10, 2), StockQuantity INT,
Manufacturer VARCHAR(100),
Weight DECIMAL(8, 2), ReleaseDate DATE
);
Create the Sales Order Table
CREATE TABLE SalesOrder (
OrderID INT PRIMARY KEY, CustomerID INT,
OrderDate DATE,
ShipDate DATE,
ShippingAddress VARCHAR(255), ShippingCity VARCHAR(100), ShippingState VARCHAR(50), ShippingZIPCode VARCHAR(15), ShippingCountry VARCHAR(100),TotalAmount DECIMAL(10, 2), OrderStatus VARCHAR(20),FOREIGN KEY (CustomerID) REFERENCES Customer(CustomerID)
);
INSERT VALUES INTO TABLE
Insert sample data into the Customer table
INSERT INTO Customer (CustomerID, FirstName, LastName, Email, Phone, Address, City, State, ZIPCode, Country, RegistrationDate, LastPurchaseDate)
VALUES
(1, 'John', 'Doe', 'john.doe@email.com', '123-456-7890', '123 Main St', 'Los Angeles', 'CA', '90001', 'USA', '2023-01-15', '2023-08-20'),
(2, 'Alice', 'Smith', 'alice.smith@email.com', '987-654-3210', '456 Elm St', 'New York', 'NY', '10001', 'USA', '2023-02-20', '2023-09-05'),
(3, 'Bob', 'Johnson', 'bob.johnson@email.com', '555-123-4567', '789 Oak St', 'Chicago', 'IL', '60601', 'USA', '2023-03-10', '2023-07-30'),
(4, 'Emily', 'Davis', 'emily.davis@email.com', '111-222-3333', '101 Pine St', 'San Francisco', 'CA', '94101', 'USA', '2023-04-05', '2023-08-15'),
(5, 'David', 'Wilson', 'david.wilson@email.com', '444-555-6666', '222 Cedar St', 'Houston', 'TX', '77001', 'USA', '2023-05-12', '2023-09-10');

