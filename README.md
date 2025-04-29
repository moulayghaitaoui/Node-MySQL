# 📝 Notes API – Node.js & MySQL

This is a simple RESTful API built using **Node.js**, **Express**, and **MySQL** to manage notes. It supports creating, retrieving all notes, and retrieving a specific note by ID.

---

## 🚀 Features

- Retrieve all notes
- Retrieve a note by ID
- Create a new note
- Clean architecture with async/await
- MySQL connection via `mysql2` with connection pooling
- Environment variable support via `dotenv`

---

## 📦 Tech Stack

- Node.js
- Express.js
- MySQL (`mysql2`)
- dotenv
- REST API

---

## 🛠️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/notes-api.git
cd notes-api
```

### 2. Install dependencies

```bash
npm install
```

### 3. Create `.env` file

Create a `.env` file in the root directory and add your MySQL credentials:

```env
MYSQL_HOST=localhost
MYSQL_USER=root
MYSQL_PASSWORD=yourpassword
MYSQL_DATABASE=notesdb
```

### 4. Set up MySQL database

Run the following SQL commands in your MySQL console:

```sql
CREATE DATABASE IF NOT EXISTS notesdb;

USE notesdb;

CREATE TABLE notes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  contents TEXT NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 5. Start the server

```bash
node index.js
```

Your server will be running at: [http://localhost:8080](http://localhost:8080)

---

## 📮 API Endpoints

### `GET /notes`
Retrieve all notes.

### `GET /notes/:id`
Retrieve a single note by its ID.

### `POST /notes`
Create a new note.  
**Request body:**
```json
{
  "title": "My Note Title",
  "contents": "This is the content of the note."
}
```

---

## 📁 Folder Structure

```
.
├── index.js         # Main server file
├── database.js      # DB logic and queries
├── .env             # Environment variables (not committed)
├── package.json
└── README.md
```

---

## 👨‍💻 Author

**Ghaitaoui Moulay El Hadj**  
[GitHub](https://github.com/moulayghaitaoui)

---

## 📄 License

This project is licensed under the MIT License.
