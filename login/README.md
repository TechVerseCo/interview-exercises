
### **Exercise: Build an Authentication System with Social Login**

#### **Objective**

Create a Node.js application that provides user authentication using both email/password and social login (Google).

----------

#### **Requirements**

1.  **Endpoints** Implement the following RESTful API endpoints:
    
    -   `POST /auth/register`: Register a new user with an email and password.
    -   `POST /auth/login`: Authenticate a user using email and password.
    -   `GET /auth/google`: Redirect the user to Google for authentication.
    -   `GET /auth/google/callback`: Handle the callback from Google and authenticate the user.
    -   `GET /auth/profile`: Retrieve the authenticated user's profile.
2.  **Data Model** Users should have the following fields:
    
```json
    `{
      "id": "string (UUID)",
      "email": "string (required, unique)",
      "password": "string (hashed, required for email/password registration)",
      "name": "string (optional)",
      "provider": "string (e.g., 'email' or 'google')",
      "googleId": "string (optional, for Google users)",
      "createdAt": "ISO 8601 date string",
      "updatedAt": "ISO 8601 date string"
    }` 
```    
3.  **Authentication**
    
    -   Use **JWT (JSON Web Token)** for authentication and authorization.
    -   Secure endpoints (e.g., `/auth/profile`) require a valid JWT in the `Authorization` header.
4.  **Social Login**
    
    -   Use **Passport.js** with the **Google OAuth 2.0** strategy for social login.
    -   Save the user's Google profile information (e.g., email, name, and Google ID) in the database if they log in for the first time.
5.  **Password Handling**
    
    -   Hash user passwords using **bcrypt** before saving them.
    -   Validate user passwords during login.
6.  **Error Handling**
    
    -   Return appropriate HTTP status codes and error messages for invalid requests (e.g., duplicate registration, invalid credentials, or missing JWT).
7.  **Project Structure**
    
    -   Use a modular structure, separating routes, controllers, middleware, and configuration.
8.  **Bonus Features (Optional)**
    
    -   Implement token refresh functionality with short-lived access tokens and long-lived refresh tokens.
    -   Add a logout endpoint to invalidate JWTs.
    -   Use environment variables to configure sensitive settings (e.g., JWT secret, Google OAuth client ID/secret).
    -   Include unit tests for critical functionality using a testing framework like Jest.

----------

#### **Setup Instructions**

-   Use **MongoDB** (or a similar database) to store user information.
-   Configure Google OAuth 2.0 credentials via the Google Cloud Console.

----------

#### **Deliverables**

-   A GitHub repository or ZIP file containing:
    -   The complete Node.js project.
    -   A `.env.example` file with placeholders for environment variables.
    -   A `README.md` file with:
        -   Instructions to install dependencies.
        -   Steps to set up Google OAuth credentials.
        -   Steps to run the application.
