# Library Management System

A Java-based library management system.

## Features

- **Book Management**
  - Add/remove books with details (title, author, price , publication year)
  - Track book status (Available, Issued, Overdue)
  
- **Member Management**
  - Register members with contact details
  - Track member fines in ₹

- **Lending Operations**
  - Issue books to members
  - Return books with automatic fine calculation (₹10/day overdue)
  - Prevent issuing to members with overdue books

- **Monitoring**
  - Background thread checks for overdue books every minute
  - Detailed overdue notifications with fine calculations

- **Search & Reporting**
  - Find books by author/title
  - Find members by name/email
  - Sort books by title/author

- **Financial Tracking**
  - All prices and fines in Indian Rupees (₹)
  - Fine payment system
  - Overdue fine notifications

## File Structure
src/
├── Main.java # Entry point with demo scenarios
├── model/
│ ├── Book.java # Book entity with ₹ pricing
│ ├── BookStatus.java # Enum (Available/Issued/Overdue)
│ ├── Member.java # Member entity with fine tracking
│ └── LendingRecord.java # Lending details with fine calculation
├── exception/
│ ├── LibraryException.java # Base exception
│ ├── BookNotAvailableException.java
│ ├── MemberNotFoundException.java
│ └── OverdueBookException.java
├── repository/
│ └── Repository.java # Generic data storage
└── service/
├── LibraryService.java # Core business logic
└── OverdueMonitor.java # Background overdue checker

## How to Run

1. **Compile the project**:
   ```bash
   javac -d . src/*.java src/*/*.java
   