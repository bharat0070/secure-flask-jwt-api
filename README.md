---  
## ✅ ** secure-flask-jwt-api**

```markdown
# Secure Flask JWT API – Best Practices

## 🔍 Overview
This repository contains a **Flask-based API** implementing secure JWT authentication with:
- **Password hashing** using `Flask-Bcrypt`.
- **Token expiration** for session security.
- **Input validation** to prevent injection attacks.

---

## ✅ Features
- User registration and login with **hashed passwords**.
- JWT-based authentication using `Flask-JWT-Extended`.
- Tokens expire after **30 minutes** by default.
- Protected route `/profile` for authenticated users.

---

## 🛠 Tech Stack
- Python 3.x
- Flask
- Flask-Bcrypt
- Flask-JWT-Extended

---

## 📦 Installation
```bash
pip install flask flask-bcrypt flask-jwt-extended

🚀 Running the API

Start the Flask server:

python secure_api.py


The API will run at:

http://127.0.0.1:5000

API Endpoints
1. Register User

POST /register
Example:

{
  "username": "alice",
  "password": "mypassword"
}

2. Login

POST /login
Example:

{
  "username": "alice",
  "password": "mypassword"
}


Response:

{
  "access_token": "<JWT_TOKEN>"
}

3. Profile (Protected)

GET /profile
Header:

Authorization: Bearer <JWT_TOKEN>

🔐 Security Measures Implemented

Strong JWT secret key.

Password hashing using bcrypt.

Token expiration (30 minutes).

Basic input validation.

🚀 Future Improvements

Add refresh tokens.

Enable RS256 for asymmetric signing.

Database integration instead of in-memory storage.

📚 References

Flask-JWT-Extended Docs

OWASP API Security Top 10
