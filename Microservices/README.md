# Kubernetes Microservices Deployment

## Overview
This project demonstrates deployment of a Node.js microservices application on Kubernetes using Minikube.  
The application includes User, Product, Order, and Gateway services.

---

## Minikube Setup

Start Minikube:

```bash
minikube start
```

Verify cluster:

```bash
kubectl get nodes
```

Configure Docker to use Minikube:

```bash
eval $(minikube docker-env)
```

Build Docker images inside Minikube:

Gateway:

http://localhost:3003/api/users

http://localhost:3003/api/products

http://localhost:3003/api/orders

```bash
docker compose build
```

---

## Deployment Steps

Navigate to Kubernetes folder:

```bash
cd k8s
```

Deploy all services:

```bash
kubectl apply -f .
```

---

## Verify Deployment

Check running pods:

```bash
kubectl get pods
```

Check services:

```bash
kubectl get svc
```

---

## Service Testing

### Using Port Forward

Forward gateway service:

```bash
kubectl port-forward svc/gateway-service 3003:3003
```

Test in browser:

- http://localhost:3003/api/users  
- http://localhost:3003/api/products  
- http://localhost:3003/api/orders  

---

### Internal Service Communication

Services communicate using Kubernetes DNS:

- http://user-service:3000  
- http://product-service:3001  
- http://order-service:3002  

---

## Troubleshooting

Check pod status:

```bash
kubectl get pods
```

View logs:

```bash
kubectl logs <pod-name>
```

Describe pod:

```bash
kubectl describe pod <pod-name>
```

Restart pod:

```bash
kubectl delete pod <pod-name>
```

---
(Skill Test - 2 : Completed microservices deployment using Docker and Kubernetes with Minikube)

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

1. Running Pods  
   - Output of: `kubectl get pods`
     <img width="940" height="270" alt="image" src="https://github.com/user-attachments/assets/e7e67535-010b-464a-9224-f0728f3f7b61" />


2. Service Logs  
   - Output of: `kubectl logs <gateway-pod>`
     <img width="940" height="268" alt="image" src="https://github.com/user-attachments/assets/97c6c29d-f319-4e80-80a0-0746debc19d7" />


3. API Testing  
   - Browser results of:
     - /api/users
       <img width="940" height="406" alt="image" src="https://github.com/user-attachments/assets/46d56df5-83a7-46c0-8c34-3438fcbe1ad4" />

     - /api/products
       <img width="882" height="522" alt="image" src="https://github.com/user-attachments/assets/8397c4f7-10f2-4b0e-b997-6efa54d23e51" />

     - /api/orders
       <img width="829" height="264" alt="image" src="https://github.com/user-attachments/assets/aacf1129-2541-489e-930d-6d4e349293a6" />


---

## Conclusion

The microservices application was successfully deployed on Kubernetes using Minikube, with proper service communication and API testing.

