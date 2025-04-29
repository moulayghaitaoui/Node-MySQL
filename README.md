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
- MySQL (with `mysql2`)
- dotenv
- REST API

---

## 🛠️ Setup Instructions

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/notes-api.git
cd notes-api
npm install
 #Create .env file
MYSQL_HOST=localhost
MYSQL_USER=root
MYSQL_PASSWORD=yourpassword
MYSQL_DATABASE=notesdb
4. Create MySQL table
CREATE DATABASE IF NOT EXISTS notesdb;

USE notesdb;

CREATE TABLE notes (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(255) NOT NULL,
  contents TEXT NOT NULL,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
