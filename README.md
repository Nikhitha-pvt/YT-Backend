# 🎬 YT Backend

A robust, scalable backend for a YouTube-like video sharing platform. Built with Node.js and Express, this project supports user authentication, video uploads, comments, likes, playlists, subscriptions, and more.

---

## 🚀 Features

- 🔐 **Authentication & Authorization**
- 📹 **Video Upload & Streaming**
- 💬 **Comments & Replies**
- 👍 **Likes & Dislikes**
- 📃 **Playlists Management**
- 👥 **User Subscriptions**
- ☁️ **Cloudinary Integration for Media Storage**
- 🛡️ **Robust Error Handling & Middleware**

---

## 🏗️ System Architecture

```mermaid
graph TD;
    Client[Client (Frontend)] -->|REST API| Backend[Express.js Backend]
    Backend -->|CRUD| DB[(Database)]
    Backend -->|Media| Cloudinary[Cloudinary]
    Backend -->|Routes| Controllers
    Controllers --> Models
    Controllers --> Middlewares
    Models --> DB
    Middlewares --> Auth[Authentication]
    Middlewares --> Multer[Multer (File Uploads)]
```

---

## 🛠️ Project Structure

```
YT Backend/
├── package.json
├── src/
│   ├── app.js
│   ├── constants.js
│   ├── index.js
│   ├── controllers/
│   ├── db/
│   ├── middlewares/
│   ├── models/
│   ├── routes/
│   └── utils/
```

- **controllers/**: Route logic for each resource
- **db/**: Database connection and config
- **middlewares/**: Auth, file upload, error handling
- **models/**: Mongoose models for all entities
- **routes/**: API endpoints
- **utils/**: Utility classes and helpers

---

## 🧑‍💻 Workflow

1. **User Registration/Login**
   - User signs up/logs in
   - Receives JWT token for authentication
2. **Video Upload**
   - Authenticated user uploads video
   - Video stored in Cloudinary, metadata in DB
3. **Interact with Videos**
   - Users can like/dislike, comment, and add videos to playlists
4. **Subscriptions**
   - Users can subscribe/unsubscribe to other users
5. **Playlists**
   - Create, update, delete playlists
6. **Error Handling**
   - All routes protected with error handling middleware

---

## ⚡️ Quick Start

```bash
# 1. Clone the repo
git clone <repo-url>
cd YT Backend

# 2. Install dependencies
npm install

# 3. Set up environment variables
# Create a .env file based on .env.example

# 4. Run the server
npm start
```

---

## 📝 Environment Variables

Create a `.env` file in the root directory with the following:

```
PORT=5000
MONGODB_URI=your_mongodb_connection_string
JWT_SECRET=your_jwt_secret
CLOUDINARY_CLOUD_NAME=your_cloudinary_cloud_name
CLOUDINARY_API_KEY=your_cloudinary_api_key
CLOUDINARY_API_SECRET=your_cloudinary_api_secret
```

---

## 📦 API Endpoints

- `/api/v1/user` — User registration, login, profile
- `/api/v1/video` — Video upload, fetch, delete
- `/api/v1/comment` — Add, fetch, delete comments
- `/api/v1/like` — Like/dislike videos
- `/api/v1/playlist` — Manage playlists
- `/api/v1/subscription` — Subscribe/unsubscribe users

---

## 🧩 Tech Stack

- **Node.js**
- **Express.js**
- **MongoDB** (Mongoose)
- **Cloudinary** (Media Storage)
- **JWT** (Authentication)
- **Multer** (File Uploads)

---

## 🤝 Contributing

1. Fork the repo
2. Create your feature branch (`git checkout -b feature/feature-name`)
3. Commit your changes (`git commit -m 'Add feature'`)
4. Push to the branch (`git push origin feature/feature-name`)
5. Open a Pull Request

---

## 📄 License

Distributed under the MIT License.

---

## 🙋‍♂️ Contact

For any queries, reach out via Issues or Pull Requests!
