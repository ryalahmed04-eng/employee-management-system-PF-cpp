# Employee Management System (C++)

A console-based Employee Management System built in C++ as a Programming Fundamentals (PF) project. It lets a logged-in user add, view, search, update, and delete employee records stored in memory.

## Features
- **Signup/Login** — create a username/password at startup, then log in to access the system
- **Add Employee(s)** — enter data for one or more employees (name, ID, address, contact, salary)
- **Show All Employees** — display all stored records
- **Search Employee** — look up a record by ID
- **Update Employee** — edit an existing record by ID
- **Delete Employee** — delete a specific record by ID, or clear all records
- **Logout / Exit** — return to login screen or close the program

## Tech Stack
- Language: C++
- Libraries: `<iostream>`, `<conio.h>`, `<windows.h>`
- Storage: In-memory array (`emp e[100]`) — data is not saved between runs

## How to Run
> **Note:** This project uses `conio.h` and `windows.h`, which are Windows-only headers. Compile and run on Windows (e.g. with MinGW or Visual Studio).

```bash
g++ EmployeeManagementSystem.cpp -o EmployeeManagementSystem
EmployeeManagementSystem.exe
```

1. Enter a new username and password when prompted (signup).
2. Log in with the same credentials.
3. Use the menu (1–7) to add, view, search, update, or delete employee records.

## Project Structure
```
.
├── EmployeeManagementSystem.cpp   # Full source code
└── README.md
```

## Known Limitations
- Data is stored in a fixed-size array (max 100 employees) and is lost when the program exits — no file/database persistence.
- No input validation (e.g. non-numeric input for salary/contact can cause issues).
- Deleting the last record in the array can behave unexpectedly (edge case in the shift logic).
