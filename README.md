# The-Flood-Relief-camp

# 🌊 Flood Relief Camp Management System

## 📌 Project Overview

The **Flood Relief Camp Management System** is a Java-based console application designed to manage and streamline operations in a flood relief camp. It helps in registering affected families, tracking resource distribution, and generating daily summaries for efficient relief management.

This project demonstrates the integration of **Java (JDBC)** with a **MySQL database** for real-time data handling.

---

## 🚀 Features

* ✅ Register new families affected by floods
* ✅ Record daily distribution of essentials (food, water, medicine)
* ✅ Prevent duplicate distribution entries for the same day
* ✅ Generate daily summary reports
* ✅ Simple menu-driven console interface

---

## 🛠️ Technologies Used

* **Java** (Core Java, JDBC)
* **MySQL** (Database)
* **SQL** (Schema & Queries)

---

## 📂 Project Structure

```
Flood Relief Camp/
│
├── Main/
│   └── Main.java              # Main application (menu-driven system)
│
├── src/
│   └── DBConnection.java      # Database connection setup
│
├── sql/
│   └── schema.sql            # Database schema file
│
└── Screenshots/
    ├── ss1.png
    └── ss2.png
```

---

## 🗄️ Database Schema

### Database: `flood_relief`

#### 1. Families Table

| Column  | Type     | Description              |
| ------- | -------- | ------------------------ |
| fam_id  | INT (PK) | Unique family ID         |
| head    | VARCHAR  | Head of family name      |
| village | VARCHAR  | Village name             |
| members | INT      | Number of family members |

#### 2. Distributions Table

| Column    | Type     | Description                         |
| --------- | -------- | ----------------------------------- |
| dist_id   | INT (PK) | Distribution ID                     |
| fam_id    | INT (FK) | References families table           |
| dist_date | DATE     | Distribution date (default current) |
| food_kg   | DECIMAL  | Food distributed (kg)               |
| water_l   | DECIMAL  | Water distributed (liters)          |
| medicine  | BOOLEAN  | Medicine provided (true/false)      |

---

## ⚙️ Setup & Installation

### 1. Install MySQL

Make sure MySQL is installed and running on your system.

### 2. Create Database

Run the following SQL file:

```sql
SOURCE path_to/schema.sql;
```

### 3. Configure Database Connection

Update credentials in `DBConnection.java`:

```java
private static final String URL = "jdbc:mysql://localhost:3306/flood_relief";
private static final String USER = "root";
private static final String PASSWORD = "your_password";
```

### 4. Compile the Project

```bash
javac Main/Main.java src/DBConnection.java
```

### 5. Run the Application

```bash
java Main.Main
```

---

## 🖥️ How It Works

### Menu Options:

1. **Register Family**
   Add details of a new family

2. **Record Distribution**
   Enter daily distribution data

3. **Daily Summary**
   View total resources distributed

4. **Exit**
   Close the application

---

## 📸 Screenshots

Screenshots of the system are available in the `Screenshots/` folder.

---

## ⚠️ Important Notes

* Ensure MySQL server is running before starting the application
* Avoid duplicate entries for the same family on the same day (handled by constraint)
* Update database credentials before running

---

## 📈 Future Enhancements

* GUI-based interface (JavaFX / Swing)
* User authentication system
* Report export (PDF/Excel)
* Web-based version using Spring Boot

---

## 👩‍💻 Author

**Esita Kundu**
MCA Final Year Project

---

## 📄 License

This project is for academic purposes only.
