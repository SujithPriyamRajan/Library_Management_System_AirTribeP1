# 📚 Library Management System (Pure Java, No Dependencies)

This is a **console-based Library Management System** implemented in pure Java with **no external dependencies or Maven/Gradle**.  
You can compile and run it directly using `javac` and `java`.

---

## 🚀 Getting Started

### 1️⃣ Download & Extract
Download the project and unzip it:

```bash
unzip Library_Management_System_AirTribeP1.zip -d Library_Management_System_AirTribeP1
```
```bash
cd Library_Management_System_AirTribeP1/src
```
### 2️⃣ Compile the Project
Run the following command from the src folder:

```bash
javac -d target src/com/example/lms/*.java \
               src/com/example/lms/util/*.java \
               src/com/example/lms/model/*.java \
               src/com/example/lms/repo/*.java \
               src/com/example/lms/service/*.java
```
This will generate .class files inside the same package directories.

### 3️⃣ Run the Application
From the same src folder, execute:

```bash
java -cp target com.example.lms.App
```

You will see the interactive console UI start up, with options to:

- View total book count

- Search / filter books

- Borrow and return books

- Switch between User & Admin portals

- Use commands like CLEAR, LOGOUT, EXIT

## 📂 Project Structure
```bash

Library_Management_System_AirTribeP1/
├─ src/
│  └─ com/example/lms/
│     ├─ App.java                 # Entry point
│     ├─ util/ConsoleUtil.java    # Console helpers (clear, delay print)
│     ├─ model/                   # Book, User, Loan data models
│     ├─ repo/                    # In-memory data repositories
│     └─ service/                 # LibraryService, ConsoleService, Recommendation
├─ data/
│  ├─ books.txt                   # Book data store (simple text format)
│  └─ users.txt                   # User data store (simple text format)
└─ README.md
```
### 🧪 Alternative Compile Method (from Root)
If you prefer building from the project root:

```bash
javac -d out src/com/example/lms/**/*.java
java -cp out com.example.lms.App
```
### 🧰 Commands in Console
Command	Action
- SEARCH	Search books by title/author/ID
- FILTER	Filter books by genre
- CLEAR	Clears the console screen
- EXIT	Exits the application
- ADMIN	Switches to admin panel
- LOGOUT	Logs out the current user

## ✅ Requirements

Java 11+ installed (java -version & javac -version must work)

Terminal or console that supports ANSI (for clear screen)

## 📝 Notes
No external JSON or database dependencies used — data is stored in data/books.txt and data/users.txt.

Simple repository pattern and service layer used for easy extension.

Can later be adapted for GUI or REST API.

## 📸 Example Console Output

===============================
📚 Welcome to MyLibrary
Total Books: 42 | Available: 35 | Borrowed: 7
Trending: "Harry Potter", "Lord of the Rings"
===============================

> Type a command (SEARCH / FILTER / ADMIN / EXIT):
