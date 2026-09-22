<div align="center">

# 🏦 Bank Management System

### A Secure, Full-Featured Banking Application Built with Java & MySQL

[![Java](https://img.shields.io/badge/Java-JDK%208%2B-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white)](https://www.java.com/)
[![MySQL](https://img.shields.io/badge/MySQL-8.0-4479A1?style=for-the-badge&logo=mysql&logoColor=white)](https://www.mysql.com/)
[![JDBC](https://img.shields.io/badge/JDBC-Database%20Connectivity-007396?style=for-the-badge&logo=java&logoColor=white)](https://docs.oracle.com/javase/tutorial/jdbc/)
[![Swing](https://img.shields.io/badge/GUI-Java%20Swing-orange?style=for-the-badge)](https://docs.oracle.com/javase/tutorial/uiswing/)
[![License](https://img.shields.io/badge/License-MIT-success?style=for-the-badge)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen?style=for-the-badge)](CONTRIBUTING.md)

<img src="docs/screenshots/banner.png" alt="Bank Management System Banner" width="100%"/>

**A production-style desktop banking solution** demonstrating real-world OOP design, secure JDBC database transactions, and an intuitive Swing UI — perfect for academic projects and portfolio showcases.

[📥 Download](#-getting-started) · [🐛 Report Bug](https://github.com/SIRATHNAYAKA/Bank-Management-System--master/issues) · [✨ Request Feature](https://github.com/SIRATHNAYAKA/Bank-Management-System--master/issues)

</div>

---

## 📑 Table of Contents

<details open>
<summary>Click to expand / collapse</summary>

- [📌 Overview](#-overview)
- [🎯 Key Highlights](#-key-highlights)
- [✨ Features](#-features)
- [🛠 Tech Stack](#-tech-stack)
- [🏗 Architecture](#-architecture)
- [📂 Project Structure](#-project-structure)
- [🗄 Database Schema](#-database-schema)
- [🚀 Getting Started](#-getting-started)
- [🎮 Usage](#-usage)
- [🖼 Screenshots](#-screenshots)
- [🔐 Security Notes](#-security-notes)
- [🧪 Testing](#-testing)
- [🔮 Roadmap](#-roadmap)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [📬 Contact](#-contact)

</details>

---

## 📌 Overview

**Bank Management System (BMS)** is a comprehensive desktop application that replicates the core operations of a modern retail bank. Built on **Java SE** with **MySQL** as the persistence layer, it delivers a realistic simulation of customer onboarding, account management, secure transactions, and administrative oversight — all through a clean, event-driven Swing interface.

The project emphasizes **clean architecture**, **separation of concerns**, and **robust error handling**, making it an ideal reference for students and developers learning enterprise-grade Java development.

> 💡 **Why this project?** Most academic banking projects stop at CRUD. This one implements transaction integrity, role-based access, audit trails, and input sanitization — bringing it closer to what real fintech systems require.

---

## 🎯 Key Highlights

| 🏆 | Highlight |
| :-: | :--- |
| 🔐 | **Role-based authentication** — Separate customer and admin access levels |
| 💰 | **ACID-compliant transactions** — Deposits, withdrawals and transfers with rollback safety |
| 🧾 | **Full audit trail** — Every action timestamped and logged |
| 🧠 | **Layered architecture** — Model → DAO → Service → UI |
| ⚡ | **Zero-downtime connection pooling** — Efficient JDBC resource management |
| 🛡️ | **Input validation & SQL-injection protection** — All queries use `PreparedStatement` |
| 📊 | **Real-time balance updates** — No stale data anywhere in the UI |
| 🎨 | **Polished Swing UI** — Custom themes, icons and intuitive navigation |

---

## ✨ Features

### 👤 Customer Portal

| Feature | Description |
| :--- | :--- |
| 🆕 **Account Registration** | Create savings or current accounts with auto-generated unique account numbers |
| 🔑 **Secure Login** | PIN-protected access with hashed credential storage |
| 💵 **Deposit** | Add funds instantly — balance updates in real time |
| 🏧 **Withdraw** | Cash-out with insufficient-balance guardrails |
| 🔄 **Fund Transfer** | Move money between accounts using atomic transactions |
| 📊 **Balance Inquiry** | View current balance and account metadata |
| 📜 **Transaction History** | Full statement with filters by date, type and amount |
| 🔒 **PIN Change** | Update your PIN after verifying current credentials |
| 🚪 **Logout** | Safe session termination |

### 🛡️ Admin Console

| Feature | Description |
| :--- | :--- |
| 👥 **Customer Management** | View, search, edit and deactivate accounts |
| 📈 **Transaction Monitoring** | Live view of all system-wide transactions |
| 📑 **Reports** | Daily / monthly summaries exportable for auditing |
| ⚙️ **System Configuration** | Manage interest rates, transaction limits and fees |
| 🔍 **Audit Log** | Trace any action back to its origin |

### ⚙️ Technical Features

- **JDBC with PreparedStatements** — 100% protection against SQL injection
- **Connection Pooling** — Reduced latency under load
- **Exception Handling** — Custom exception hierarchy (`BankException`, `InsufficientFundsException`, etc.)
- **Modular Design** — Swap the UI or DB layer without touching business logic
- **Config-driven** — All DB credentials in `db.properties`, never hardcoded

---

## 🛠 Tech Stack

<div align="center">

| Category | Technology |
| :--- | :--- |
| **Language** | Java SE 8+ |
| **Database** | MySQL 5.7 / 8.0 |
| **DB Connectivity** | JDBC (MySQL Connector/J) |
| **GUI Framework** | Java Swing (with custom Look & Feel) |
| **Build Tool** | Maven / Gradle *(optional)* |
| **IDE Support** | IntelliJ IDEA · Eclipse · NetBeans |
| **Version Control** | Git + GitHub |

</div>

---

## 🏗 Architecture

The application follows a **classic 4-tier layered architecture**:
