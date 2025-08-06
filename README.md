# Flask REST API - User Management

This is a simple REST API built using **Python Flask** to manage user data with basic **CRUD** operations (Create, Read, Update, Delete).  
The user data is stored in an **in-memory dictionary**, which means it resets every time the server restarts.

## Features

✅ Get all users  
✅ Get a specific user by ID  
✅ Add a new user  
✅ Update existing user  
✅ Delete a user  

## Tech Stack

- Python 3
- Flask
- Postman / Curl (for testing)

##  How to Run This App

### 1. Create a Virtual Environment (Optional but Recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows use: venv\Scripts\activate
```

### 2. Install Dependencies

```bash
pip install flask
```

### 3. Run the Flask App

```bash
python app.py
```

The app will run on:  
`http://127.0.0.1:5000/`

## API Endpoints

### GET `/users`

**Description:** Get all users  
**Example:**  
```bash
curl http://127.0.0.1:5000/users
```

### GET `/users/<id>`

**Description:** Get user by ID  
**Example:**  
```bash
curl http://127.0.0.1:5000/users/1
```

### POST `/users`

**Description:** Add a new user  
**Body (JSON):**
```json
{
  "name": "Charlie",
  "email": "charlie@gmail.com"
}
```

**Example with curl:**
```bash
curl -X POST -H "Content-Type: application/json" \
-d '{"name": "Charlie", "email": "charlie@gmail.com"}' \
http://127.0.0.1:5000/users
```

### PUT `/users/<id>`

**Description:** Update existing user  
**Body (JSON):**
```json
{
  "email": "updated@email.com"
}
```

**Example with curl:**
```bash
curl -X PUT -H "Content-Type: application/json" \
-d '{"email": "updated@email.com"}' \
http://127.0.0.1:5000/users/1
```

### DELETE `/users/<id>`

**Description:** Delete a user  
**Example:**
```bash
curl -X DELETE http://127.0.0.1:5000/users/2
```
