Here is the fixed version of your `README.md` with properly formatted clickable Table of Contents and consistent section references:

---

# APP - Backend API

## 1. Project Overview

A RESTful API built with:

- **Node.js** runtime
- **Express** framework
- **PostgreSQL** database
- **JWT** for authentication

---

## 2. Table of Contents

1. [Project Overview 🚀](#1-project-overview-🚀)
2. [Table of Contents 📑](#2-table-of-contents)
3. [Installation & Setup ⚙️](#3-installation-and-setup)
   - [Prerequisites](#prerequisites)
   - [Quick Start](#quick-start)
4. [API Documentation 📖](#4-api-documentation)
   - [Endpoints](#endpoints)
   - [Example Request](#example-request)
5. [Database Setup (Optional)](#5-database-setup-optional)
6. [Authentication & Security 🔒](#6-authentication--security)
7. [Deployment Guide 🚀](#7-deployment-guide)
8. [Contributing Guidelines 🤝](#8-contributing-guidelines)
9. [License](#9-license)

---

## 3. Installation and Setup

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

## 4. API Documentation

### Endpoints

| Method | Endpoint           | Description      |
| ------ | ------------------ | ---------------- |
| GET    | /api/v1/movies     | Get all movies   |
| POST   | /api/v1/movies     | Create new movie |
| GET    | /api/v1/movies/:id | Get single movie |
| PUT    | /api/v1/movies/:id | Update a movie   |

### Example Request

Using PostgreSQL on Render:

1. Set up your PostgreSQL database on Render.
2. Go to the Render dashboard and create a new PostgreSQL database.
3. Copy the database connection string.
4. Configure database connection:
   Replace the existing values in `db.js` with your Render PostgreSQL credentials.
5. No migrations needed:
   Tables are created automatically by Sequelize. Just ensure the database connection is correct.
6. Verify the connection:
   Start your server and test API endpoints to ensure the database is working.

---

## 5. Database Setup (Optional)

Follow the steps in the [Example Request](#example-request) section to configure your database.

---

## 6. Authentication & Security

- JWT-based authentication (setup in backend).
- Secure your `.env` file and database credentials.
- Always validate inputs on the frontend and backend.

---

## 7. Deployment Guide

1. Push your code to GitHub.
2. Deploy your backend on Render or any other Node.js-supported platform.
3. Add your environment variables (e.g., `DATABASE_URL`) to the Render dashboard.

---

## 8. Contributing Guidelines

1. Fork the repository.
2. Create a new branch:

   ```bash
   git checkout -b feature/feature-name
   ```

3. Commit your changes:

   ```bash
   git commit -m "Added feature"
   ```

4. Push to your branch:

   ```bash
   git push origin feature/feature-name
   ```

5. Open a pull request.

---

## 9. License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---
