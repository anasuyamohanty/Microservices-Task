# Microservices Docker Assignment

## Overview
This project containerizes four Node.js microservices using Docker and Docker Compose.

## Services
- User Service – Port 3000
- Product Service – Port 3001
- Order Service – Port 3002
- Gateway Service – Port 3003

## Setup Instructions

1. Clone repository:
   git clone <repo-link>

2. Navigate to project:
   cd Microservices

3. Build and run:
   docker compose up --build

## Testing Endpoints

User:
http://localhost:3000/users

Product:
http://localhost:3001/products

Order:
http://localhost:3002/orders

Gateway:
http://localhost:3003/api/users
http://localhost:3003/api/products
http://localhost:3003/api/orders

## Troubleshooting

- If port busy → docker compose down
- If build fails → docker compose build
- If gateway fails → ensure service names used inside gateway code

## Screenshots

(Insert screenshots here)