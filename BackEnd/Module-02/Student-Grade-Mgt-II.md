# Student Grade Management System: Project/Task Management Lab

## Project Overview
* **Complexity:** Medium
* **Time Estimate:** 10 hours
* **Technology Stack:** Java 21 (LTS), IntelliJ IDEA Community Edition

### Description
Build a console-based **Project/Task Management System** where users can create projects, add and assign tasks, record task completion status, and calculate completion averages. This lab focuses on core Java programming and Object-Oriented Programming (OOP) principles while storing all data in-memory using arrays.

This project serves as the foundation for a multi-week series. Future labs will enhance this base by replacing arrays with Collections, adding file persistence, and integrating user authentication.

---

## Learning Objectives
By completing this lab, you will be able to:
1.  **Design** a console-based application using core Java.
2.  **Apply OOP principles** (Encapsulation, Inheritance, and Polymorphism).
3.  **Manage Data** using Java arrays, loops, and conditional structures in memory.
4.  **Define Architecture** using classes, abstract classes, and interfaces.
5.  **Implement Polymorphism** through method overloading and overriding.
6.  **Create UI** with structured menu-driven console interfaces and input validation.
7.  **Compute Logic** to aggregate data and calculate project completion percentages.

---

## System Features

### 1. Project Catalog Management
* Create new projects (e.g., `SoftwareProject`, `HardwareProject`).
* View projects with details: ID, name, description, team size, and budget.
* Filter projects by type.
* Display project-specific attributes dynamically.

### 2. Task Operations
* Add tasks to specific projects.
* Manage task statuses: `Pending`, `In Progress`, `Completed`.
* Update or delete tasks.
* Input validation for statuses and duplicate task names.

### 3. User Management
* Roles: `RegularUser` and `AdminUser`.
* Role-based access control (Admin: Delete/Update | Regular: View/Add).
* Automatic unique ID generation.

### 4. Status Processing & Reporting
* Calculate completion averages per project.
* Generate status reports (e.g., “Project Alpha is 75% complete”).
* Display task statistics: total, completed, and pending counts.

### 5. User Experience
* Clear main menu and sub-menus.
* Validation for numbers, text, and IDs.
* Graceful exit and return navigation.

---

## Technical Requirements (User Stories)

### Epic 1: Project Catalog Management
* **US-1.1:** Browse projects with ID, name, type, and budget.
* **Technical:** Create abstract class `Project` with private fields and an abstract method `getProjectDetails()`. Implement subclasses `SoftwareProject` and `HardwareProject`.

### Epic 2: Task Operations
* **US-2.1:** Add tasks with unique IDs and initial status.
* **Technical:** Create `Task` class. Implement `Completable` interface with a `boolean isCompleted()` method.

### Epic 3: User Management
* **US-3.1:** Create `RegularUser` and `AdminUser` roles.
* **Technical:** Abstract `User` class with static counters for ID generation.

### Epic 4: Reporting
* **US-4.1:** Calculate completions.
* **Technical:** Iterate through task arrays to count completions and round results to 2 decimals.

---

## Project Structure
```text
project-management-system/
│
├── src/
│   ├── Main.java                     # Application entry point
│   ├── models/
│   │   ├── Project.java              # Abstract base class
│   │   ├── SoftwareProject.java      # Concrete project type
│   │   ├── HardwareProject.java      # Concrete project type
│   │   ├── Task.java                 # Task model
│   │   ├── User.java                 # Abstract user base
│   │   ├── RegularUser.java          # Concrete user type
│   │   ├── AdminUser.java            # Concrete user type
│   │   └── StatusReport.java         # Status report generation
│   │
│   ├── interfaces/
│   │   └── Completable.java          # Interface for completion logic
│   │
│   ├── services/
│   │   ├── ProjectService.java       # Project operations
│   │   ├── TaskService.java          # Task operations
│   │   └── ReportService.java        # Reporting logic
│   │
│   └── utils/
│       ├── ConsoleMenu.java          # Menu handling
│       └── ValidationUtils.java      # Input validation
│
├── docs/
│   ├── class-diagram.png
│   └── design-decisions.md
│
└── README.md
