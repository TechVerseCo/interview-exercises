### **Exercise: Build a Notes Management System**

#### **Objective**

Create a simple backend for managing notes using Node.js. The application should allow users to perform CRUD operations on notes and include basic validation and error handling.

----------

#### **Requirements**

1.  **Endpoints** Implement the following RESTful API endpoints:
    
    -   `GET /notes`: Retrieve a list of all notes.
    -   `GET /notes/:id`: Retrieve a single note by its ID.
    -   `POST /notes`: Create a new note.
    -   `PUT /notes/:id`: Update an existing note by its ID.
    -   `DELETE /notes/:id`: Delete a note by its ID.
2.  **Data Model** Notes should have the following fields:
    
```json
{
  "id": "string (UUID)",
  "title": "string (required)",
  "content": "string (optional)",
  "createdAt": "ISO 8601 date string",
  "updatedAt": "ISO 8601 date string"
}` 
```

3.  **Features**
    
    -   Validate that the `title` field is not empty when creating or updating a note.
    -   Automatically generate `id`, `createdAt`, and `updatedAt` fields on creation.
    -   Update the `updatedAt` field whenever a note is modified.
4.  **Error Handling**
    
    -   Return appropriate HTTP status codes (e.g., `400` for bad requests, `404` for not found).
    -   Include meaningful error messages in the response body.
5.  **Middleware**
    
    -   Use middleware for logging each request (method, URL, status code, and response time).
    -   Implement a middleware for centralized error handling.
6.  **Storage**
    
    -   Use an in-memory array for storing notes during development (no database required).
    -   Bonus: Allow switching to a file-based JSON storage system.
7.  **Testing**
    
    -   Provide at least 3 test cases using a testing framework (e.g., Jest) to verify key functionality.
8.  **Project Structure**
    
    -   Follow a modular file structure (e.g., separate routes, controllers, and middleware).
9.  **Bonus Features (Optional)**
    
    -   Add filtering and searching for notes (e.g., by title or creation date) using query parameters (`GET /notes?title=example`).
    -   Add pagination to the `GET /notes` endpoint.
    -   Use environment variables for configurable settings (e.g., port number) using `dotenv`.

----------

#### **Deliverables**

-   A GitHub repository or ZIP file containing:
    -   Complete Node.js project files.
    -   A `README.md` file with:
        -   Instructions to install dependencies.
        -   Steps to run the application and any tests.
