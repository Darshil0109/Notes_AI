### 📘 AI-Powered Notes App Documentation

#### 🧠 Overview

This **AI-Powered Notes App** is a full-stack web application that empowers users to create, manage, and enhance personal notes using AI. It’s built with a modern stack: **React** for the frontend and **Node.js + Express** for the backend. The integration of **TinyLlama via Ollama** provides intelligent summarization and note enhancement capabilities.

---

### 🚀 Features

| Feature                   | Description                                                       |
| ------------------------- | ----------------------------------------------------------------- |
| ✍️ Create & Edit Notes    | Simple and elegant interface to write or modify notes.            |
| 🧠 AI Summarization       | Auto-generates summaries using TinyLlama for quick understanding. |
| 🔒 Authentication         | Secure login and registration system with session/token handling. |
| ☁️ Persistent Storage     | Notes are saved in a database and persist across sessions.        |


---

### 🛠️ Tech Stack

| Layer      | Technology                                                         |
| ---------- | ------------------------------------------------------------------ |
| Frontend   | React                                               |
| Backend    | Node.js, Express                                                   |
| AI Engine  | TinyLlama via Ollama                                               |
| Storage    | MongoDB                      |


---

### ⚙️ AI Integration (TinyLlama)

**Model Used:** [`TinyLlama` by Ollama](https://ollama.com/library/tinyllama)

The app integrates with the TinyLlama LLM using a local or remote Ollama setup. It's utilized for:

* 🔹 **Generating summaries** from long notes.
* 🔹 **Enhancing note content** with better structure or grammar.
* 🔹 **Providing AI writing suggestions** in real-time or on demand.

Ensure the Ollama server is running locally:

```bash
ollama run tinyllama
```

Backend connects to it via HTTP calls (usually at `http://localhost:11434`).

---

### 🧑‍💻 Getting Started

#### 1. Clone the Repository

```bash
git clone https://github.com/Darshil0109/Notes_AI.git
cd notes-ai-app
```

#### 2. Install Dependencies

```bash
# Frontend
cd ai-notes-client
npm install

# Backend
cd ../server
npm install
```

#### 3. Setup Environment Variables

Create `.env` files in the `server` directory. Add:

```
# server/.env
MONGO_URI=Your_MongoDB_URI
JWT_SECRET=your_secret_key
OPENAI_API_KEY=your_OPENAI_API_KEY
```

#### 4. Run the Application

```bash
# Start backend
cd server
npm start

# Start frontend
cd ../ai-notes-client
npm start
```

---

### 🔐 Authentication Flow

* User registers or logs in.
* A JWT or session cookie is stored.
* All protected routes (like creating/updating notes) are accessible only with valid authentication.

---

### 📦 Folder Structure

```
notes-ai-app/
├── client/               # React frontend
│   ├── components/       # Reusable UI elements
│   ├── pages/            # Route components
│   └── App.jsx
├── server/               # Express backend
│   ├── routes/           # Route handlers (auth, notes)
│   ├── controllers/      # Logic for each route
│   ├── services/         # AI communication logic
│   └── index.js
└── README.md             # Project instructions
```

---

### 📡 API Endpoints

#### 🔐 Auth Routes

| Endpoint           | Method | Description    |
| ------------------ | ------ | -------------- |
| `/api/auth/login`  | POST   | Logs in user   |
| `/api/auth/signup` | POST   | Registers user |

#### 📝 Note Routes

| Endpoint         | Method | Description            |
| ---------------- | ------ | ---------------------- |
| `/api/notes`     | GET    | Get all notes for user |
| `/api/notes`     | POST   | Create a new note      |
| `/api/notes/:id` | PUT    | Update a note          |
| `/api/notes/:id` | DELETE | Delete a note          |

#### 🧠 AI Route

| Endpoint            | Method | Description      |
| ------------------- | ------ | ---------------- |
| `/api/ai/summarize` | POST   | Summarize a note |

---

### 💡 Development Tips

* Use `Postman` or `Thunder Client` to test backend endpoints.
* Add a loading spinner while waiting for AI response to improve UX.
* Debounce search input to improve performance on large note sets.

---

### 🧪 Future Improvements

* 🗂️ Folders & tags for notes organization
* 🖼️ Rich text & image support
* 🔄 Sync with cloud storage (e.g., Google Drive)
* 📱 PWA or mobile app version
* 📊 Note analytics (word count, AI grading, etc.)

---

### 🙌 Credits

* **Frontend & Backend:** Darshil Patel
* **AI Model:** TinyLlama by [Ollama](https://ollama.com)
* **Tools:** React, Node.js, Express , Mongodb


