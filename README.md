````markdown
# Blog API & Frontend

This project demonstrates the creation of a simple blog platform using a **RESTful API** and a **frontend interface** built with **Express.js**. It allows users to perform basic CRUD (Create, Read, Update, Delete) operations on blog posts. The backend API is built with Node.js and Express, while the frontend uses EJS templates to render content dynamically.

## Features

- **CRUD Operations**: Create, update, and delete blog posts.
- **View Blog Posts**: The homepage displays a list of all posts with options to edit or delete them.
- **Separation of Concerns**: The API (running on port 4000) handles data management, and the frontend (running on port 3000) renders the content.

## Tech Stack

- **Backend**: Node.js, Express.js, Body-Parser
- **Frontend**: EJS, HTML, CSS
- **Database**: In-memory data store (simple JavaScript array for blog posts)
- **HTTP Requests**: Axios (for API requests from the frontend)

## Installation

1. Clone this repository:

   ```bash
   git clone https://github.com/costa-developer/Blog-API-Project.git
   cd Blog-API-Project
````

2. Install dependencies for both the backend and frontend:

   ```bash
   npm install
   ```

3. Start the server:

   ```bash
   # Start the API server on port 4000
   npm start
   ```

4. Visit the application:

   * The API server will be running at `http://localhost:4000`.
   * The frontend server will be running at `http://localhost:3000`.

## API Endpoints

### `GET /posts`

* **Description**: Get a list of all blog posts.
* **Response**: JSON array of posts.

### `GET /posts/:id`

* **Description**: Get a specific blog post by ID.
* **Response**: JSON object of the post with the given ID.

### `POST /posts`

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

### `PATCH /posts/:id`

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

### `DELETE /posts/:id`

* **Description**: Delete a specific post by ID.
* **Response**: JSON message confirming the deletion.

## Folder Structure

```
/Blog-API-Project
    /views
        - index.ejs        # Homepage (displays all posts)
        - modify.ejs       # New/Edit post form
    /public
        - main.css         # CSS styles
    - index.js             # Backend API logic
    - server.js            # Starts the frontend app and serves EJS views
    - package-lock.json
    - package.json
    - README.md            # Project documentation
```

## Future Improvements

* Implement persistent storage using a database like MongoDB.
* Add user authentication and authorization.
* Implement form validation and error handling on the frontend.
* Improve UI/UX design for a more polished experience.

## License

This project is licensed under the MIT License.


```
