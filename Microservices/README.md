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


## Screenshots
## Testing
a.	User – Service End point – http://localhost:3000/users
<img width="940" height="379" alt="image" src="https://github.com/user-attachments/assets/cbfae737-e601-4b2c-b6b0-005752962de2" />

 b. Product -service - http://localhost:3001/products
 <img width="876" height="535" alt="image" src="https://github.com/user-attachments/assets/008ba1a5-b5d0-481b-995b-2eb34f1a22e2" />

 c. order-service - http://localhost:3002/orders
 <img width="685" height="291" alt="image" src="https://github.com/user-attachments/assets/4a2afda8-d07b-4218-af51-260a5db423cd" />

 

d. Gateway-service:

•	http://localhost:3003/api/users
<img width="717" height="271" alt="image" src="https://github.com/user-attachments/assets/ae239b94-5dd6-4931-87bc-892b6b24b962" />

 
•	http://localhost:3003/api/products
<img width="811" height="265" alt="image" src="https://github.com/user-attachments/assets/8828741a-cfc3-496a-875d-76a8811ea0d8" />

 
•	http://localhost:3003/api/orders
 <img width="657" height="298" alt="image" src="https://github.com/user-attachments/assets/57f724d7-74ca-408b-8402-e6393a62cdc1" />


