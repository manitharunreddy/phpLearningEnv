# 🚀 PHP + MySQL Development Environment (Docker)

This project provides a simple Docker-based setup to develop and run PHP applications with MySQL, all isolated in containers. Ideal for local development, learning, or quick prototyping.

---

## 📦 What's Included

- **PHP 8.2 + Apache**: Serves PHP applications.
- **MySQL 8.0**: Stores application data with persistent volume.
- **phpMyAdmin** *(optional)*: Web GUI to manage your MySQL database.
- **Live Code Editing**: Your host files sync into the container.

---

## 📁 Project Structure

```
phpLearningenv/
├── docker-compose.yml
├── php/
│   └── index.php
└── README.md
```

---

## 🚀 How to Use

### 1. Clone or Download

```bash
git clone https://github.com/yourusername/phpLearningEnv.git
cd phpLearningEnv
```

### 2. Start Containers

Make sure Docker Desktop is running, then:

```bash
docker-compose up -d
```

### 3. Access Your App

- PHP App: [http://localhost:8080](http://localhost:8080)
- phpMyAdmin: [http://localhost:8081](http://localhost:8081) *(if enabled)*

---

## 🧠 MySQL Info

| Key       | Value        |
|-----------|--------------|
| Host      | `db`         |
| Database  | `mydb`       |
| User      | `user`       |
| Password  | `userpass`   |
| Root Pass | `rootpass`   |

---

## 🗂 Data Persistence

MySQL data is stored locally at:

```
C:\Users\0633\Desktop\mysql_data
```

You can back it up or inspect it directly from your desktop.

---

## 📥 Example Code (`php/index.php`)

```php
<?php
$mysqli = new mysqli("db", "user", "userpass", "mydb");
if ($mysqli->connect_error) {
  die("❌ Connection failed: " . $mysqli->connect_error);
}
echo "✅ Connected to MySQL successfully!";
?>
```

---

## 🧹 Stopping & Cleanup

To stop containers:

```bash
docker-compose down
```

To remove volumes too (i.e., erase MySQL data):

```bash
docker-compose down -v
```

---

## 📌 Requirements

- Docker Desktop (Windows, Mac, or Linux)
- Git (optional but recommended)

---

## 📃 License

MIT — use this setup freely for learning or development.

---

Feel free to customize this environment for Laravel, WordPress, or other PHP frameworks.
