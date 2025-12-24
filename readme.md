# Expense Tracker App (Node.js + Express + MySQL)

A simple Expense Tracker web application built using **Node.js**, **Express**, **EJS**, and **MySQL**, with automated deployment using **Jenkins CI/CD**.

---

## 🚀 Features

- Add, view, and delete expenses
- Track expense details:
  - Title
  - Category
  - Amount
  - Payment Mode
  - Expense Date
  - Notes
- MySQL database integration
- Server-side rendering with EJS
- Jenkins-based CI/CD deployment

---

## 🛠 Tech Stack

- Node.js
- Express.js
- EJS
- MySQL
- Jenkins

---

## 📁 Project Structure

```
Expense-Tracker-App/
├── views/
│   └── index.ejs
├── app.js
├── db.js
├── package.json
├── Jenkinsfile
└── README.md
```

---

## ⚙️ Local Setup

### 1. Clone Repository
```bash
git clone https://github.com/Swatiz-cloud/Expense-Tracker-App.git
cd Expense-Tracker-App
```

### 2. Install Dependencies
```bash
npm install
```

### 3. MySQL Database Setup
```sql
CREATE DATABASE expense_db;
USE expense_db;

CREATE TABLE expenses (
  id INT AUTO_INCREMENT PRIMARY KEY,
  title VARCHAR(100),
  category VARCHAR(50),
  amount DECIMAL(10,2),
  payment_mode VARCHAR(20),
  expense_date DATE,
  notes VARCHAR(255),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

### 4. Configure Database (`db.js`)
```js
const db = mysql.createConnection({
  host: "localhost",
  user: "expense_user",
  password: "StrongPassword@123",
  database: "expense_db"
});
```

### 5. Run Application
```bash
npm start
```

Access: http://localhost:3000

---

## 🤖 Jenkins Deployment Guide

### Prerequisites
- Jenkins installed
- Node.js & npm on Jenkins server
- PM2 installed (`npm install -g pm2`)
- MySQL accessible

---

### Create Jenkins Job
1. Jenkins Dashboard → New Item
2. Select **Pipeline**
3. SCM → Git
4. Repo URL: https://github.com/Swatiz-cloud/Expense-Tracker-App.git
5. Save → Build Now

---

## 📌 Notes

- Use environment variables for DB credentials in production
- Recommended to Dockerize for scalable deployments
- Can be extended with authentication and reporting features

---

## 👩‍💻 Author

**Swati Zampal**  
Cloud & DevOps Engineer | AWS Certified
