# APP - Backend API

## 1. Project Overview 🚀

A RESTful API built with:

- **Node.js** runtime
- **Express** framework
- **PostgreSQL** database
- **JWT** for authentication

---

## 2. Table of Contents 📑

1. [Project Overview](#1-project-overview)
2. [Table of Contents](#2-table-of-contents)
3. [Installation & Setup](#3-installation--setup)
4. [API Documentation](#4-api-documentation)
5. [Database Setup](#5-database-setup-optional)
6. [Authentication & Security](#6-authentication--security)
7. [Deployment Guide](#7-deployment-guide)
8. [Contributing Guidelines](#8-contributing-guidelines)
9. [License](#9-license)

---

## 3. Installation & Setup ⚙️

### Prerequisites

- Node.js (v18+)
- PostgreSQL (if using database)
- npm

### Quick Start

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/backend-project.git
   cd backend-project
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Start the server:

   ```bash
   node server.js
   ```

---

## 4. API Documentation 📖

### Endpoints

| Method | Endpoint             | Description     |
| ------ | -------------------- | --------------- |
| GET    | `/api/v1/movies`     | Get all users   |
| POST   | `/api/v1/movies`     | Create new user |
| GET    | `/api/v1/movies/:id` | Get single user |

#### Example Request

```http
GET /api/v1/movies/1
```

#### Sample Response

```json
{
  "id": 1,
  "title": "Great movie 1",
  "genre": "Sci-Fi",
  "release_year": 2010,
  "director": "Christopher Nolan",
  "rating": "8.8"
}
```

---

## 5. Database Setup (Optional) 🗄️

### Using PostgreSQL on Render

1. **Set up your PostgreSQL database on Render**:

   - Go to the Render dashboard and create a new PostgreSQL database.
   - Note down the connection string (e.g., `DATABASE_URL`).

2. **Configure environment variables**:

   - Add the `DATABASE_URL` to your `.env` file:
     ```
     DATABASE_URL=postgres://<username>:<password>@<host>:<port>/<database>
     ```

3. **Run migrations**:

   - Use the following command to set up the database schema:
     ```bash
     npm run migrate
     ```

4. **Verify the connection**:
   - Test the database connection by running the application and ensuring the API endpoints interact with the database correctly.

---

---

## 6. Authentication & Security 🔒

### JWT Flow

1. User logs in via `/auth/login`.
2. Server returns a JWT token.
3. Include the token in the `Authorization` header for protected routes.

#### Example Header

```http
Authorization: Bearer <your_token>
```

#### Protected Route Example

```javascript
router.get('/profile', authenticateToken, (req, res) => {
  // Access user data via req.user
})
```

---

## 7. Deployment Guide ☁️

Deploy the application to Render:

1. Create a new web service on Render and connect it to your GitHub repository.

2. Set the required environment variables in the Render dashboard:

   ```
   BASE_URL=http://<your-render-service-url>/api/v1
   ```

3. Render will automatically build and deploy your application after pushing changes to the connected branch.

4. Run migrations on the production database:
   ```bash
   ssh <your-render-service> -- npm run migrate
   ```

---

## 8. Contributing Guidelines 🤝

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes and push to your fork.
4. Submit a pull request.

---

## 9. License 📄

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
