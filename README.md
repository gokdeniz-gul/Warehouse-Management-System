# 📦 Warehouse Management System (C++)

A modern, robust, Object-Oriented C++ application designed to handle warehouse operations, inventory tracking, order processing, input validation, and report generation.

---

## 🚀 Features

### 1. 🛒 Product Management
- **Add Product:** Insert new products with unique IDs, names, quantities, and prices.
- **Search Product:** Search inventory by Product ID and view detailed product specs.
- **Update Product:** Dynamically modify product name, stock quantity, and price.
- **Delete Product:** Safely remove products from inventory.
- **Tax Calculation:** Automatic VAT (18%) calculation built into product models via polymorphism.

### 2. 📋 Order Management
- **Place Order:** Process customer orders while verifying real-time product stock and warehouse availability.
- **Order History:** View completed order history and tracking numbers.

### 3. 📊 Analytics & Reporting
- **Product Listing:** Display structured tables of all products in stock.
- **Critical Stock Report:** Identify low-stock items based on customizable threshold values.
- **Warehouse Analysis:** Calculate total inventory monetary value, stock occupancy rate, and capacity status.
- **Occupancy Warnings:** Custom C++ exception handling for capacity warnings and limits.

### 4. 🛡️ Input Validation
- Robust string, numeric, email, and range validation via dedicated `InputValidator` class to prevent runtime buffer issues and invalid data entries.

---

## 🏛️ System Architecture & OOP Design

The project strictly follows Object-Oriented Programming (OOP) principles:

- **Inheritance & Polymorphism:** `BaseProduct` (Abstract Base Class) is extended by `Product` to enforce interface implementations like `display()` and `calculateTax()`.
- **Encapsulation:** Private data members with clean public getters/setters across all model classes (`Product`, `Warehouse`, `Order`, `User`).
- **Exception Handling:** Custom exception classes (`WarehouseFullException` and `WarehouseOccupancyWarning`) deriving from `std::exception`.
- **Friend Functions:** `analyzeWarehouse` is integrated as a friend function to inspect internal warehouse data directly for analytical reporting.
