# Secure Flask JWT API

## Overview
A simple Flask API demonstrating secure JWT authentication with password hashing, token expiry, and input validation.

## Requirements
- Python 3.x
- Install dependencies:
  ```bash
  pip install flask flask-bcrypt flask-jwt-extended
  ```

## Running the API
1. Start the server:
   ```bash
   python secure_api.py
   ```
   The API will run at [http://127.0.0.1:5000](http://127.0.0.1:5000).

## API Endpoints

### Register
- **POST** `/register`
- **Body:**  
  ```json
  {
    "username": "alice",
    "password": "mypassword"
  }
  ```
- **Example (PowerShell):**
  ```powershell
  Invoke-RestMethod -Uri "http://127.0.0.1:5000/register" `
    -Method Post `
    -Body '{"username":"alice","password":"mypassword"}' `
    -ContentType "application/json"
  ```

### Login
- **POST** `/login`
- **Body:**  
  ```json
  {
    "username": "alice",
    "password": "mypassword"
  }
  ```
- **Example (PowerShell):**
  ```powershell
  $response = Invoke-RestMethod -Uri "http://127.0.0.1:5000/login" `
    -Method Post `
    -Body '{"username":"alice","password":"mypassword"}' `
    -ContentType "application/json"
  $response.access_token
  ```

### Profile (Protected)
- **GET** `/profile`
- **Headers:**  
  `Authorization: Bearer <access_token>`
- **Example (PowerShell):**
  ```powershell
  Invoke-RestMethod -Uri "http://127.0.0.1:5000/profile" `
    -Headers @{"Authorization"="Bearer <access_token>"} `
    -Method Get
  ```

## Notes
- Tokens expire after 30 minutes.
- Passwords are securely hashed.
- Input is validated for presence; you can extend validation as needed.
- For RS256 signing, see Flask-JWT-Extended documentation.

## Testing with Postman
1. Register a user via POST `/register`.
2. Login via POST `/login` and copy the `access_token`.
3. Access `/profile` with the `Authorization: Bearer <access_token>` header.

---
