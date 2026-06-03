# Clothing Order Management System

A full-stack order management system for a clothing e-commerce business.

## Tech Stack

- Frontend: React, TypeScript
- Backend: Java Spring Boot
- Database: PostgreSQL
- Tools: Git, GitHub, VS Code, Thunder Client/Postman

## Planned Features

- Staff login
- Customer management
- Stock/product management
- Supplier management
- Order creation
- Order line items
- Order status tracking
- Low-stock warnings
- Dashboard statistics

## Project Goal

The aim of this project is to demonstrate full-stack software development skills, including database design, REST API development, frontend design, authentication, validation and testing.

## Current Progress

- Project repository created
- React TypeScript frontend created
- Spring Boot backend created
- Health check API endpoint added
- PostgreSQL database created
- Backend configured to connect to PostgreSQL
- Database plan documented
- Customer entity created
- Customer repository created
- Customer API endpoints added
- Customer endpoints tested using Thunder Client/Postman
- Product entity created
- Product repository created
- Product API endpoints added
- Low-stock endpoint added
- Product endpoints tested using Thunder Client/Postman

## Local Development

### Frontend

```bash
cd frontend
npm install
npm run dev
```

The frontend should run at:

```text
http://localhost:5173
```

### Backend

```bash
cd backend
.\mvnw.cmd spring-boot:run
```

The backend should run at:

```text
http://localhost:8080
```

### Health Check

Open this URL in your browser:

```text
http://localhost:8080/api/health
```

Expected response:

```text
Order Management API is running
```

## API Endpoints

### Health

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/health` | Checks if the backend is running |

### Customers

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/customers` | Get all customers |
| GET | `/api/customers/{id}` | Get one customer by ID |
| POST | `/api/customers` | Create a new customer |
| DELETE | `/api/customers/{id}` | Delete a customer |

### Products

| Method | Endpoint | Description |
|---|---|---|
| GET | `/api/products` | Get all products |
| GET | `/api/products/{id}` | Get one product by ID |
| POST | `/api/products` | Create a new product |
| DELETE | `/api/products/{id}` | Delete a product |
| GET | `/api/products/low-stock` | Get products where stock is at or below reorder level |

## Project Structure

```text
clothing-order-management-system/
├── frontend/
├── backend/
├── docs/
│   ├── planning/
│   ├── erd/
│   └── screenshots/
└── README.md
```

## Next Steps

- Add supplier management API
- Connect products to suppliers
- Add order creation logic
- Add order line items
- Reduce stock when an order is placed
- Build frontend pages for customers and products
- Add authentication and staff roles
