# 🔐 HBnB – Part 3: Authentication & Database Integration

# Overview 🏗️

This project represents the third stage of the HBnB application. In this part, the backend is enhanced with authentication, authorization, and database integration.
The application transitions from in-memory storage to a persistent database and introduces JWT-based security, making it closer to a real-world production system.

# Key Features 🔹

🔐 JWT Authentication (login & protected routes)
👤 Role-based Authorization (admin vs regular users)
🗄️ Database integration with SQLAlchemy
💾 Persistent storage using SQLite (development)
🔄 Full CRUD operations with database support
🧩 Entity relationships (User, Place, Review, Amenity)

# 📆 Project Structure

This project extends the previous architecture by integrating a database layer and authentication system.
hbnb/
├── app/
│ ├── **init**.py
│ ├── api/
│ │ ├── **init**.py
│ │ └── v1/
│ │ ├── **init**.py
│ │ ├── users.py
│ │ ├── auth.py
│ │ ├── places.py
│ │ ├── reviews.py
│ │ └── amenities.py
│ ├── models/
│ │ ├── **init**.py
│ │ ├── user.py
│ │ ├── place.py
│ │ ├── review.py
│ │ └── amenity.py
│ ├── services/
│ │ ├── **init**.py
│ │ └── facade.py
│ └── persistence/
│ ├── **init**.py
│ ├── repository.py
│ └── database.py
├── config.py
├── requirements.txt
├── run.py
└── README.md

# 🧠 Key Concepts Implemented

✅ JWT authentication using Flask-JWT-Extended
✅ Role-based access control using is_admin
✅ SQLAlchemy ORM integration
✅ SQLite database for development
✅ Transition from in-memory to persistent storage
✅ Proper entity relationships and mappings
✅ Secure password handling using hashing

# ⚙️ Getting Started

# 🔹 Install dependencies

python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# 🔹 Run the application

python run.py
API will be available at:
http://localhost:5000/api/v1/

# 🔐 Authentication

Users must log in to receive a JWT token
Include token in requests:
Authorization: Bearer <your_token>
Protected routes require valid authentication
Some endpoints are restricted to admin users only

# 🗄️ Database

SQLite is used for development
Managed with SQLAlchemy ORM
Designed to support MySQL in production

# 🔧 Technologies Used

Python 3.x
Flask
Flask-RESTx
Flask-JWT-Extended
SQLAlchemy
SQLite
bcrypt

# 📚 References

Flask Documentation
Flask-JWT-Extended Documentation
SQLAlchemy Documentation
SQLite Documentation
Mermaid.js Documentation
