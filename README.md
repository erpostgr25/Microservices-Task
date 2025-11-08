# Microservices-Task

## Overview
This document provides details on testing various services after running the `docker-compose` file. These services include User, Product, Order, and Gateway Services. Each service has its own endpoints for testing purposes.

---

## Services and Endpoints

### **User Service**
- **Base URL:** `http://localhost:3000`
- **Endpoints:**
  - **List Users:**  
    ```
    curl http://localhost:3000/users
    ```
    Or open in your browser: [http://localhost:3000/users](http://localhost:3000/users)
    <img width="715" height="53" alt="users" src="https://github.com/user-attachments/assets/512a4759-85aa-450c-8c43-8dc2c63684cd" />  

---

### **Product Service**
- **Base URL:** `http://localhost:3001`
- **Endpoints:**
  - **List Products:**  
    ```
    curl http://localhost:3001/products
    ```
    Or open in your browser: [http://localhost:3001/products](http://localhost:3001/products)
    <img width="930" height="62" alt="products" src="https://github.com/user-attachments/assets/8312c46d-8e56-4172-a336-8cad58542971" />


---

### **Order Service**
- **Base URL:** `http://localhost:3002`
- **Endpoints:**
  - **List Orders:**  
    ```
    curl http://localhost:3002/orders
    ```
    Or open in your browser: [http://localhost:3002/orders](http://localhost:3002/orders)  
    <img width="517" height="56" alt="orders" src="https://github.com/user-attachments/assets/c0732b81-991f-40a6-a4d0-f7aca79cf51b" />


---

### **Gateway Service**
- **Base URL:** `http://localhost:3003/api`
- **Endpoints:**
  - **Users:**  
    ```
    curl http://localhost:3003/api/users
    ```
    <img width="557" height="68" alt="gatewayhealth" src="https://github.com/user-attachments/assets/9c82a1b5-8796-46a8-928f-08db024b17bb" />
    <img width="747" height="67" alt="gatewayusers" src="https://github.com/user-attachments/assets/84119b44-f5b7-4c93-b23d-eb44031b3e7b" />


  - **Products:**  
    ```
    curl http://localhost:3003/api/products
    ```
    <img width="902" height="78" alt="gatewayproducts" src="https://github.com/user-attachments/assets/69b0da33-12d1-4c2d-a3cd-d0233a9caddf" />

  - **Orders:**  
    ```
    curl http://localhost:3003/api/orders
    ```
    <img width="563" height="50" alt="gatewayorders" src="https://github.com/user-attachments/assets/f7e020b1-25cb-4db9-8cc3-44d2557e131c" />

---

## Instructions
1. Start all services using the `docker-compose` file:
   ```
   docker-compose up
   ```
2. Once the services are running, use the above endpoints to verify the functionality.
<img width="1848" height="866" alt="docker-compose-up" src="https://github.com/user-attachments/assets/e19b9880-1e72-44e1-9fe1-413ff96a9e25" />
<img width="1858" height="255" alt="docker-compose-up1" src="https://github.com/user-attachments/assets/80a654ac-53aa-486e-b6b4-fab23cfe95be" />
<img width="1763" height="181" alt="docker-compose-ps" src="https://github.com/user-attachments/assets/8025b444-619d-4988-ae1e-7a607b86e02c" />
<img width="758" height="142" alt="docker-compose-network" src="https://github.com/user-attachments/assets/37cdb81b-2edd-4a7f-9f3e-c054e88b6c17" />
<img width="993" height="132" alt="docker-compose-images" src="https://github.com/user-attachments/assets/07facbfd-3738-44e8-95bb-fff1f35f9d1c" />
<img width="1030" height="201" alt="docker-compose-final" src="https://github.com/user-attachments/assets/ab1047f9-43cd-4efb-a5c3-cd4481cc0d0f" />
Happy testing!
