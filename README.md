# Basic Server Setup with User Management

This repository provides a basic server setup with user management functionality. It includes features such as user registration, login, logout, and middleware for authentication. The server is built using Node.js and Express, and it interacts with a MongoDB database.

## Functionality

- **User Management**
  - **Register:** Allows users to create a new account.
  - **Login:** Authenticates users and provides a JWT token for session management.
  - **Logout:** Logs users out by invalidating their session token.

- **Middleware**
  - **Authentication Middleware:** Protects routes by ensuring that requests are made by authenticated users.

## Routes

### User Routes

- **POST /register**
  - **Description:** Register a new user.
  - **Request Body:**
    ```json
    {
      "name": "John Doe",
      "username": "johndoe",
      "email": "johndoe@example.com",
      "password": "password123"
    }
    ```
  - **Response:** `{ "message": "User registered successfully" }`

- **POST /login**
  - **Description:** Authenticate a user and provide a JWT token.
  - **Request Body:**
    ```json
    {
      "email": "johndoe@example.com",
      "password": "password123"
    }
    ```
  - **Response:** `{ "token": "JWT_TOKEN", "user": { "username": "johndoe", "email": "johndoe@example.com" } }`

- **POST /logout**
  - **Description:** Log out a user and invalidate their session token.
  - **Request Body:**
    ```json
    {
      "email": "johndoe@example.com"
    }
    ```
  - **Response:** `{ "message": "User successfully logged out" }`

### Post Routes (Future Implementation)

- **POST /posts**: Create a new blog post.
- **GET /posts**: Fetch all blog posts.
- **GET /posts/:id**: Fetch a blog post by ID.
- **PUT /posts/:id**: Update a blog post by ID.
- **DELETE /posts/:id**: Delete a blog post by ID.

## Packages Used

- **express:** Web framework for Node.js.
- **mongoose:** MongoDB object modeling tool.
- **bcryptjs:** Library for hashing passwords.
- **jsonwebtoken:** Library for creating and verifying JWT tokens.
- **dotenv:** Loads environment variables from a `.env` file.

## How to Use

1. **Clone the Repository:**

   ```bash
   git clone https://github.com/your-username/repo-name.git
   cd repo-name
