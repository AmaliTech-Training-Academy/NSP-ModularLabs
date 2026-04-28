# Task Management System

## Project Overview

**Complexity:** Medium
**Time Estimate:** 6–8 hours
**Technology Stack:** Java 21 (LTS), IntelliJ IDEA Community Edition, JUnit 5

This lab builds on Lab 1 – Java Basics by refactoring the Project/Task Management System for cleaner, safer, and testable code.

You will apply:

* Exception handling
* SOLID principles
* Unit testing (JUnit 5)
* Git version control

All previous functionality remains, with enhancements:

* Custom exceptions for invalid inputs
* Refactored modular code
* JUnit tests
* Git workflow integration

> Data is stored in memory using arrays (no database yet).

---

## Project Objectives

By completing this lab, you will:

* Apply clean code principles (SOLID, naming, modularity)
* Implement exception handling using try-catch and custom exceptions
* Refactor code for readability and maintainability
* Write and run JUnit tests
* Use Git for version control
* Handle invalid user inputs gracefully
* Prepare for future enhancements (collections & persistence)

---

## System Features Overview

### Feature 1: Project Catalog Management

* Create and list projects
* Validate inputs using custom exceptions
* Enforce unique project IDs and positive budgets

### Feature 2: Task Operations

* Handle invalid task assignments
* Refactor task methods
* Add unit tests for status updates and progress calculation

### Feature 3: User Management

* Separate logic into services (e.g., UserService)
* Validate email and roles
* Use Git branches for feature updates

### Feature 4: Status Processing & Reporting

* Handle empty projects using exceptions
* Test average calculations
* Refactor output formatting

### Feature 5: Menu Navigation & UX

* Input validation using exceptions
* Display user-friendly error messages
* Ensure stable menu loop

---

## Console UI Examples

### Main Menu

```
JAVA PROJECT MANAGEMENT SYSTEM

Current User: Alice Johnson (Admin)

1. Manage Projects
2. Manage Tasks
3. View Status Reports
4. Switch User
5. Exit
```

### Invalid Input Handling

```
Enter project ID: P999
Error: ProjectNotFoundException – Project ID 'P999' does not exist.
Please try again.
```

### Add Task

```
Task 'Implement API' successfully added to Project P001.
```

### Status Report

```
PROJECT ID | PROJECT NAME | TASKS | COMPLETED | PROGRESS (%)
P001       | Alpha Tracker | 4     | 3         | 75%
P002       | IoT Sensor Kit | 2    | 1         | 50%

AVERAGE COMPLETION: 62.5%
```

---

## Git Workflow Example

```bash
git init
git add .
git commit -m "Refactor: Added custom exceptions and cleaned structure"
git branch feature/testing
git checkout feature/testing
git add src/test
git commit -m "Added JUnit tests"
git checkout main
git merge feature/testing
```

---

## JUnit Test Example

```java
@Test
void testCalculateCompletionPercentage() {
    Project p = new SoftwareProject("P001", "Alpha Tracker", 5, 15000);
    p.addTask(new Task("T001", "Setup DB", "Completed"));
    p.addTask(new Task("T002", "Design UI", "In Progress"));

    double result = p.calculateCompletionPercentage();
    assertEquals(50.0, result);
}
```

---

## Project Structure

```
project-management-system/
│
├── src/
│   ├── Main.java
│   ├── models/
│   ├── interfaces/
│   ├── services/
│   └── utils/
│       └── exceptions/
│
├── test/
├── docs/
└── README.md
```

---

## Implementation Phases

### Phase 1: Refactoring (1–2 hrs)

* Apply SOLID principles
* Improve naming and structure

### Phase 2: Exception Handling (2 hrs)

* Add custom exceptions
* Implement validation

### Phase 3: Testing (2 hrs)

* Write JUnit tests
* Ensure all tests pass

### Phase 4: Git (1–2 hrs)

* Initialize repository
* Commit changes
* Use branches

---

## Minimum Requirements Checklist

* Java 21 configured
* Refactored clean code
* At least 3 custom exceptions
* Proper exception handling
* At least 3 JUnit tests passing
* Git repository with at least 3 commits
* Feature branch created and merged
* Functional console menu
* Updated README

---

## User Stories

### Refactoring

* Clean, maintainable code
* No duplication
* Clear naming

### Exception Handling

* Custom exceptions
* Graceful error handling

### Testing

* JUnit tests for core logic
* Edge cases covered

### Git

* Version control with commits and branches

### Menu Handling

* Stable UI under invalid input

---

## Testing Scenarios

1. Project creation works after refactoring
2. Task creation handles invalid project IDs
3. Project listing displays correctly
4. Completion percentage is accurate
5. Invalid inputs do not crash the system
6. All JUnit tests pass
7. Git branch workflow works
8. Remote repository reflects commits
9. Code is clean and documented

---

## Grading Rubric

| Criteria           | Points  |
| ------------------ | ------- |
| Code Refactoring   | 20      |
| Exception Handling | 20      |
| Testing            | 20      |
| Git Usage          | 15      |
| Functionality      | 15      |
| Data Structures    | 10      |
| **Total**          | **100** |

---

## Submission Requirements

### Repository Must Include:

* `/src` and `/test`
* `README.md`
* Documentation (`docs/`)
* Optional: Test screenshots

### Documentation Must Include:

* Setup instructions
* Feature summary
* Class diagram
* Refactoring explanation
* Git commit history

---

## Setup Instructions

1. Clone repository:

```bash
git clone <your-repo-link>
```

2. Open in IntelliJ IDEA

3. Run:

* `Main.java` for application
* Test classes for JUnit

---

## Notes

* No database is used (arrays only)
* Future labs will introduce collections and persistence
* Follow clean coding standards throughout
