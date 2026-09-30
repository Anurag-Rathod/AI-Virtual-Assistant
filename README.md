# 🤖 AI Virtual Assistant

A full-stack **AI-powered virtual assistant** built with the **MERN stack** and **Google Gemini AI**. allowing users to interact with an intelligent assistant to answer queries, manage information, and receive real-time responses.

## ✨ Features

- 🤖 **AI-Powered Conversations** — Generates intelligent responses using the Google Gemini API.
- 🎙️ **Voice Interaction** — Supports voice input using the browser's Web Speech API.
- 🔐 **JWT Authentication** — Provides secure user registration, login, and protected API access.
- 🔒 **Password Security** — Hashes user passwords using `bcryptjs` before storing them in the database.
- 👤 **User Management** — Supports user registration, authentication, and profile management.
- 🖼️ **Profile Image Uploads** — Handles image uploads using `Multer` and stores them securely with Cloudinary.
- ⚡ **RESTful APIs** — Provides backend APIs for authentication, user management, and AI interactions.
- 🗄️ **MongoDB Integration** — Stores user and application data using MongoDB and Mongoose.
- 📱 **Responsive UI** — Provides a responsive interface built with React.js and Tailwind CSS.
- 🔄 **API Communication** — Uses Axios for communication between the frontend and backend.

---

## 🛠️ Tech Stack

**Frontend:** React.js, JavaScript (ES6+), Vite, React Router, Tailwind CSS, Axios, React Icons, Web Speech API

**Backend:** Node.js, Express.js, RESTful APIs, Multer, CORS, Cookie Parser, dotenv

**Database:** MongoDB, Mongoose

**Authentication:** JWT, bcryptjs

**AI:** Google Gemini API

**Cloud Storage:** Cloudinary

**Development Tools:** Git, GitHub, VS Code, Nodemon

---

## 🏗️ Application Architecture

    ┌──────────────────────┐
    │         User         │
    └──────────┬───────────┘
               │
               │ Text / Voice Input
               ▼
    ┌──────────────────────┐
    │   React Frontend     │
    │ React + Tailwind CSS │
    └──────────┬───────────┘
               │
               │ Axios / REST API
               ▼
    ┌──────────────────────┐
    │   Express Backend    │
    │ Routes / Middleware  │
    │    Controllers       │
    └───────┬────────┬─────┘
            │        │
            ▼        ▼
    ┌────────────┐  ┌─────────────────┐
    │  MongoDB   │  │  Google Gemini  │
    │ + Mongoose │  │       API       │
    └──────┬─────┘  └─────────────────┘
           │
           ▼
    ┌──────────────────────┐
    │      Cloudinary      │
    │    Profile Images    │
    └──────────────────────┘

---

## 🔄 Application Workflow

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
     │     └── MongoDB + Mongoose
     │
     ├── Profile Image Upload
     │     └── Multer → Cloudinary
     │
     └── AI Interaction
           │
           ▼
      Google Gemini API
           │
           ▼
      AI-Generated Response
           │
           ▼
      React Frontend
           │
           ▼
          User

### Request Flow

1. The user registers or logs into the application.
2. The backend validates the credentials and authenticates the user using JWT.
3. Passwords are securely hashed using `bcryptjs` before being stored.
4. The authenticated user interacts with the assistant through text or voice input.
5. The React frontend sends the request to the Express backend using Axios.
6. The backend processes the request and sends the relevant prompt to the Google Gemini API.
7. Gemini generates the AI-powered response.
8. The backend returns the response to the React frontend.
9. The response is displayed in the assistant interface.
10. Profile images are uploaded using Multer and stored on Cloudinary.

---

## 🚀 Future Improvements

- 🔔 **AI Productivity Features** — Add reminders, task management, scheduling, and other AI-powered utilities.
- 🗣️ **Enhanced Voice Interaction** — Add text-to-speech and improve conversational voice capabilities.
