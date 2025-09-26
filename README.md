# Social Media API

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](#)  
[![Build Status](https://img.shields.io/badge/build-passing-brightgreen.svg)](#)

A **RESTful API** built for social media applications.  
This project provides endpoints for **user authentication, posts, comments, likes, and more**, making it a solid foundation for any social media platform.

---

## 🚀 Features

- User registration & login (JWT authentication)  
- Create, read, update, and delete (CRUD) posts  
- Commenting and replies on posts  
- Like/unlike functionality  
- Basic analytics (post counts, likes, comments)  
- Secure authentication and authorization  
- Scalable architecture with modular code structure  

---

## 🛠 Tech Stack

- **Backend:** Node.js, Express  
- **Database:** MongoDB / PostgreSQL (update based on your project)  
- **Authentication:** JWT / OAuth  
- **Validation:** Express-validator / Joi  
- **Testing:** Jest / Mocha (if implemented)  
- **Deployment:** Docker / Heroku / AWS (optional, if deployed)  

---

## 📂 Project Structure

```
/src
 ┣ /routes        → API routes  
 ┣ /controllers   → Business logic  
 ┣ /models        → Database schemas  
 ┣ /middlewares   → Auth, validation, error handling  
 ┗ server.js      → App entry point  
```

---

## ⚙️ Installation

Clone the repository:
```bash
git clone https://github.com/anuragverma4895/social-media-api.git
cd social-media-api
```

Install dependencies:
```bash
npm install
```

Set up environment variables (`.env` file):
```env
PORT=5000
DB_URI=your_database_uri
JWT_SECRET=your_jwt_secret
```

Run the server:
```bash
npm run dev
```

---

## 📌 Usage Examples

### Register a user
```http
POST /api/auth/register
```
Body:
```json
{
  "username": "john_doe",
  "email": "john@example.com",
  "password": "mypassword"
}
```

### Login
```http
POST /api/auth/login
```
Response:
```json
{
  "token": "your_jwt_token"
}
```

### Create a post
```http
POST /api/posts
Authorization: Bearer <token>
```
Body:
```json
{
  "text": "Hello world!",
  "media": ["https://example.com/image.jpg"]
}
```

---

## 📖 API Endpoints

| Method | Endpoint                 | Description          | Auth Required |
|--------|---------------------------|----------------------|---------------|
| POST   | `/api/auth/register`     | Register new user    | No            |
| POST   | `/api/auth/login`        | Login & get token    | No            |
| GET    | `/api/posts`             | Get all posts        | Yes           |
| POST   | `/api/posts`             | Create a post        | Yes           |
| GET    | `/api/posts/:id`         | Get a single post    | Yes           |
| PUT    | `/api/posts/:id`         | Update a post        | Yes           |
| DELETE | `/api/posts/:id`         | Delete a post        | Yes           |
| POST   | `/api/posts/:id/comment` | Add a comment        | Yes           |

---

## 🧪 Testing

Run tests (if implemented):
```bash
npm test
```

---

## 🤝 Contributing

Contributions are welcome!  
- Fork the repo  
- Create a new branch (`feature/new-feature`)  
- Commit changes and push  
- Open a Pull Request  

---

## 📜 License

This project is licensed under the **MIT License**.

---

## 👤 Author

- **Anurag Verma**  
- GitHub: [anuragverma4895](https://github.com/anuragverma4895)  
- Email: your-email@example.com
