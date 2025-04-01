# Final Project and Deployment

## Objectives
Build a fully functional web application.
Apply HTML, CSS, and JavaScript concepts learned.
Deploy the project using GitHub Pages, Netlify, or Vercel.

Creating a fully functional web application involves several steps, from planning and building the application to deploying it on a platform like GitHub Pages, Netlify, or Vercel. I'll guide you through the basic steps for building a simple web application and deploying it.

### Step 1: **Plan Your Application**
Let's create a simple **To-Do List Web Application** where users can add tasks, mark them as complete, and remove them. This app will involve HTML for structure, CSS for styling, and JavaScript for functionality.

### Step 2: **Create the Application Files**
We'll create three files:
1. `index.html` - the structure of the page.
2. `styles.css` - the styling of the page.
3. `app.js` - the JavaScript to manage the functionality.

#### `index.html`

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>To-Do List</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>
  <div class="container">
    <h1>My To-Do List</h1>
    <input type="text" id="taskInput" placeholder="Add a new task" />
    <button id="addButton">Add Task</button>

    <ul id="taskList"></ul>
  </div>

  <script src="app.js"></script>
</body>
</html>
```

#### `styles.css`

```css
body {
  font-family: Arial, sans-serif;
  margin: 0;
  padding: 0;
  background-color: #f4f4f9;
}

.container {
  width: 100%;
  max-width: 600px;
  margin: 50px auto;
  padding: 20px;
  background-color: #fff;
  box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
}

h1 {
  text-align: center;
  color: #333;
}

#taskInput {
  width: 80%;
  padding: 10px;
  font-size: 16px;
  margin: 20px 10px 10px;
}

button {
  padding: 10px 20px;
  font-size: 16px;
  cursor: pointer;
  background-color: #4CAF50;
  color: white;
  border: none;
}

button:hover {
  background-color: #45a049;
}

ul {
  list-style-type: none;
  padding: 0;
}

li {
  padding: 10px;
  background-color: #f9f9f9;
  margin: 5px 0;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

li.completed {
  text-decoration: line-through;
  color: gray;
}

button.delete {
  background-color: #f44336;
}

button.delete:hover {
  background-color: #e53935;
}
```

#### `app.js`

```javascript
document.getElementById("addButton").addEventListener("click", function() {
  let taskInput = document.getElementById("taskInput");
  let taskValue = taskInput.value.trim();

  if (taskValue !== "") {
    // Create new list item
    let li = document.createElement("li");

    // Add the task text to the list item
    li.textContent = taskValue;

    // Create a "Complete" button
    let completeButton = document.createElement("button");
    completeButton.textContent = "Complete";
    li.appendChild(completeButton);

    // Create a "Delete" button
    let deleteButton = document.createElement("button");
    deleteButton.textContent = "Delete";
    deleteButton.classList.add("delete");
    li.appendChild(deleteButton);

    // Append the new task to the list
    document.getElementById("taskList").appendChild(li);

    // Clear the input field
    taskInput.value = "";

    // Mark task as completed
    completeButton.addEventListener("click", function() {
      li.classList.toggle("completed");
    });

    // Delete task
    deleteButton.addEventListener("click", function() {
      li.remove();
    });
  }
});
```

### Step 3: **Test the Application Locally**
Before deploying, test the application locally to make sure it works:

1. Create a folder named `todo-app`.
2. Inside this folder, create the three files: `index.html`, `styles.css`, and `app.js`.
3. Open `index.html` in your browser to check if the to-do list works as expected (add tasks, complete them, and delete them).

### Step 4: **Deploy the Web Application**

Now that your app is ready, let's deploy it using **GitHub Pages**, **Netlify**, or **Vercel**. I'll show you how to deploy using **GitHub Pages**.

#### 1. **Create a GitHub Repository**
1. Go to [GitHub](https://github.com/), log in, and create a new repository. Name it something like `todo-app`.
2. Initialize the repository with a README (optional) and push your project to the GitHub repository.

#### 2. **Push the Code to GitHub**
In your terminal, run the following commands to push your project to GitHub:

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/your-username/todo-app.git
git push -u origin main
```

#### 3. **Enable GitHub Pages**
1. Go to your GitHub repository and click on the "Settings" tab.
2. Scroll down to the **GitHub Pages** section.
3. Under **Source**, select the **main branch** and save.
4. GitHub will give you a URL like `https://your-username.github.io/todo-app/`. This is the link to your live application!

### Step 5: **Deploy with Netlify or Vercel (Optional)**

**Netlify** and **Vercel** are other excellent platforms for deploying static sites. Here's how to deploy using either service:

#### Netlify:
1. Go to [Netlify](https://www.netlify.com/) and sign up.
2. Click "New site from Git" and connect your GitHub repository.
3. Follow the steps to deploy your site.

#### Vercel:
1. Go to [Vercel](https://vercel.com/) and sign up.
2. Click "New Project" and import your GitHub repository.
3. Follow the prompts to deploy your site.

### Conclusion:
- **HTML** is used to structure the content (task list, buttons).
- **CSS** is used to style the application (inputs, buttons, task items).
- **JavaScript** is used for functionality (adding, completing, and deleting tasks).
- **GitHub Pages, Netlify, or Vercel** can be used to deploy your app live.

You now have a basic to-do list app deployed and functional! You can continue to enhance this app by adding features like saving tasks in `localStorage`, adding categories, etc.
## Instructions
Choose one of the following project ideas:
Blog Website: Implement a multi-page site with navigation.
Ecommerce Website: Implement a multi-page site with navigation.

>[!NOTE]
> - Include at least:
> - A responsive design.
> - JavaScript interactivity.
> - A deployment link.

## Tasks

Create a well-structured HTML5 document.
Use at least 5 different HTML elements.
Ensure semantic correctness.Sure! Below is an example of a well-structured HTML5 document that uses at least five different HTML elements and ensures semantic correctness:

### Example HTML5 Document:

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>My Awesome Web Page</title>
  <link rel="stylesheet" href="styles.css">
</head>
<body>

  <!-- Header Section -->
  <header>
    <h1>Welcome to My Awesome Web Page</h1>
    <p>Your go-to resource for web development tips and tricks!</p>
  </header>

  <!-- Main Content Section -->
  <main>
    <section>
      <h2>Latest Blog Post</h2>
      <article>
        <h3>Understanding Semantic HTML</h3>
        <p>Semantic HTML helps improve the accessibility and SEO of your website. It provides meaning to the structure of your content.</p>
        <a href="https://example.com" target="_blank">Read more</a>
      </article>
    </section>

    <section>
      <h2>Popular Topics</h2>
      <ul>
        <li><a href="#html">HTML Basics</a></li>
        <li><a href="#css">CSS Styling</a></li>
        <li><a href="#javascript">JavaScript Fundamentals</a></li>
      </ul>
    </section>
  </main>

  <!-- Footer Section -->
  <footer>
    <p>&copy; 2025 My Awesome Web Page. All rights reserved.</p>
  </footer>

</body>
</html>
```

### Explanation of the HTML Elements Used:

1. **`<!DOCTYPE html>`**: Declares the document as HTML5.
2. **`<html lang="en">`**: The root element, defining the document's language as English.
3. **`<head>`**: Contains metadata like the charset, viewport settings, title, and external stylesheets.
4. **`<header>`**: A semantic element used to define introductory content, typically including a title or navigation.
5. **`<h1>`**: A top-level heading to introduce the main topic of the page.
6. **`<p>`**: A paragraph element used to display a brief description.
7. **`<main>`**: Specifies the main content area of the document.
8. **`<section>`**: Used to group related content, like the latest blog post and popular topics.
9. **`<article>`**: Defines an independent section of content (in this case, a blog post) that can stand alone.
10. **`<h2>` and `<h3>`**: Subheadings to organize the content in a hierarchical way.
11. **`<a>`**: Defines a hyperlink for navigation.
12. **`<ul>` and `<li>`**: A list of popular topics, providing navigation links.
13. **`<footer>`**: Defines footer content, often containing copyright information or links.

### Semantic Correctness:
- **`<header>`** is used to group introductory content or navigation links.
- **`<main>`** contains the primary content of the document.
- **`<section>`** groups content into different thematic areas.
- **`<article>`** is used for a self-contained piece of content (like a blog post).
- **`<footer>`** provides footer content, usually at the end of the document or section.

This structure is semantically correct and ensures accessibility and SEO friendliness.


Good luck and happy coding! 🚀💻
