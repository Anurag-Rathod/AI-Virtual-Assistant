# 🤖 AI Virtual Assistant

A full-stack **AI-powered virtual assistant** built with the **MERN stack** and **Google Gemini AI**. allowing users to interact with an intelligent assistant to answer queries, manage information, and receive real-time responses.

## ✨ Features

* 🤖 **Gemini AI Integration** — Generates AI-powered responses using Google Gemini.
* 🎙️ **Voice Interaction** — Supports voice input using the browser's Web Speech API.
* 💬 **Text Interaction** — Allows users to communicate with the assistant through natural-language text queries.
* 🔐 **JWT Authentication** — Implements user authentication and protected API access using JSON Web Tokens.
* 🔒 **Password Hashing** — Passwords are hashed using `bcryptjs` before being stored.
* 👤 **User Management** — Supports user registration, login, authentication, and profile management.
* 🖼️ **Profile Image Upload** — Handles image uploads using Multer and stores them using Cloudinary.
* ⚡ **RESTful APIs** — Express.js APIs handle authentication, user management, and AI-related requests.
* 🗄️ **MongoDB Database** — Stores user and application data using MongoDB and Mongoose.
* 📱 **Responsive UI** — Built with React and Tailwind CSS.
* 🔄 **API Communication** — Axios is used for communication between the React frontend and Express backend.

---

## 🛠️ Tech Stack

### Frontend

* **React.js**
* **JavaScript (ES6+)**
* **React Router**
* **Axios**
* **Tailwind CSS**
* **React Icons**
* **Vite**
* **Web Speech API**

### Backend

* **Node.js**
* **Express.js**
* **REST APIs**
* **MongoDB**
* **Mongoose**
* **JWT**
* **bcryptjs**
* **Multer**
* **Cookie Parser**
* **CORS**
* **dotenv**

### AI & Cloud Services

* **Google Gemini AI**
* **Cloudinary**

### Development Tools

* **Git & GitHub**
* **VS Code**
* **Nodemon**

---

## 🏗️ Application Architecture

```text
                         ┌───────────────────┐
                         │       User        │
                         └─────────┬─────────┘
                                   │
                              Text / Voice
                                   │
                                   ▼
                         ┌───────────────────┐
                         │  React Frontend   │
                         │  React + Tailwind │
                         └─────────┬─────────┘
                                   │
                              Axios / REST
                                   │
                                   ▼
                         ┌───────────────────┐
                         │  Express Backend  │
                         │ Routes / Middleware│
                         │    Controllers    │
                         └───────┬─────┬─────┘
                                 │     │
                    ┌────────────┘     └─────────────┐
                    ▼                                ▼
           ┌─────────────────┐              ┌─────────────────┐
           │    MongoDB      │              │   Gemini AI     │
           │ User / App Data │              │ AI Responses    │
           └─────────────────┘              └─────────────────┘
                    │
                    ▼
           ┌─────────────────┐
           │   Cloudinary    │
           │ Profile Images  │
           └─────────────────┘
```

---

## 📂 Project Structure

```text
AI-Virtual-Assistant/
│
├── Backend/
│   ├── config/
│   ├── controllers/
│   ├── middlewares/
│   ├── models/
│   ├── public/
│   ├── routes/
│   ├── gemini.js
│   ├── index.js
│   ├── .gitignore
│   ├── package.json
│   └── package-lock.json
│
├── Frontend/
│   ├── public/
│   ├── src/
│   ├── .gitignore
│   ├── eslint.config.js
│   ├── index.html
│   ├── package.json
│   ├── package-lock.json
│   └── vite.config.js
│
└── README.md
```

## 🔄 How the Application Works

```text
User
 │
 ├── Register / Login
 │
 ▼
React Frontend
 │
 │ Axios
 ▼
Express REST API
 │
 ├── Authentication
 │     └── JWT + bcryptjs
 │
 ├── User Management
 │     └── MongoDB / Mongoose
 │
 ├── Profile Image
 │     └── Multer → Cloudinary
 │
 └── AI Request
       │
       ▼
   Gemini AI
       │
       ▼
   AI Response
       │
       ▼
 React Frontend
```

### Request Flow

1. User registers or logs into the application.
2. The backend validates the credentials and handles authentication using **JWT**.
3. Passwords are hashed using **bcryptjs** before being stored.
4. The authenticated user interacts with the assistant through text or voice.
5. The React frontend sends requests to the Express backend using **Axios**.
6. The backend processes the request and communicates with **Google Gemini AI**.
7. Gemini generates the AI response.
8. The backend returns the response to the frontend.
9. The response is displayed in the assistant interface.
10. Profile images are uploaded using **Multer** and stored through **Cloudinary**.

---

## 🚀 Future Improvements

* 🔔 AI Productivity Features — Add reminders, task management, and other AI-powered utilities.
* ☁️ Production Deployment — Deploy the application with production-ready infrastructure.
* 🔄 CI/CD Pipeline — Automate testing, builds, and deployment workflows.
