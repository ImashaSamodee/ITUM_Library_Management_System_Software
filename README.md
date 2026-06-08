# 📚 ITUM Library Management System

> A full-stack web-based Library Management System built for the Institute of Technology, University of Moratuwa (ITUM), enabling students and admins to manage books, issue/return transactions, fines, and member records through a role-based dashboard.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap_5-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)

---

## 📖 About

The **ITUM Library Management System** is a web application designed for ITUM students and library staff. Users can register, log in with their Registration Number, and access a dashboard to issue and return books. Admins have additional access to manage members, generate reports, and handle fine management — all through a clean sidebar-based dashboard.

Library hours: **Open 08:00 AM – Close 06:00 PM**

---

## ✨ Features

### 👨‍🎓 User Features
- 🏠 **Home Page** — Welcome page with library hours and Get Started button
- 🔐 **Login / Register** — Secure session-based login using Registration Number and hashed password
- 📊 **Dashboard** — Quick-access cards for all available modules
- 📚 **Book Management** — Add, View, Update, and Delete books (with modal popups)
- 📤 **Issue Books** — Issue an available book to a registered member with due date tracking
- 📥 **Return Books** — Return an issued book and update its availability status

### 🛠️ Admin-Only Features
- 👥 **Members** — View all registered members
- 📋 **Fine Management** — Manage fines for overdue books
- 📈 **Reports** — View library activity reports
- 🔒 **Role-Based Access** — Admin-only sidebar links hidden from regular users

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|------------|
| Frontend | HTML5, CSS3, JavaScript |
| UI Framework | Bootstrap 5.3 |
| Icons | Font Awesome 6.5 / 7.0 (CDN) |
| Backend | PHP (Sessions, Prepared Statements) |
| Database | MySQL |
| Local Server | XAMPP (Apache + MySQL) |

---

## 🗄️ Database Schema

**Database name:** `library_management_system`

| Table | Key Columns |
|-------|-------------|
| `book_information` | `id`, `title`, `author`, `isbn`, `status` (`available` / `issued`) |
| `issue_return` | `id`, `registration_no`, `book_id`, `action` (`issue`/`return`), `issue_date`, `return_date`, `due_date` |
| `user_registered_info` | `RegistrationNo`, `FirstName`, `LastName`, `Password`, `Email`, `MobileNo`, `Role` |

---

## 📁 Project Structure

```
ITUM_Library_Management_System/
│
├── index.html                  # Public home page
├── login.php                   # Login page with session handling
├── register.php                # New user registration
├── library_management_system.sql  # MySQL database dump
│
├── css/
│   └── style.css               # Main stylesheet (all pages)
│
├── js/
│   └── main.js                 # Frontend JavaScript
│
├── image/
│   ├── Logo.png
│   ├── Background1.jpg
│   ├── LMS 1 .png
│   └── LMS 2 .png
│
└── php/                        # Backend PHP files
    ├── connection.php          # MySQL database connection function
    ├── dashboard.php           # Role-based dashboard (User / Admin)
    ├── book_management.php     # Add / View / Update / Delete books
    ├── issue_books.php         # Issue book to a member
    ├── return_books.php        # Return an issued book
    ├── member.php              # View all registered members (Admin)
    ├── fine_management.php     # Manage overdue fines (Admin)
    └── report.php              # Library reports (Admin)
```

---

## 🚀 Getting Started

### Prerequisites

- [XAMPP](https://www.apachefriends.org/) (Apache + MySQL)
- A web browser

### Installation Steps

1. **Clone or download the repository**
   ```bash
   git clone https://github.com/ImashaSamodee/ITUM_Library_Management_System_Software.git
   ```

2. **Move the project to XAMPP's htdocs folder**
   ```
   C:/xampp/htdocs/ITUM_Library_Management_System
   ```

3. **Import the database**
   - Start XAMPP — turn on **Apache** and **MySQL**
   - Open [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
   - Create a new database named `library_management_system`
   - Click **Import** → select `library_management_system.sql` → click **Go**

4. **Configure database connection** *(if needed)*

   Open `php/connection.php` and update:
   ```php
   $servername = "localhost";
   $username   = "root";
   $password   = "";       // your MySQL password
   $dbname     = "library_management_system";
   ```

5. **Run the project**

   Open your browser and go to:
   ```
   http://localhost/ITUM_Library_Management_System
   ```

---

## 🔑 Default Login Credentials

| Role | Registration No | Password |
|------|----------------|----------|
| Admin | `23IT0470` | *(set during registration)* |
| User | `23IT0527` | *(set during registration)* |

> Passwords are hashed using PHP `password_hash()` — use the Register page to create a new account.

---

## 🧭 Pages & Navigation

| Page | File | Access |
|------|------|--------|
| Home | `index.html` | Public |
| Login | `login.php` | Public |
| Register | `register.php` | Public |
| Dashboard | `php/dashboard.php` | Logged-in users |
| Book Management | `php/book_management.php` | Logged-in users |
| Issue Books | `php/issue_books.php` | Logged-in users |
| Return Books | `php/return_books.php` | Logged-in users |
| Members | `php/member.php` | Admin only |
| Fine Management | `php/fine_management.php` | Admin only |
| Reports | `php/report.php` | Admin only |

---

## 👩‍💻 Author

**J.B.A. Imasha Samodee**
- GitHub: [@ImashaSamodee](https://github.com/ImashaSamodee)

---

## 📄 License

Copyright © 2025 ITUM Library Management System. All Rights Reserved.

---

<p align="center">Made with ❤️ for ITUM Students</p>
