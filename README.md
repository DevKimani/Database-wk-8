# Database-wk-8

# E-commerce Store Database Management System

A comprehensive **MySQL relational database schema** designed for an **e-commerce store**, covering product management, customers, orders, payments, inventory, and more.  
This schema is built with **best practices** for scalability, performance, and data integrity.

---

## Features
- **Customer Management**
  - Securely stores customer profiles with email validation.
  - Supports multiple shipping and billing addresses.

- **Product Management**
  - Hierarchical product categories.
  - Multiple images per product with one designated primary image.
  - Supplier tracking with primary supplier support.

- **Order Management**
  - Full order lifecycle: pending → processing → shipped → delivered → cancelled/refunded.
  - Support for coupons and discounts.

- **Shopping Cart**
  - Persistent carts linked to customer accounts.

- **Payments**
  - Multiple payment methods supported: credit card, debit card, PayPal, bank transfer.
  - Tracks payment statuses and transaction IDs.

- **Inventory Management**
  - Logs all stock changes through inventory transactions.

- **Reviews**
  - Customer product reviews with moderation.

- **Coupons & Discounts**
  - Supports percentage or fixed amount discounts.
  - Configurable start and end dates, usage limits, and active/inactive toggling.

---

## 🗂 Database Structure

### Core Tables
| Table               | Purpose |
|---------------------|---------|
| **customers**       | Stores customer information with secure password hash and email validation. |
| **addresses**       | Stores billing and shipping addresses for each customer. |
| **categories**      | Self-referencing hierarchical categories. |
| **products**        | Stores product details including stock, price, and status. |
| **product_images**  | Product images, with support for a primary image. |
| **orders**          | Tracks customer orders and status. |
| **order_items**     | Line items in each order (many-to-many relationship between orders and products). |
| **payments**        | Tracks payments for orders. |
| **reviews**         | Customer reviews and ratings for products. |
| **shopping_cart**   | Persistent shopping cart linked to a customer. |
| **cart_items**      | Items within a customer's shopping cart. |
| **coupons**         | Discount codes with start/end dates and usage limits. |
| **order_coupons**   | Tracks which coupons are applied to which orders. |
| **suppliers**       | Supplier details for products. |
| **product_suppliers**| Many-to-many relationship between products and suppliers. |
| **inventory_transactions** | Logs all inventory movements like purchases, sales, and adjustments. |

**ERD Diagram can be accessed here: https://www.mermaidchart.com/app/projects/a6e33b5b-16d3-4820-acc9-16b0461c3112/diagrams/cdfbb47f-5891-4b4a-925e-3bfd66b5d2ec/version/v0.1/edit**


