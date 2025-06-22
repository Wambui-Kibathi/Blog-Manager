# Blog Manager

Blog Manager is a single-page application that allows users to view, add, edit, and delete blog posts dynamically. It features a responsive layout, persistent data storage via a local JSON server, and a user-friendly interface for managing blog content.

# Features
- View Posts: Display a list of all blog posts, sorted by newest first.
- Post Details: Click on a post title to view its full content, author, date, and associated image. The first post's details are displayed by default on page load.
- Add New Posts: A form is provided to create new blog posts, including title, author, image URL, and content. New posts are automatically added to the list and persisted.
- Edit Existing Posts: Edit the title and content of any existing post through a dedicated form. Changes are reflected immediately and persisted.
- Delete Posts: Easily remove posts from the list, with changes persisted to the backend.
- Image Support: Posts can include an image via a URL, which is displayed in the post detail view.

# Technologies Used
HTML5: For the structure and content of the web page.
CSS3: For styling and responsive layout.
JavaScript (ES6+): For all dynamic functionality and interaction with the API.
JSON Server: A fake REST API for local development, providing a backend (db.json) for data persistence.

# Installation and Setup
1. To run this project locally, follow these steps:
```bash
git clone https://github.com/your-username/Blog-Manager.git
cd Blog-Manager
```
(Replace your-username with your actual GitHub username.)
2. Install JSON Server: If you don't have it globally, you'll need to install json-server.
```bash
npm install -g json-server
```
(If you don't have Node.js and npm, you'll need to install them first from nodejs.org)
3. Prepare your db.json file:
Create a file named db.json in the root of your project directory with your initial blog post data. For example:
```JSON
{
  "posts": [
    {
      "id": 1,
      "title": "We Need More Black Artists In Alternative Rock",
      "content": "A deep dive into the representation of Black artists in the alternative rock scene...",
      "author": "Wambui W.",
      "date": "2024-01-10",
      "avatar": "https://via.placeholder.com/600x400/87CEEB/000000?text=Black+Artists"
    },
    {
      "id": 2,
      "title": "A Journey Through Code",
      "content": "Exploring the vast world of programming one line at a time...",
      "author": "Octavio S.",
      "date": "2024-02-20",
      "avatar": "https://via.placeholder.com/600x400/98FB98/000000?text=Code+Journey"
    }
  ]
}
```
4. Start JSON Server
Open a terminal in your project root directory and run:
```bash
json-server --watch db.json
```
This will start the API server, typically on http://localhost:3000/. Your posts will be available at http://localhost:3000/posts.
5. Open the application in your browser. You can do that through a live server via VS Code.

# Usage
Once the JSON Server and your application are running:
1. View Posts: The left panel will display a list of all posts. Click any post title to see its full details on the right.
2. Add New Post: Use the "Add New Post" form on the right panel. Fill in the details and click "Add Post". The new post will appear in the list and be saved to db.json.
3. Edit Post: Select a post to view its details. Click the "Edit" button below the post. An edit form will appear, pre-filled with the post's current title and content. Make your changes and click "Update Post".
4. Delete Post: Select a post to view its details. Click the "Delete" button below the post. Confirm the deletion, and the post will be removed from the list and db.json.

# Project Structure
Blog-Manager/
├── index.html
├── css/
│   └── style.css
├── src/
│   └── index.js
└── db.json

# Contributing
Pull requests are welcome. For major changes or new features, please open an issue first to discuss what you would like to change.
Please make sure to update relevant parts of the code and documentation as appropriate.

# Author
Wambui Kibathi

# License
This project is licensed under the MIT License.
Copyright (c) 2025 Wambui-Kibathi

