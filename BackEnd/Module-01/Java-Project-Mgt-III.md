# Java Project Management System (Console Edition)

## Project Overview
Build a console-based **Project/Task Management System** using Java 21. This application serves as a foundation for learning object-oriented principles, using in-memory arrays to manage projects, tasks, and users.

**Tech Stack:** Java 21 (LTS), IntelliJ IDEA Community Edition.

---

## Learning Objectives
* Design a menu-driven console interface.
* Apply **OOP Principles**: Encapsulation, Inheritance, and Polymorphism.
* Manage data in-memory using **Java Arrays** and loops.
* Implement **Interface-based logic** for completion tracking.
* Validate complex user inputs (regex, numeric ranges, and state).

---

## 🏗 System Features

### 1. Project Catalog Management
* Create and browse `SoftwareProject` and `HardwareProject` types.
* Filter projects by type or search by budget range.
* Display project-specific attributes dynamically via method overriding.

### 2. Task Operations
* Add and assign tasks to specific projects.
* Manage statuses: `Pending`, `In Progress`, and `Completed`.
* Validate against duplicate task names within a project.

### 3. User Management
* Role-based access: `AdminUser` (Manage) vs. `RegularUser` (View/Add).
* Auto-generate unique User IDs using static counters.

### 4. Reporting & Analytics
* Calculate project completion percentages: $(Completed \div Total) \times 100$.
* Aggregate statistics across all projects for an "Average Completion" report.

---

## 🖥 Console UI Examples

### Main Menu
```text
╔════════════════════════════════════════════╗
║     JAVA PROJECT MANAGEMENT SYSTEM         ║
╚════════════════════════════════════════════╝
Current User: Alice Johnson (Admin)

1. Manage Projects
2. Manage Tasks
3. View Status Reports
4. Switch User
5. Exit
