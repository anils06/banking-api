# banking-api

# Mini Banking Full-Stack Application (Java Spring Boot + React/Vite)

This project is a full-stack assessment application developed to demonstrate core banking functionalities, including Account Management (CRUD), Fund Transfers, and JWT Authentication.

## 🚀 Project Structure

The project is divided into two main directories:

1.  `mini-banking-api`: The backend RESTful API built with Java Spring Boot.
2.  `mini-banking-ui`: The frontend user interface built with React and Vite.

## 🛠️ Setup and Running Instructions

For the application to run successfully, both the backend and the frontend must be started concurrently.

### A. Backend Setup (`mini-banking-api`)

| Requirement | Version |
| :--- | :--- |
| Java | JDK 21+ |
| Maven | 3.6+ |
| Database | In-Memory H2 |

1.  **Open in IDE:** Open the `mini-banking-api` directory in your IDE (IntelliJ IDEA recommended).
2.  **Run:** Locate the main class (`MiniBankingApiApplication.java`) and run the application.
3.  **Status Check:** The console should show the message `Tomcat started on port 8080`.

### B. Frontend Setup (`mini-banking-ui`)

| Requirement | Version |
| :--- | :--- |
| Node.js | v16+ |
| npm/Yarn | Latest |

1.  **Navigate:** Open your terminal and change the directory to `mini-banking-ui`.
    ```bash
    cd mini-banking-ui
    ```
2.  **Install Dependencies:** Install all necessary Node modules.
    ```bash
    npm install
    ```
3.  **Start:** Run the application in development mode.
    ```bash
    npm run dev
    ```
4.  **Access:** The application will typically run at `http://localhost:5174`. Open this address in your browser.

## 🔒 API Endpoints and Documentation

All protected endpoints require a valid JWT token obtained from the `/api/users/login` endpoint.

| Area | Method | Endpoint | Description |
| :--- | :--- | :--- | :--- |
| **Auth** | `POST` | `/api/users/register` | Registers a new user. |
| **Auth** | `POST` | `/api/users/login` | Authenticates a user and returns a JWT. |
| **Account** | `POST` | `/api/accounts` | Creates a new account. |
| **Transaction** | `POST` | `/api/transactions/transfer`| Initiates a fund transfer. |
| **History** | `GET` | `/api/transactions/account/{id}`| Retrieves transaction history. |

**API Documentation (Swagger):** Once the backend is running, you can view the complete API documentation and schemas at `http://localhost:8080/swagger-ui/index.html`.
