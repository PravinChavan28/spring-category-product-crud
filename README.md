# 🛠️ Category-Product CRUD API

This is a Spring Boot RESTful API application for managing **Categories** and their associated **Products**. It supports full **CRUD operations**, implements a **one-to-many relationship**, and includes **server-side pagination**.

---

## 🚀 Features

- CRUD for **Categories**
- CRUD for **Products**
- One-to-many relationship: One **Category** → Many **Products**
- Server-side pagination for both Categories and Products
- Product detail response includes Category information
- Swagger UI / Postman testing support

---

## 📦 Technologies Used

- Java 17
- Spring Boot
- Spring Data JPA
- Hibernate
- MySQL or H2 (you can switch)
- Maven
- Lombok
- Postman for testing

---

## 📁 Project Structure

```
src/
├── controller/
│   ├── CategoryController.java
│   └── ProductController.java
├── entity/
│   ├── Category.java
│   └── Product.java
├── repository/
    ├── CategoryRepository.java
    └── ProductRepository.java
---

## 🌐 API Endpoints

### 📂 Category CRUD

| Method | Endpoint                        | Description                  |
|--------|----------------------------------|------------------------------|
| GET    | `/api/categories?page=0`        | Get all categories (paginated) |
| GET    | `/api/categories/{id}`          | Get category by ID           |
| POST   | `/api/categories`               | Create a new category        |
| PUT    | `/api/categories/{id}`          | Update category by ID        |
| DELETE | `/api/categories/{id}`          | Delete category by ID        |

### 📂 Product CRUD

| Method | Endpoint                        | Description                  |
|--------|----------------------------------|------------------------------|
| GET    | `/api/products?page=0`          | Get all products (paginated) |
| GET    | `/api/products/{id}`            | Get product by ID (with category details) |
| POST   | `/api/products`                 | Create a new product         |
| PUT    | `/api/products/{id}`            | Update product by ID         |
| DELETE | `/api/products/{id}`            | Delete product by ID         |

---

## 🧪 How to Test Using Postman

### ✅ Create Category
**POST** `/api/categories`

```json
{
  "name": "Fertilizers"
}
```

### ✅ Create Product
**POST** `/api/products`

```json
{
  "name": "Urea",
  "description": "Nitrogen-based",
  "price": 400.0,
  "category": {
    "id": 1
  }
}
```

### ✅ Get Product with Category
**GET** `/api/products/1`

---

## ⚙️ Running the Application

### Step 1: Clone & Navigate

```bash
git clone https://github.com/yourusername/category-product-crud.git
cd category-product-crud
```

### Step 2: Configure DB (MySQL or H2)

Edit `application.properties` or `application.yml`:

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/testdb
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### Step 3: Run

```bash
./mvnw spring-boot:run
```



## 🙌 Author

**Pravin Chavan**  
Email: pravinchavan2828@gmail.com  
Location: Pune, Maharashtra  
GitHub: [@yourgithub](https://github.com/yourgithub)

---

## 📎 Optional

- 📄 Swagger UI: `http://localhost:8080/swagger-ui/index.html`
- 📬 Postman Collection: [Click here](link-to-your-postman-collection-if-any)

