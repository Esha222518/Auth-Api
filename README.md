# 🔐 Auth API

A secure and modular **Authentication API** built with **Node.js**, **TypeScript**, **Express**, and **MySQL**. This project provides endpoints for user registration, login, and accessing protected resources using **JWT (JSON Web Tokens)**.

This API demonstrates a solid backend foundation with essential practices like secure password storage using bcrypt, token-based authentication, and TypeScript for type safety.


## 🌟 Features

- ✅ **User Registration** — securely register new users with hashed passwords.
- ✅ **Login with JWT Token** — validate user credentials and return a signed JWT.
- ✅ **Protected Routes** — allow access only to authenticated users via JWT verification middleware.
- ✅ **Error Handling** — clear, consistent error responses.
- ✅ **Modular Folder Structure** — organized into controllers, routes, middleware, and utils.

---

## 🛠️ Technologies Used

| Technology     | Purpose                              |
|----------------|--------------------------------------|
| Node.js        | JavaScript runtime                   |
| Express.js     | Web framework for API handling       |
| TypeScript     | Type safety and maintainability      |
| MySQL          | Relational database                  |
| bcrypt         | Password hashing                     |
| JWT (jsonwebtoken) | Secure token-based authentication |
| dotenv         | Load environment variables           |
| ts-node-dev    | Hot-reloading for TypeScript         |

---

## 📁 Project Structure

auth-api/
├── src/
│ ├── controllers/ # Route handlers (register, login, profile)
│ ├── routes/ # API routes
│ ├── middleware/ # JWT auth middleware
│ ├── models/ # (Optional) For future data models
│ ├── utils/ # Database connection utility
│ └── app.ts # Express app entry point
├── .env # Environment variables (excluded from repo)
├── .gitignore
├── package.json
├── tsconfig.json
└── README.md


---

## 🔌 API Endpoints

| Method | Endpoint             | Description              | Protected |
|--------|----------------------|--------------------------|------------|
| POST   | `/api/auth/register` | Register a new user      | ❌         |
| POST   | `/api/auth/login`    | Login user and get token | ❌         |
| GET    | `/api/auth/profile`  | Get user details         | ✅ (JWT)   |

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/Esha222518/Auth-Api.git
cd Auth-Api
### 2. Install dependencies
```bash
npm install
3. Configure environment
Create a .env file:
env
DB_HOST=localhost
DB_USER=your_mysql_user
DB_PASSWORD=your_mysql_password
DB_NAME=auth_api_db
JWT_SECRET=your_secret_key
PORT=give port number
⚠️ Don't forget to create the auth_api_db database in your MySQL server and add a users table.
4. Start the server
npm run dev

🧪 Testing with Postman
Register a user at POST /api/auth/register

Login at POST /api/auth/login and copy the returned JWT token.

Access the protected route GET /api/auth/profile with Authorization header:
Bearer <your_token_here>
📝 License
This project is licensed under the MIT License.

## 🙋‍♀️ Author
- Name: Esha Jha  
- 📧 Email: [eshajha22@gmail.com](mailto:eshajha22@gmail.com)  
- 🔗 GitHub: [Auth-API Project](https://github.com/Esha222518/Auth-Api)



