# Database Plan

This project uses a relational database to manage customers, staff, suppliers, products, orders and order line items.

## Tables

### Customer

Stores customer information.

Fields:

- customer_id
- first_name
- last_name
- email
- phone
- address
- created_at

### Staff

Stores staff user information.

Fields:

- staff_id
- first_name
- last_name
- email
- password_hash
- role
- created_at

### Supplier

Stores supplier information.

Fields:

- supplier_id
- supplier_name
- contact_email
- phone
- address
- created_at

### Product

Stores clothing stock/product information.

Fields:

- product_id
- supplier_id
- product_name
- category
- size
- colour
- price
- stock_quantity
- reorder_level
- created_at

### Order

Stores customer orders.

Fields:

- order_id
- customer_id
- staff_id
- order_date
- status
- total_amount

### Order Line

Stores individual products inside an order.

Fields:

- order_line_id
- order_id
- product_id
- quantity
- unit_price
- line_total

## Relationships

- One customer can have many orders.
- One staff member can process many orders.
- One supplier can provide many products.
- One order can have many order lines.
- One product can appear in many order lines.

## Notes

The Order Line table is needed because one order can contain multiple products. It also stores the price at the time of purchase, so old orders stay accurate even if product prices change later.