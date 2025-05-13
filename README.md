---

# Blog API and Frontend

This project demonstrates the creation of a simple blog platform using a **RESTful API** and a **frontend interface** built with **Express.js**. It allows users to perform basic CRUD (Create, Read, Update, Delete) operations on blog posts. The backend API is built in Node.js with Express, while the frontend uses EJS templates to render content dynamically.

## Features

* **Create, Edit, and Delete Blog Posts**: Users can create, update, and delete blog posts.
* **View Blog Posts**: The homepage displays a list of all posts with options to edit or delete them.
* **Separation of Frontend and Backend**: The API (running on port 4000) handles the data, and the server (running on port 3000) serves the frontend.

## Tech Stack

* **Backend**: Node.js, Express.js, Body-Parser
* **Frontend**: EJS, HTML, CSS
* **Database**: In-memory data store (simple JavaScript array for blog posts)
* **HTTP Requests**: Axios (for API requests from frontend)

## Installation

1. Clone this repository:

   ```bash
   git clone  https://github.com/costa-developer/Blog-API-Project.git
   cd Blog-API-Project
   ```

2. Install the dependencies for both backend and frontend:

   ```bash
   # Install dependencies
   npm install
   ```

3. Start the backend server:

   ```bash
   # Start the API server on port 4000
   cd backend
   npm start
   ```

4. Start the frontend server:

   ```bash
   # Start the frontend server on port 3000
   cd frontend
   npm start
   ```

5. Visit the application:

   * API server is running at `http://localhost:4000`
   * Frontend server is running at `http://localhost:3000`

## API Endpoints

### `/posts` (GET)

* **Description**: Get a list of all blog posts.
* **Response**: JSON array of posts.

### `/posts/:id` (GET)

* **Description**: Get a specific blog post by ID.
* **Response**: JSON object of the post with the given ID.

### `/posts` (POST)

* **Description**: Create a new blog post.
* **Request body**:

  ```json
  {
    "title": "Post Title",
    "content": "Post Content",
    "author": "Author Name"
  }
  ```
* **Response**: JSON object of the created post.

### `/posts/:id` (PATCH)

* **Description**: Update a specific post by ID (partial update).
* **Request body**:

  ```json
  {
    "title": "Updated Title",
    "content": "Updated Content",
    "author": "Updated Author"
  }
  ```
* **Response**: JSON object of the updated post.

### `/posts/:id` (DELETE)

* **Description**: Delete a specific post by ID.
* **Response**: JSON message confirming deletion.

## Folder Structure

```
/Blog+API+Project
    - views/
      - index.ejs       # Homepage (displays all posts)
      - modify.ejs      # New/Edit post form
    - public/
      - main.css         # CSS styles
    - index.js          # Backend API code
    - server.js         # Starts frontend app, serves EJS views
    - package-lock.json
    - package.json
  - README.md           # Project documentation
```

## Future Improvements

* Implement persistent storage using a database like MongoDB.
* Add user authentication and authorization.
* Add form validation and error handling on the frontend.
* Improve UI/UX design.

## License

This project is licensed under the MIT License.

---
