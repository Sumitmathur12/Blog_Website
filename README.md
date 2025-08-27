# 📝 Blog Website

A full-stack **Blog Management Website** built with **React (Vite, Tailwind CSS, Redux)** on the frontend and **Node.js (Express, MongoDB, Mongoose)** on the backend.  
This platform allows users to create, edit, like, and comment on blog posts with authentication, authorization, and role-based access control.

---

## 🚀 Features
- 🔑 **Authentication & Authorization** (JWT + Role-based: Admin/User)
- 📝 **Blog Management**: Add, edit, delete blogs with categories
- 👍 **Blog Likes** and 💬 **Comments** support
- 🖼️ **Cloudinary** for image storage
- 🔥 **Google Login** integration
- 🎨 **Modern UI** with Tailwind CSS and ShadCN components
- 📊 **Redux State Management**

---

## 🛠️ Tech Stack
### **Frontend (client)**
- React (Vite)
- Redux Toolkit
- Tailwind CSS + ShadCN UI
- Firebase (for Google login)

### **Backend (api)**
- Node.js + Express
- MongoDB + Mongoose
- Cloudinary (media upload)
- Multer (file handling)
- JWT (authentication)

---

## 📂 Folder Structure

### **Backend (api/)**
api/
┣ config/ # Cloudinary & Multer setup
┣ controllers/ # Business logic (Auth, Blog, Comment, User, Category)
┣ helpers/ # Utility helpers (error handling)
┣ middleware/ # Authentication & admin protection
┣ models/ # Mongoose models (Blog, Comment, User, Category, BlogLike)
┣ routes/ # Express routes (Auth, Blog, Comment, User, Category)
┣ index.js # Entry point for Express server
┣ .env.example # Example env vars

markdown
Copy code

### **Frontend (client/)**
client/
┣ public/ # Static assets
┣ src/
┃ ┣ assets/images/ # Logos, icons
┃ ┣ components/ui/ # Reusable UI components (button, card, input, etc.)
┃ ┣ components/ # Feature components (Sidebar, BlogCard, Comments, etc.)
┃ ┣ helpers/ # Helper functions (firebase, env, toast)
┃ ┣ hooks/ # Custom hooks (fetch, mobile detection)
┃ ┣ pages/ # Main pages (Blog, Category, SignIn, SignUp, Profile)
┃ ┣ redux/user/ # Redux state management
┃ ┣ App.jsx # Main App component
┃ ┣ main.jsx # React entry file
┃ ┣ store.js # Redux store
┣ index.html
┣ tailwind.config.js
┣ vite.config.js
┣ .env.example

yaml
Copy code

---

## ⚙️ Setup & Installation

### 1️⃣ Clone the Repository
```bash
git clone https://github.com/Sumitmathur12/Blog_Website.git
cd Blog_Website
2️⃣ Setup Backend
bash
Copy code
cd api
npm install
cp .env.example .env   # configure MongoDB URI, JWT_SECRET, Cloudinary keys
npm run dev
3️⃣ Setup Frontend
bash
Copy code
cd ../client
npm install
cp .env.example .env   # configure Firebase + API URL
npm run dev
Now visit 👉 http://localhost:5173

🔑 Environment Variables
Backend (api/.env)
ini
Copy code
MONGO_URI=your_mongodb_url
JWT_SECRET=your_secret_key
CLOUDINARY_CLOUD_NAME=xxx
CLOUDINARY_API_KEY=xxx
CLOUDINARY_API_SECRET=xxx
Frontend (client/.env)
ini
Copy code
VITE_API_URL=http://localhost:5000
VITE_FIREBASE_API_KEY=xxx
VITE_FIREBASE_AUTH_DOMAIN=xxx
