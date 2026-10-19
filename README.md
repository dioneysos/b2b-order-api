# b2b-order-api

A RESTful API for B2B order management built with Java Spring Boot. Supports multi-tenant architecture, role-based access control, and full order lifecycle management.

## Features
- Multi-tenant order management (by company ID)
- Role-based access: Admin / Sales / Buyer
- Order CRUD with status transitions (PENDING → CONFIRMED → SHIPPED → DELIVERED)
- JWT authentication
- Pagination & filtering

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | /api/v1/orders | Create new order |
| GET | /api/v1/orders | List orders (paginated) |
| GET | /api/v1/orders/{id} | Get order detail |
| PATCH | /api/v1/orders/{id}/status | Update order status |
| DELETE | /api/v1/orders/{id} | Cancel order |

## Quick Start
```bash
./mvnw spring-boot:run
# API runs on http://localhost:8080
```

## Tech Stack
- Java 17 + Spring Boot 3.2
- Spring Security + JWT
- PostgreSQL + JPA/Hibernate
- Docker Compose