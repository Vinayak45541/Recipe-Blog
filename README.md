# 🍔 Full-Stack Recipe Blog Platform

A modern, full-stack Web Application built using the **MERN** stack (MongoDB, Express, React, Node.js). This platform bridges the gap between culinary creators and food enthusiasts. It allows recipe creators to share their culinary masterpieces and enables an audience to easily browse, favourite, and follow their favourite chefs.

---

## 🎯 Objective

The core objective of this project is to provide an interactive, scalable platform equipped with two distinct environments:
- **Creator Dashboard**: A focused workspace for chefs/enthusiasts to write, upload, manage and track their recipes.
- **Audience Feed**: A social-media-style feed for users to explore recipes, favourite the ones they love, and follow creators.

By separating these workflows and roles, the application provides a customized experience tailored to both the producer and the consumer of the content.

---

## ⚙️ Working & Features

### 👨‍🍳 For Creators:
- **Recipe Management**: Create (with Image Upload), Read, Update, and Delete (CRUD) personal recipes.
- **Audience Engagement**: View the list of followers who subscribe to their content.
- **Secure Access**: Protected dashboard specific to their authoring role.

### 👥 For Audiences:
- **Exploration**: Browse all global recipes uploaded to the platform.
- **Interactions**: Mark favourite recipes making them easily accessible later.
- **Social Following**: Visit Creator profiles and follow them for more content.

### 🔒 General Built-in Features:
- **Authentication & Security**: Secure user registration and login using encrypted passwords and JWT (JSON Web Tokens).
- **Responsive Layout**: Designed to be fully accessible on desktops, tablets, and mobile devices.
- **Role-based Authentication**: Differentiates logic dynamically between a viewer and an author.

---

## 🏗️ Project Architecture

This is a classic Single Page Application (SPA) utilizing a RESTful architecture pattern.

1. **Client-Side (Frontend)**: React handles the UI view layer and routing, fetching data asynchronously using Axios.
2. **Server-Side (Backend)**: An Express server coordinates API routes, applies middleware for auth and file processing (Multer), and communicates with the Database.
3. **Database Layer (MongoDB)**: Data persistence layer storing Users, Recipes, Follower mappings, and Favourites via Mongoose Schemas.

---

## 💻 Tech Stack

### Frontend
- **Framework**: React 18
- **Tooling**: Vite (Lightning fast HMR and optimized builds)
- **Routing**: React Router DOM (v6)
- **Styling**: Vanilla CSS / SCSS
- **HTTP Client**: Axios
- **Iconography**: React Icons

### Backend
- **Runtime Environment**: Node.js
- **Server Framework**: Express.js
- **Database Modeler**: Mongoose

### Security & Utilities
- **Authentication**: JsonWebToken (JWT)
- **Hash Function**: Bcrypt
- **File Uploads**: Multer (Local disk storage image caching)
- **Environment Management**: dotenv
- **Cross-Origin Logic**: CORS

---

## 📂 Folder Structure

The project maintains a clean separation of concerns:

```text
Recipe-Blog-main/
│
├── backend/                  # Node.js Server Environment
│   ├── config/               # Database connection configs (MongoDB)
│   ├── controller/           # Business logic (recipe.js, user.js)
│   ├── middleware/           # Custom middleware (auth validations)
│   ├── models/               # Mongoose Schema Definitions
│   ├── public/               # Uploaded static assets (recipe images)
│   ├── routes/               # Express API endpoints mapping
│   ├── server.js             # Server Application Entry Point
│   └── package.json          # Backend Dependencies
│
├── frontend/                 # React UI Environment
│   ├── public/               # Static base templates
│   ├── src/                  
│   │   ├── assets/           # Client-side static assets
│   │   ├── components/       # Reusable UI React Components
│   │   ├── pages/            # Page layouts / Routes 
│   │   ├── App.jsx           # Main React component tree
│   │   ├── main.jsx          # React DOM mounting point
│   │   └── App.css / index.css # Global Styles
│   ├── vite.config.js        # Vite bundler configurations
│   └── package.json          # Frontend Dependencies
│
└── README.md                 # Project Documentation
```

---

## 🚀 Installation & Local Setup

Run this project locally in your own environment by following these steps:

### Prerequisites
- [Node.js](https://nodejs.org/en/) installed on your local machine.
- A running instance of [MongoDB](https://www.mongodb.com/try/download/community) (Local or Atlas URI).

### 1. Clone the Repository
```bash
git clone https://github.com/Vinayak45541/Recipe-Blog.git
cd Recipe-Blog-main
```

### 2. Backend Setup
Open a terminal and navigate to the backend directory:
```bash
cd backend
npm install
```

Create a `.env` file inside the `backend` folder and configure the following variables:
```env
PORT=3000
SECRET_KEY=your_super_secret_jwt_key
# MONGO_URI=your_mongodb_connection_string (ensure your config/connectionDb matches your database path)
```

Start the backend server:
```bash
npm run dev
# The server will start on http://localhost:3000
```

### 3. Frontend Setup
Open a **new separate terminal window** and navigate to the frontend directory:
```bash
cd frontend
npm install
```

Start the React development server:
```bash
npm run dev
# The frontend will be served typically on http://localhost:5173 
```

Visit the frontend URL in your browser and start exploring the Recipe Blog!
