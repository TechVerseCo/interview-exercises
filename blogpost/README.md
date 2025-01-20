

### **Exercise: Build a Simple Blog Application**

#### **Objective**

Create a simple blog application using Next.js.. The application should display a list of blog posts, allow viewing individual blog post details, and include a form for adding a new blog post.

#### **Requirements**

1.  **Pages and Routing**
-  Create a homepage (`/`) that lists all blog posts.
- Create a dynamic route (`/posts/[id]`) for viewing the details of an individual blog post.
2.  **Data Management**
- Use a mock JSON file (e.g., `data/posts.json`) to store blog posts initially.
- Each blog post should have the following structure:

```json
{
  "id": 1,
  "title": "Blog Title",
  "content": "Blog content goes here...",
  "author": "Author Name",
  "date": "YYYY-MM-DD"
}
```

 - Implement functionality to fetch data from the mock file and dynamically display it.
3.  **Features**
- Display all blog posts on the homepage with the title and author.
-  Clicking on a post's title should navigate to the detailed view (`/posts/[id]`) showing the title, author, date, and full content.
- Add a form (`/add-post`) that allows users to add a new blog post. Validate that all fields are filled before submission.
- Use local state or a temporary in-memory solution to manage the new posts (no need for backend integration).
4.  **Styling**
- Style the application using CSS modules or a library like Tailwind CSS. Ensure the application has a clean and responsive design.
5.  **Bonus (Optional)**
- Implement server-side rendering (SSR) for the homepage.
- Add client-side validation for the form using React state.
- Include pagination on the homepage to limit the number of posts displayed per page.
- Store the data in a mock API using Next.js API routes.

#### **Deliverables**
- A GitHub repository or a ZIP file containing the complete Next.js project.
- A `README.md` file with:
  - Instructions on how to run the application locally.
  - A brief description of the features implemented.
