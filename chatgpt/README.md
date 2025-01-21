# **Exercise: Build a ChatGPT-like web app**
## Objective

Create a simple ChatGPT-like web app. The application should allow to chat with a chatbot, allow to view the previous chat sessions.

## Requirements
1.  **Pages and Routing**
- Create a homepage (`/`) that load the chat application.
2.  **Data Management**
- Use a mock JSON file (e.g., `data/chatbot.json`) to store the responses of chatbot.
- Implement functionality to fetch data from the mock file and dynamically display it.
3.  **Features**
- Display simple chat application like ChatGPT on homepage.
- When entering content in chat box, it returns a random response from mock data.
- Can create a new chat session and view the previous chat sessions in the left sidebar like ChatGPT
- Use local state or a temporary in-memory solution to store the content of chat session (no need for backend integration).
4.  **Styling**
- Style the application using CSS modules or a library like Tailwind CSS. Ensure the application has a clean and responsive design.
5.  **Bonus (Optional)**
-   Store the mock data in an API.
-   Use OpenAPI API to get real response from chatbot.

## Deliverables
-   A GitHub repository or a ZIP file containing the complete project.
-   A `README.md` file with:
    -   Instructions on how to run the application locally.
