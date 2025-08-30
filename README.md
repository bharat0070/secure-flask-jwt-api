
# 🔐 Secure Flask JWT API – Best Practices for Authentication

## 📖 Overview
This repository provides a **Flask-based REST API** that implements **secure JWT authentication** following industry best practices.  
It includes:
- **User Registration** with password hashing (bcrypt).
- **Login** with JWT token generation (HS256).
- **Protected Profile Endpoint** requiring valid JWT.
- **Token expiration** for session security.

✅ **Educational Purpose:** Demonstrates how to properly secure APIs using JWT in Python Flask.

---

## ✅ Features
- Secure user authentication with **JWT**.
- Password hashing using **Flask-Bcrypt**.
- Token expiration (30 minutes) for improved security.
- Input validation for basic request checks.
- Simple **in-memory user store** for demonstration.

---

## 🛠 Tech Stack
- **Python 3.x**
- **Flask**
- **Flask-Bcrypt**
- **Flask-JWT-Extended**

---

## 📦 Installation

### 1. Clone the repository
```bash
git clone https://github.com/<your-username>/secure-flask-jwt-api.git
cd secure-flask-jwt-api
