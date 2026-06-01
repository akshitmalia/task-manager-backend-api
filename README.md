# 🚀 Task Manager Backend API

A RESTful Task Manager API built using **Node.js**, **Express.js**, **MongoDB Atlas**, and **Mongoose**.

This project allows users to create, view, update, and delete tasks while storing data in a MongoDB database. Each task contains a name, description, status, and automatically generated timestamps. The API also includes task statistics and proper error handling for invalid requests.

---

## 🌐 Live Demo

### Render Deployment

https://task-manager-backend-api-hojr.onrender.com

### API Base URL

https://task-manager-backend-api-hojr.onrender.com/api/tasks

---

## 📂 GitHub Repository

https://github.com/akshitmalia/task-manager-backend-api

---

## ✨ Features

* ✅ Create Tasks
* ✅ View All Tasks
* ✅ View Task By ID
* ✅ Update Existing Tasks
* ✅ Delete Tasks
* ✅ Task Status Management (Pending / Completed)
* ✅ MongoDB Atlas Integration
* ✅ Automatic Timestamps
* ✅ Statistics Endpoint
* ✅ Error Handling
* ✅ RESTful API Architecture

---

## 🛠️ Tech Stack

### Backend

* Node.js
* Express.js

### Database

* MongoDB Atlas
* Mongoose

### Testing

* Postman

### Deployment

* Render

---

## 📁 Project Structure

```bash
task-manager-api
│
├── config
│   └── db.js
│
├── controllers
│   └── taskController.js
│
├── models
│   └── Task.js
│
├── routes
│   └── taskRoutes.js
│
├── .gitignore
├── package.json
├── package-lock.json
├── server.js
└── README.md
```

---

## 📌 API Endpoints

### 1️⃣ Home Route

**GET**

```http
https://task-manager-backend-api-hojr.onrender.com/
```

Response:

```json
Task Manager API Running
```

---

### 2️⃣ Get All Tasks

**GET**

```http
https://task-manager-backend-api-hojr.onrender.com/api/tasks
```

Returns all tasks stored in the database.

---

### 3️⃣ Get Task Statistics

**GET**

```http
https://task-manager-backend-api-hojr.onrender.com/api/tasks/stats
```

Example Response:

```json
{
  "totalTasks": 6,
  "completedTasks": 2
}
```

---

### 4️⃣ Get Task By ID

**GET**

```http
https://task-manager-backend-api-hojr.onrender.com/api/tasks/:id
```

Example:

```http
https://task-manager-backend-api-hojr.onrender.com/api/tasks/685c123abc456def789ghi
```

---

### 5️⃣ Create New Task

**POST**

```http
https://task-manager-backend-api-hojr.onrender.com/api/tasks
```

Request Body:

```json
{
  "name": "Study DBMS",
  "description": "Revise normalization and SQL joins",
  "status": "pending"
}
```

⚠️ Use Postman or another API client for POST requests.

---

### 6️⃣ Update Existing Task

**PUT**

```http
https://task-manager-backend-api-hojr.onrender.com/api/tasks/:id
```

Request Body:

```json
{
  "status": "completed"
}
```

⚠️ Use Postman or another API client for PUT requests.

---

### 7️⃣ Delete Task

**DELETE**

```http
https://task-manager-backend-api-hojr.onrender.com/api/tasks/:id
```

Example Response:

```json
{
  "message": "Task deleted successfully"
}
```

⚠️ Use Postman or another API client for DELETE requests.

---

## 🧾 Task Schema

```javascript
{
  name: String,
  description: String,
  status: "pending" | "completed",
  createdAt: Date,
  updatedAt: Date
}
```

---

## ⚙️ Installation & Setup

### Clone Repository

```bash
git clone https://github.com/akshitmalia/task-manager-backend-api.git
```

### Navigate To Project

```bash
cd task-manager-backend-api
```

### Install Dependencies

```bash
npm install
```

### Create Environment Variables

Create a `.env` file:

```env
PORT=5000
MONGO_URI=your_mongodb_connection_string
```

### Start Server

```bash
npm run dev
```

---

## 📊 Sample Statistics Response

```json
{
  "totalTasks": 10,
  "completedTasks": 5
}
```

---

## ❌ Error Handling

The API handles common errors such as:

* Invalid Request Data
* Task Not Found
* Database Errors
* Internal Server Errors

Example:

```json
{
  "message": "Task not found"
}
```

---

## 🚀 Deployment

This application is deployed on Render.

Live URL:

https://task-manager-backend-api-hojr.onrender.com

---

## 🔮 Future Improvements

* Authentication & Authorization
* API Key Security
* User Accounts
* Task Categories
* Search & Filtering
* Pagination
* Swagger API Documentation

---

## 👨‍💻 Author

**Akshit Malia**

GitHub:
https://github.com/akshitmalia

---

### Task Submission

This project was developed as part of a Backend Development Task to demonstrate:

* REST API Development
* MongoDB Integration
* CRUD Operations
* Backend Architecture
* Deployment & API Testing
* Error Handling & Validation
