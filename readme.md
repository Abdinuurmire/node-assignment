# Companies CRUD API

A simple **CRUD REST API** built with **Node.js**, **Express**, and **MySQL2**, following the **MVC architecture** pattern. This application allows users to create, read, update, and delete **companies** stored in a MySQL database.

---

## 📌 Features

* Create a new company
* Get all companies
* Get a single company by ID
* Update a company
* Delete a company
* Uses **MySQL2 with prepared statements** (SQL Injection safe)
* Environment variables managed with **dotenv**
* Structured using **MVC architecture**

---

## 🛠️ Technologies Used

* Node.js
* Express.js
* MySQL2
* dotenv

---

## 📁 Project Structure

```
project/
│
├── config/
│   └── db.js
│
├── models/
│   └── company.model.js
│
├── controllers/
│   └── company.controller.js
│
├── routes/
│   └── company.routes.js
│
├── .env
├── .gitignore
├── server.js
└── package.json
```

---

## 🗄️ Database Setup (IMPORTANT)

### 1️⃣ Create the Database

Create a MySQL database named:

```
CRUD_DB
```

### 2️⃣ Create the `companies` Table

Run the following SQL command:

```sql
CREATE TABLE companies (
  id INT AUTO_INCREMENT PRIMARY KEY,
  name VARCHAR(255) NOT NULL,
  desc TEXT NOT NULL
);
```

* `id` is **auto-incremented**
* `name` stores the company name
* `desc` stores company details

---

## 🔐 Environment Variables (.env)

Create a `.env` file in the root directory:

```
PORT=3000
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=
DB_NAME=CRUD_DB
DB_PORT=3306
```

⚠️ Ensure `.env` is included in `.gitignore`

---

## 📦 Install Dependencies

```bash
npm install
```

---

## ▶️ Run the Server

```bash
npm start
```

OR

```bash
node server.js
```

Server will start at:

```
http://localhost:3000
```

---

## 🔄 API Endpoints (CRUD)

### ➕ Create a Company

**POST** `/companies`

```json
{
  "name": "Tech Solutions Ltd",
  "desc": "Software development company"
}
```

---

### 📄 Get All Companies

**GET** `/companies`

---

### 🔍 Get Company by ID

**GET** `/companies/:id`

Example:

```
/companies/1
```

---

### ✏️ Update a Company

**PUT** `/companies/:id`

```json
{
  "name": "Tech Solutions International",
  "desc": "Global software services company"
}
```

---

### ❌ Delete a Company

**DELETE** `/companies/:id`

---

## ⚠️ Error Handling

* Proper HTTP status codes (`200`, `201`, `404`, `500`)
* `try...catch` used for async logic
* Clean, user-friendly error messages

---

## ✅ Assignment Compliance

✔ MVC Architecture implemented
✔ MySQL2 used with prepared statements
✔ dotenv used for environment variables
✔ All CRUD operations implemented
✔ Server runs with `npm start`

---

## 👤 Author

**Ganacdase Abdinur Mire**

---

## 📜 License

This project is for educational purposes only.

