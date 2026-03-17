# Product Inventory Management API using SpringBoot

This project is a simple REST API for managing products built using **Spring Boot**.  
It demonstrates CRUD operations and a layered architecture using **Controller → Service → Repository**.


## How To Run The Project
- Using the follwing command: "./mvnw spring-boot:run"

---

## API EndPoints

- GET /api/products
- Method Name: getAllProducts
- Description: This method is used to get all products from the array list
- URL: http://localhost:8080/api/products

---

- GET /api/products/{id}
- Method Name: getProductById
- Description: This method is used to get a specific product by its ID
- URL Example: http://localhost:8080/api/products/1

---

- POST /api/products
- Method Name: createProduct
- Description: This method is used to create a new product and add it to the list
- URL: http://localhost:8080/api/products

---

- PUT /api/products/{id}
- Method Name: updateProduct
- Description: This method is used to update an existing product using its ID
- URL Example: http://localhost:8080/api/products/1

---

- DELETE /api/products/{id}
- Method Name: deleteProduct
- Description: This method is used to delete a product using its ID
- URL Example: http://localhost:8080/api/products/1

## CURL Examples
- curl.exe -X POST http://localhost:8080/api/products -H "Content-Type: application/json" -d "{\"name\":\"Laptop\",\"category\":\"Electronics\",\"price\":999.99,\"quantity\":10}"
- curl.exe -X GET  http://localhost:8080/api/products 
- curl.exe -X PUT http://localhost:8080/api/products/1 -H "Content-Type: application/json" -d "{\"name\":\"Laptop Pro\",\"category\":\"Electronics\",\"price\":1200.00,\"quantity\":5}"
- curl.exe -X DELETE http://localhost:8080/api/products/1
- curl.exe -X GET  http://localhost:8080/api/products/2 


## Sample Responses
- Create a Product
- curl.exe -X POST http://localhost:8080/api/products -H "Content-Type: application/json" -d "{\"name\":\"Laptop\",\"category\":\"Electronics\",\"price\":999.99,\"quantity\":10}"
{"id":1,"name":"Laptop","category":"Electronics","price":999.99,"quantity":10

- Update a Product
- curl.exe -X PUT http://localhost:8080/api/products/1 -H "Content-Type: application/json" -d "{\"name\":\"Laptop Pro\",\"category\":\"Electronics\",\"price\":1200.00,\"quantity\":5}"
  {"id":2,"name":"Laptop Pro","category":"Electronics","price":1200.0,"quantity":5}

- Delete a Product
- curl.exe -X DELETE http://localhost:8080/api/products/1

- Get all products 
- curl.exe -X GET  http://localhost:8080/api/products [{"id":1,"name":"Laptop","category":"Electronics","price":999.99,"quantity":10}]