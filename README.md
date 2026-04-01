# JWT Authentication Demo (Spring Boot)

## 📌 Overview
This project is a **RESTful API** built using **Spring Boot** that implements secure communication using **JSON Web Tokens (JWT)**. It follows a clean, layered architecture to manage user authentication and student data management.

## 🏗️ Project Structure
The project is organized into functional packages under `src/main/java/com.AML2A.JWT_DEMO`:

* **`controller`**: Contains `AuthController.java` and others to handle incoming HTTP requests.
* **`service`**: Implements the business logic.
* **`repository`**: Interfaces for database operations (e.g., `StudentRepository.java`).
* **`model`**: Defines the data entities (e.g., `Student.java`).
* **`security`**: Contains security configurations like `SecurityConfig.java`.
* **`config`**: General application configuration classes.
* **`service`**: Helper classes, including `JwtUtil.java` for token generation and validation.
* **`JwtDemoApplication.java`**: The main entry point of the Spring Boot application.

## 🚀 Technologies Used
* **Java 17**
* **Spring Boot 3.x**
* **Spring Security** (JWT Implementation)
* **Spring Data JPA**
* **Maven**
* **Eclipse IDE / Spring Tool Suite**

## ⚙️ How to Run the Project
1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/JWT-DEMO.git
   ```
2. **Navigate to the project directory**
   ```bash
   cd JWT-DEMO
   ```
3. **Run the application**
   * **Using Maven:**
     ```bash
     mvn spring-boot:run
     ```
   * **Using IDE:** Right-click `JwtDemoApplication.java` > **Run As** > **Spring Boot App**.

## 🌐 API Endpoints
| Method | Endpoint | Description | Auth Required |
| :--- | :--- | :--- | :--- |
| **POST** | `/auth/login` | Authenticate user & receive JWT | No |
| **GET** | `/api/students` | Fetch all students | **Yes** |
| **POST** | `/api/students` | Add a new student | **Yes** |
| **PUT** | `/api/students/{id}` | Update student details | **Yes** |
| **DELETE** | `/api/students/{id}` | Remove a student | **Yes** |

## 🧪 Testing the API
1.  **Generate Token:** Send a POST request to the login endpoint with valid credentials.
2.  **Access Protected Routes:** Include the received token in the header of your requests:
    `Authorization: Bearer <your_token_here>`
3.  **Tools:** Recommended to use **Postman** or **cURL** for testing header-based authentication.

## IMPLEMENTATION

<img width="1557" height="368" alt="Screenshot 2026-03-31 120328" src="https://github.com/user-attachments/assets/10fcdcf2-7332-4d6f-be8c-2b01c5370ddb" />

## API CALLS (POSTMAN)

<img width="1091" height="980" alt="Screenshot 2026-03-31 120226" src="https://github.com/user-attachments/assets/9afc0c0a-f3e8-4138-a59d-476f297b4915" />

<img width="1101" height="967" alt="Screenshot 2026-03-31 120236" src="https://github.com/user-attachments/assets/282f6a52-33ea-4602-8aee-fa4060a1e66d" />


## 📂 Build
To package the project into a JAR file:
```bash
mvn clean install
```

## ⚠️ Notes
* **Port:** Default is `8080`. Ensure it is not occupied.
* **Security:** Ensure the secret key in `JwtUtil.java` is kept secure in a production environment.
* **Database:** Check `src/main/resources/application.properties` for H2 or MySQL configurations.

## 📄 License
This project is for educational purposes.
