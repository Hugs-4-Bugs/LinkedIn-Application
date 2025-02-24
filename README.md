# 📌 LinkedIn Application  

🚀 **LinkedIn-Application** is a microservices-based project built using **Spring Boot**, replicating key LinkedIn features such as user management, connections, posts, and notifications. It utilizes **Eureka Server** for service discovery and **API Gateway** for seamless communication between services.  

## 📂 Repository Structure  

```
📦 LinkedIn-Application  
 ┣ 📂 api-gateway               # API Gateway for routing requests  
 ┣ 📂 connection-services       # Manages user connections  
 ┣ 📂 eureka-server             # Service Discovery (Eureka)  
 ┣ 📂 notification-services     # Handles notifications  
 ┣ 📂 post-services            # Manages user posts  
 ┣ 📂 user-services            # User management and authentication  
 ┗ 📜 README.md                 # Project Documentation  
```

## ✨ Features  

✔️ **User Management** – Create, update, and manage user profiles  
✔️ **Connection Handling** – Send, accept, and manage connections between users  
✔️ **Posts & Feeds** – Users can create, update, and interact with posts  
✔️ **Notifications** – Real-time notifications for connection requests, likes, and comments  
✔️ **Microservices Architecture** – Scalable and distributed system using Spring Cloud  
✔️ **Service Discovery** – Eureka Server for automatic service registration  
✔️ **API Gateway** – Single entry point for all services  

## 🛠️ Tech Stack  

| Technology  | Description |  
|-------------|------------|  
| **Java 17+**  | Core backend language |  
| **Spring Boot** | Microservices framework |  
| **Spring Cloud Eureka** | Service Discovery |  
| **Spring Cloud Gateway** | API Gateway for request routing |  
| **MySQL / PostgreSQL** | Database for user and post storage |  
| **Kafka / RabbitMQ** | Event-driven communication (future enhancement) |  
| **Docker** | Containerization for deployment |  

## 🔧 Prerequisites  

Ensure you have the following installed:  
- **Java 17+**  
- **Maven**  
- **MySQL or PostgreSQL**  
- **Docker (Optional, for containerized deployment)**  

## 🚀 Installation & Setup  

### 1️⃣ Clone the Repository  

```bash
git clone https://github.com/Hugs-4-Bugs/LinkedIn-Application.git  
cd LinkedIn-Application
```

### 2️⃣ Configure Database  

Update `application.properties` in the respective microservices with your database credentials:  

```properties
spring.datasource.url=jdbc:mysql://localhost:3306/linkedin_db
spring.datasource.username=root
spring.datasource.password=yourpassword
spring.jpa.hibernate.ddl-auto=update
```

### 3️⃣ Build and Run Each Microservice  

Navigate to each service and build:  

```bash
mvn clean install  
mvn spring-boot:run  
```

OR start all services using **Docker Compose** (if configured):  

```bash
docker-compose up --build  
```

## 📡 API Endpoints  

### 🔹 **User Service**  
| Method | Endpoint | Description |  
|--------|---------|-------------|  
| `POST` | `/api/users/register` | Register a new user |  
| `GET` | `/api/users/{id}` | Retrieve user details |  

### 🔹 **Connection Service**  
| Method | Endpoint | Description |  
|--------|---------|-------------|  
| `POST` | `/api/connections/send` | Send a connection request |  
| `GET` | `/api/connections/{userId}` | Get user connections |  

### 🔹 **Post Service**  
| Method | Endpoint | Description |  
|--------|---------|-------------|  
| `POST` | `/api/posts/create` | Create a new post |  
| `GET` | `/api/posts/feed` | Fetch user feed |  

## 📌 Future Enhancements  

- Implement **JWT Authentication** for secure access  
- Add **Kafka-based Event Streaming** for scalable notifications  
- Integrate a **GraphQL API** for efficient data fetching  
- Deploy on **AWS with Kubernetes** for production  

## 🤝 Contribution  

Contributions are welcome! Feel free to submit issues or create pull requests.  

## 📜 License  

This project is licensed under the **MIT License**.  

---

