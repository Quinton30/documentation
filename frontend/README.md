# Web - Frontend

## 1. Project Overview 🚀

A modern web application built with:

- **HTML5** for structure
- **Tailwind CSS** (via CDN) for styling
- **Vanilla JavaScript** for interactivity

No frameworks, build tools, or dependencies required!

---

## 2. Table of Contents 📑

1. [Project Overview](#1-project-overview-🚀)
2. [Table of Contents](#2-table-of-contents-📑)
3. [Installation & Setup](#3-installation--setup-⚙️)
4. [Usage Instructions](#4-usage-instructions-🖥️)
5. [API Integration (Optional)](#5-api-integration-optional-🔌)
6. [Contributing Guidelines](#6-contributing-guidelines-🤝)
7. [License](#7-license-📄)

---

## 3. Installation & Setup ⚙️

### Requirements

- Web browser (Chrome/Firefox/Safari)
- Git (optional, for cloning)

### Steps

1. Clone the repository:
   ```bash
   git clone https://github.com/Quinton30/web
   ```
2. Navigate to the project folder:
   ```bash
   cd frontend
   ```
3. Open `index.html` in your browser (use a live server extension).

**Note:** Tailwind CSS is loaded via CDN in the HTML file:

```html
<script src="https://cdn.tailwindcss.com"></script>
```

---

## 4. Usage Instructions 🖥️

### Overview

This web application connects to the backend API at `http://localhost:3000/api/v1/movies` to manage movie records. It includes features to add, view, and update movies through an intuitive, mobile-responsive interface.

### Key Features

- ✅ **Dynamic Form Validation**  
  All forms validate user input to prevent incomplete or invalid data submissions.

- 🖥️ **Real-Time Data Interaction**  
  Instantly fetches, displays, and updates movie data through API calls.

### Pages & Usage

#### 1. Add Movie — `postMovie.html`

Add a new movie to the database.

1. Fill out all the form fields:

   - **Title**
   - **Genre**
   - **Release Year**
   - **Director**
   - **Rating**

2. Click **Submit** to add the movie.

- A toast notification will confirm if the movie was added successfully.
- Errors like missing fields or invalid formats will also be shown via toast.

#### 2. View Movies — `getMovies.html`

View the list of all movies in the database.

- When the page loads, it automatically fetches all movie records from the API.
- Movies are displayed in a responsive, user-friendly table format.
- Use this page to verify if additions or updates have been applied successfully.

#### 3. Edit Movie — `putMovie.html`

Update details of an existing movie.

1. Enter the **Movie ID** and click **Fetch Movie**.

   - If the movie exists, the form auto-populates with its current details.

2. Edit any of the available fields:

   - **Title**
   - **Genre**
   - **Release Year**
   - **Director**
   - **Rating**

3. Click **Submit** to update the record.

- You'll get a success or error toast notification based on the operation.


## 5. API Integration

If your app connects to an API:

- **Base URL:** `http://localhost:3000/api/v1/movies`

### Example Request

```javascript
// Fetch data from an endpoint
fetch('http://localhost:3000/api/v1/movies')
  .then((response) => response.json())
  .then((data) => {
    // Update the DOM here
    document.getElementById('result').innerHTML = data.message
  })
  .catch((error) => console.error('Error:', error))
```

---

## 6. Contributing Guidelines 🤝

1. Fork the repository.
2. Create a branch:
   ```bash
   git checkout -b feature
   ```
3. Follow coding standards:
   - Use semantic HTML.
   - Avoid inline styles (use Tailwind classes).
   - Comment complex JavaScript logic.
4. Commit changes and open a Pull Request.

---

## 7. License 📄

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
