# Backend Requirements Specification – Airbnb Clone

---

## 1. User Authentication

### API Endpoints

- POST /api/auth/register
- POST /api/auth/login
- POST /api/auth/logout

### Input Fields

- name
- email
- password

### Validation

- email must be unique
- password min length: 8

### Performance

- Auth response time < 300ms

---

## 2. Property Management

### API Endpoints

- GET /api/properties
- POST /api/properties
- PUT /api/properties/:id
- DELETE /api/properties/:id

### Input Fields

- name
- description
- price
- host_id

### Validation

- price must be > 0
- name required

---

## 3. Booking System

### API Endpoints

- POST /api/bookings
- GET /api/bookings/:id

### Input Fields

- user_id
- property_id
- dates

### Validation

- property must be available
- total_price calculated

---

## Performance

- API responses < 500ms
- System handles 10,000 concurrent users
