# Database Queries

### Display the ProductName and CategoryName for all products in the database. Shows 76 records.

    SELECT products.productName, categories.categoryName FROM [Categories]
    inner join products on categories.categoryID = products.categoryID

### Display the OrderID and ShipperName for all orders placed before January 9, 1997. Shows 161 records.

    SELECT * FROM [Orders]
    inner join shippers on orders.ShipperId = shippers.ShipperId Where OrderDate < '1997-01-09'

### Display all ProductNames and Quantities placed on order 10251. Sort by ProductName. Shows 3 records.
    SELECT Products.ProductName, OrderDetails.quantity
    FROM Products
    inner join OrderDetails on OrderDetails.ProductID = products.ProductID
    Where OrderDetails.OrderID = 10251

    orderDetails and ProductId
### Display the OrderID, CustomerName and the employee's LastName for every order. All columns should be labeled clearly. Displays 196 records.
    SELECT Orders.OrderId, customers.CustomerName, employees.lastName
    FROM Orders
    inner join customers on orders.customerId = customers.customerId
    inner join employees on orders.employeeId = employees.employeeId
### (Stretch)  Displays CategoryName and a new column called Count that shows how many products are in each category. Shows 9 records.

### (Stretch) Display OrderID and a  column called ItemCount that shows the total number of products placed on the order. Shows 196 records. 