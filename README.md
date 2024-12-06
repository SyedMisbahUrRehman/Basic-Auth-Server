#  User Authentication API

This is a basic API for user authentication, developed using **Node.js (Express)** and **MongoDB**. It includes routes for user signup and login, along with a health check and test endpoint.

---

## Features

1. **Health Check**
   - **Endpoint:** `/`
   - **Method:** `GET`
   - **Response:** `"Server is Running!"`
   - **Purpose:** Confirms that the API server is running.

2. **Test Route**
   - **Endpoint:** `/test`
   - **Method:** `GET`
   - **Response:** `"Testing endpoint!"`
   - **Purpose:** Simple route for testing and debugging during development.

3. **User Signup**
   - **Endpoint:** `/signup`
   - **Method:** `POST`
   - **Request Body:**
     ```json
     {
       "username": "your_username",
       "password": "your_password"
     }
     ```
   - **Responses:**
     - `201 Created`: User registered successfully.
     - `400 Bad Request`: Username already taken or invalid input.
     - `500 Internal Server Error`: Database or server error.

4. **User Login**
   - **Endpoint:** `/login`
   - **Method:** `POST`
   - **Request Body:**
     ```json
     {
       "username": "your_username",
       "password": "your_password"
     }
     ```
   - **Responses:**
     - `200 OK`: Login successful.
     - `400 Bad Request`: Invalid credentials or missing input.
     - `500 Internal Server Error`: Database or server error.

---

## Installation

### Prerequisites

- **Node.js** (v14 or higher)
- **MongoDB** (local or cloud instance)
- **NPM** or **Yarn**

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/SyedMisbahUrRehman/Basic-Auth-Server.git
   cd basic-server
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Create a `.env` file in the root directory and add:
   ```env
    MONGO_URI=mongodb://localhost:27017/YOUR-DATABASE_NAME
   PORT=3000
   ```

4. Run the application:
   ```bash
   nodemon index.js
   ```

---

## Usage

1. **Start the server**:
   Run `nodemon index.js` and ensure the server is connected to MongoDB (`MongoDB connected...` will appear in the console).

2. **Test the endpoints** using tools like [Postman](https://www.postman.com/) or [cURL](https://curl.se/).

---


## Dependencies

- **express**: Web framework for Node.js
- **mongoose**: MongoDB object modeling for Node.js
- **dotenv**: For managing environment variables
- **body-parser**: Middleware for parsing JSON requests (built into Express from v4.16.0).

---

Enjoy building your application! 🚀