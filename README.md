Clothing Store Backend API

📝 Project Overview
This is the backend API for a Clothing Store web application. The API is built using Node.js and Express, with MongoDB as the database. It provides a set of RESTful endpoints for managing user authentication, clothing items, and orders.

The project is designed to be a starting point for developers looking to create a full-featured e-commerce platform. It includes user registration and login, JWT-based authentication, and CRUD operations for managing clothing items in the store.

🌟 Features
User Authentication: Secure user registration and login with JWT-based authentication.
Clothing Management: Full CRUD operations (Create, Read, Update, Delete) for clothing items.
Image Upload: Support for uploading images associated with clothing items.
Role-Based Access: Admin roles for managing the store's inventory.
Database Segregation: Separate databases for user accounts and clothing items to enhance data organization.
🛠 Technologies Used
Node.js: JavaScript runtime for building the API.
Express.js: Web framework for Node.js.
MongoDB: NoSQL database for storing user and clothing data.
Mongoose: ODM (Object Data Modeling) library for MongoDB and Node.js.
JWT (JSON Web Tokens): For secure user authentication and authorization.
Multer: Middleware for handling file uploads.
Dotenv: For managing environment variables.
🚀 Getting Started
Prerequisites
Node.js v22.2.0 or later
MongoDB (local or Atlas)
npm (Node Package Manager)
Installation
Clone the Repository


git clone https://github.com/yourusername/clothing-store-backend.git
cd clothing-store-backend
Install Dependencies


npm install
Set Up Environment Variables

Create a .env file in the root directory and add the following environment variables:

plaintext
Copiar código
MONGO_URL=mongodb+srv://yourusername:yourpassword@cluster0.mongodb.net/
MONGO_DB_ACCOUNTS_NAME=accounts_db
MONGO_DB_CLOTHES_NAME=clothes_db
AUTH_SECRET_KEY=your_jwt_secret_key
PORT=3000
Run the Application

bash
Copiar código
nodemon index.js
The server should be running on http://localhost:3000.

📋 API Endpoints
Here's a brief overview of the available endpoints:

Auth Routes

POST /auth/register: Register a new user.
POST /auth/login: Login a user and return a JWT token.
Clothing Routes

GET /api/clothes: Get all clothing items.
POST /api/clothes: Add a new clothing item (Admin only).
PUT /api/clothes/:id: Update a clothing item by ID (Admin only).
DELETE /api/clothes/:id: Delete a clothing item by ID (Admin only).
User Routes

GET /api/users: Get all users (Admin only).
GET /api/users/:id: Get a single user by ID (Admin only).
DELETE /api/users/:id: Delete a user by ID (Admin only).
🗂 Database Schema
User Schema
json
Copiar código
{
  "username": "string",
  "email": "string",
  "password": "string",
  "role": "string"
}
Clothes Schema
json
Copiar código
{
  "type": "string",
  "color": "string",
  "name": "string",
  "price": "number",
  "stock": "number",
  "description": "string",
  "image": "string"
}
🔐 Authentication
This project uses JWT for securing endpoints. Users need to be authenticated to access certain routes, such as creating or modifying clothing items. Admin users have additional permissions, such as deleting users or managing inventory.

🔧 Environment Variables
MONGO_URL: MongoDB connection string.
MONGO_DB_ACCOUNTS_NAME: Name of the accounts database.
MONGO_DB_CLOTHES_NAME: Name of the clothes database.
AUTH_SECRET_KEY: Secret key used for signing JWTs.
PORT: Port on which the server will run.
🤝 Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

Fork the Project
Create your Feature Branch (git checkout -b feature/yourFeature)
Commit your Changes (git commit -m 'Add some feature')
Push to the Branch (git push origin feature/yourFeature)
Open a Pull Request
📝 License
This project is licensed under the MIT License
