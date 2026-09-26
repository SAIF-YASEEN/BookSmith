# 📚 Booksmith — Library Management System

[![Java](https://img.shields.io/badge/Java-17+-orange.svg)](https://www.oracle.com/java/)
[![OOP](https://img.shields.io/badge/Programming-OOP-blue.svg)]()
[![File Handling](https://img.shields.io/badge/Storage-File%20Handling-green.svg)]()
[![Console App](https://img.shields.io/badge/Interface-Console-yellow.svg)]()

**Booksmith** is a comprehensive **Library Management System** built with Java and Object-Oriented Programming principles. It provides a practical way to manage books, members, librarians, borrowing operations, and library records through a structured console interface.

The project demonstrates core Java concepts including **classes, inheritance, polymorphism, encapsulation, abstraction, collections, file handling, and data persistence**.

> **Customized and maintained by Saif Yaseen.**

---

## 🎯 Project Overview

Booksmith provides a complete set of features for managing day-to-day library operations:

* **Book Management** — Add, search, issue, and return books
* **Member Management** — Register and manage different membership types
* **Librarian Management** — Manage librarian profiles and administrative information
* **File Persistence** — Store application data using local files
* **Inheritance Hierarchy** — `Person → Member / Librarian`
* **Polymorphism** — Abstract methods and method overriding
* **Library Statistics** — View useful information about books and members
* **Backup Support** — Create backups of stored library data

---

## 🔧 OOP Concepts Demonstrated

### 1. Classes and Objects

The project uses multiple classes to represent real-world library entities:

* `Book` — Represents books and their current status
* `Person` — Abstract base class for library users
* `Member` — Represents library members
* `Librarian` — Represents library staff
* `Library` — Handles the main library operations
* `FileHandler` — Handles file-based data persistence

### 2. Inheritance

```text
Person (Abstract Base Class)
├── Member (extends Person)
└── Librarian (extends Person)
```

### 3. Encapsulation

The application uses:

* Private fields
* Public getter/setter methods
* Data validation
* Encapsulated business logic
* Protected members where required for inheritance

### 4. Polymorphism

Polymorphism is demonstrated through:

* Abstract methods in the `Person` class
* Method overriding
* Different implementations of inherited behavior

### 5. File Handling

Booksmith stores data locally using file handling:

* Reading and writing text files
* CSV-style data storage
* Backup functionality
* Error handling for file operations

---

## 📸 User Interface

Booksmith uses a structured console interface designed to make navigation simple and readable.

### Main Menu

```text
┌──────────────────────────────────────────────────┐
│                    BOOKSMITH                     │
│              LIBRARY MANAGEMENT SYSTEM           │
├──────────────────────────────────────────────────┤
│ 1. Book Management                               │
│ 2. Member Management                             │
│ 3. Librarian Management                          │
│ 4. Issue / Return Books                           │
│ 5. Search & Display                              │
│ 6. Library Statistics                            │
│ 7. Backup Data                                   │
│ 8. Exit                                          │
└──────────────────────────────────────────────────┘
```

The interface uses:

* Clean menu navigation
* Unicode box-drawing characters
* Formatted tables
* Consistent headings
* Structured information displays
* Auto-adjusting table columns

---

# 🚀 Features

## 📖 Book Management

* ✅ Add new books
* ✅ Search books by title
* ✅ Search books by author
* ✅ Search books by category
* ✅ Search books by ID
* ✅ View available books
* ✅ View issued books
* ✅ Track book status
* ✅ Display detailed book information

## 👥 Member Management

Booksmith supports different membership types:

| Membership | Maximum Books |
| ---------- | ------------: |
| Regular    |             3 |
| Premium    |            10 |
| Student    |             5 |

Members can be:

* Registered
* Viewed
* Searched
* Associated with issued books
* Tracked by membership type

## 👨‍💼 Librarian Management

Librarian functionality includes:

* Add librarian profiles
* Store employee information
* Department management
* Salary information
* Administrative library operations

## 🔄 Issue and Return System

* ✅ Issue books to members
* ✅ Return books
* ✅ Check book availability
* ✅ Validate member limits
* ✅ Track issue dates
* ✅ Automatically calculate due dates
* ✅ Enforce borrowing restrictions

The default borrowing period is **14 days**.

## 💾 Data Persistence

No external database is required.

The application uses local files for storage:

* Books
* Members
* Librarians
* Backup data

Data is automatically loaded when the application starts.

## 📊 Reports and Statistics

Booksmith provides statistics including:

* Total number of books
* Available books
* Issued books
* Books by category
* Members by membership type
* Library activity information

---

# 📁 Project Structure

```text
Booksmith/
├── src/
│   ├── Book.java
│   ├── Person.java
│   ├── Member.java
│   ├── Librarian.java
│   ├── Library.java
│   ├── FileHandler.java
│   └── LibraryManagementApp.java
│
├── data/
│   ├── books.txt
│   ├── members.txt
│   └── librarians.txt
│
├── build/
├── docs/
├── compile_and_run.bat
├── run.bat
└── README.md
```

---

# 🚀 Quick Start

## Prerequisites

Before running Booksmith, make sure you have:

* **Java JDK 8 or higher**
* Command Prompt or terminal
* Windows for the included `.bat` scripts, or another operating system for manual compilation

---

## Method 1 — Windows Batch Files

Navigate to the project directory:

```bash
cd Booksmith
```

Compile and run for the first time:

```bash
.\compile_and_run.bat
```

For subsequent runs:

```bash
.\run.bat
```

---

## Method 2 — Manual Compilation

Navigate to the project:

```bash
cd Booksmith
```

Create the build directory:

```bash
mkdir build
```

Compile:

```bash
javac -d build src/*.java
```

Run:

```bash
cd build
java LibraryManagementApp
```

---

## Method 3 — Using an IDE

You can open the project using:

* IntelliJ IDEA
* Eclipse
* VS Code with Java extensions
* Other Java-compatible IDEs

Set the `src` directory as the source directory and run:

```text
LibraryManagementApp.java
```

---

# 🎮 How to Use

## 1. First Launch

When Booksmith starts, the application can create sample library data.

Sample data is stored in:

```text
data/
```

## 2. Main Menu

```text
┌──────────────────────────────────────────────────┐
│                    BOOKSMITH                     │
├──────────────────────────────────────────────────┤
│ 1. Book Management                               │
│ 2. Member Management                             │
│ 3. Librarian Management                          │
│ 4. Issue / Return Books                           │
│ 5. Search & Display                              │
│ 6. Library Statistics                            │
│ 7. Backup Data                                   │
│ 8. Exit                                          │
└──────────────────────────────────────────────────┘
```

## 3. Issue a Book

Example:

```text
1. Select Issue / Return Books
2. Select Issue Book
3. Enter Book ID: B001
4. Enter Member ID: M001
```

The system automatically calculates the return date.

Default borrowing period:

```text
14 days
```

## 4. Add a Member

Navigate to:

```text
Member Management
        ↓
Add New Member
```

Then enter the member information and select:

```text
Regular
Premium
Student
```

The appropriate borrowing limit is automatically applied.

## 5. Search Books

Navigate to:

```text
Search & Display
        ↓
Search Books
```

Books can be searched using:

* Book ID
* Title
* Author
* Category

---

# 📊 Sample Data

## Default Books

| ID   | Book             | Author        |
| ---- | ---------------- | ------------- |
| B001 | Java Programming | James Gosling |
| B002 | Data Structures  | Robert Lafore |
| B003 | Clean Code       | Robert Martin |
| B004 | Design Patterns  | Gang of Four  |
| B005 | Algorithms       | Thomas Cormen |

## Default Members

| ID   | Member      | Type    | Limit |
| ---- | ----------- | ------- | ----: |
| M001 | John Doe    | Regular |     3 |
| M002 | Jane Smith  | Premium |    10 |
| M003 | Bob Johnson | Student |     5 |

## Default Librarian

| ID   | Name         | Department   |
| ---- | ------------ | ------------ |
| L001 | Alice Wilson | Main Library |

---

# 🔍 OOP Implementation

## Inheritance

```java
public abstract class Person {
    protected String id;
    protected String name;
    protected String email;
    protected String phone;
    protected String address;

    public abstract String getRole();
    public abstract void displayInfo();
    public abstract String toFileString();
}
```

### Member

```java
public class Member extends Person {
    private String membershipType;
    private List<String> issuedBooks;

    // Member-specific functionality
}
```

### Librarian

```java
public class Librarian extends Person {
    private String employeeId;
    private String department;
    private double salary;

    // Librarian-specific functionality
}
```

---

## Encapsulation

The `Book` class demonstrates encapsulation through private fields and controlled access:

```java
public class Book {

    private String bookId;
    private boolean isIssued;

    public String getBookId() {
        return bookId;
    }

    public boolean issueBook(
            String memberId,
            String issueDate,
            String returnDate
    ) {

        if (!isIssued) {
            this.isIssued = true;

            // Additional issue logic

            return true;
        }

        return false;
    }
}
```

---

## File Handling

Booksmith uses Java I/O classes to save library data:

```java
public static boolean saveBooks(List<Book> books) {

    try (
        BufferedWriter writer =
            new BufferedWriter(
                new FileWriter(BOOKS_FILE)
            )
    ) {

        for (Book book : books) {
            writer.write(book.toFileString());
            writer.newLine();
        }

        return true;

    } catch (IOException e) {

        System.err.println(
            "Error saving books: " + e.getMessage()
        );

        return false;
    }
}
```

---

# 📈 Learning Outcomes

This project demonstrates practical understanding of:

### 🎯 Core OOP

* Encapsulation
* Inheritance
* Polymorphism
* Abstraction
* Classes and objects
* Method overriding

### 💾 File Handling

* Reading files
* Writing files
* Data persistence
* CSV-style storage
* Exception handling

### 🏗️ Software Design

* Separation of responsibilities
* Reusable classes
* Business logic organization
* Object-oriented architecture
* Data management

### 🔧 Programming Practices

* Input validation
* Error handling
* Java naming conventions
* Structured application design
* User-friendly console interaction

---

# 🚀 Future Enhancements

Possible future improvements include:

* [ ] GUI using Swing or JavaFX
* [ ] MySQL database integration
* [ ] SQLite support
* [ ] Advanced search and filtering
* [ ] Fine management
* [ ] Late-return penalties
* [ ] Email due-date notifications
* [ ] Barcode scanning
* [ ] PDF report generation
* [ ] Multi-library/branch support
* [ ] JUnit testing
* [ ] Logging
* [ ] Configuration files
* [ ] Authentication and authorization

---

# 🎓 Educational Value

Booksmith can be used to practice:

* Java fundamentals
* Object-Oriented Programming
* Classes and objects
* Inheritance
* Polymorphism
* Encapsulation
* Abstraction
* File I/O
* Collections
* Data persistence
* Application architecture
* Problem solving

### Resume Skills Demonstrated

* Java
* Object-Oriented Programming
* File Handling
* Data Persistence
* Inheritance
* Polymorphism
* Encapsulation
* Abstraction
* CRUD Operations
* Console Application Development
* Software Design

---

# 👨‍💻 Project Information

**Project:** Booksmith — Library Management System
**Developer / Maintainer:** Saif Yaseen
**Language:** Java
**Programming Paradigm:** Object-Oriented Programming
**Application Type:** Console Application
**Difficulty:** Intermediate
**Estimated Development Time:** 2–3 days

This version of Booksmith has been **customized, reworked, and maintained by Saif Yaseen** as a Java/OOP portfolio project.

---

# 🤝 Contributing

Contributions and improvements are welcome.

### Development Workflow

```bash
git checkout -b feature/new-feature
```

Implement and test your changes, then:

```bash
git add .
git commit -m "Add new feature"
git push origin feature/new-feature
```

After pushing, open a Pull Request.

### Development Guidelines

* Follow Java naming conventions
* Maintain OOP principles
* Keep responsibilities separated
* Add JavaDoc where appropriate
* Include proper error handling
* Test changes before committing
* Update documentation when adding major features

---

# 📄 License

This project is distributed under the **MIT License**.

See the `LICENSE` file for the complete license terms.

If this repository was adapted from an existing open-source project, retain the original license and required attribution notices.

---

<div align="center">

# 📚 Booksmith

### Library Management System

**Built with Java and Object-Oriented Programming**

**Developed and maintained by Saif Yaseen**

</div>
