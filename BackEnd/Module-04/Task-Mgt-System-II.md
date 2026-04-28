# Task Management System
---

## Project Objectives

By completing this project, you will be able to:

Design and implement type-safe data structures using Java Collections Framework and generics to efficiently manage complex student and grade data, selecting optimal collection types based on performance requirements and access patterns

Implement modern file I/O operations using NIO.2 API and Stream processing to handle multiple file formats (CSV, JSON, binary), with proper resource management and functional transformations for data import/export

Create comprehensive input validation using regular expressions to validate student IDs, email addresses, phone numbers, and other structured data formats, ensuring data integrity across the system

Design and implement thread-safe concurrent operations for background tasks such as batch processing, automated report generation, and real-time statistics updates using appropriate synchronization strategies and Executor framework

Optimize application performance by analyzing collection performance characteristics, implementing efficient data access patterns, and ensuring thread safety in multi-threaded operations

---

## What You'll Build

An enterprise-grade Student Grade Management System with advanced features including optimized collections, multi-format file handling, regex validation, concurrency, caching, auditing, and stream processing.

---

## Features

### Advanced Data Management

* HashMap for O(1) student lookup
* TreeMap for sorted GPA rankings
* HashSet for unique course tracking
* LinkedList for grade history
* PriorityQueue for task scheduling

### Multi-Format File Support

* CSV, JSON, Binary export/import
* NIO.2 Path and Files API
* Streaming for large files

### Regex-Based Validation

* Student ID, Email, Phone, Date, Course Code validation
* Centralized ValidationUtils class

### Concurrent Processing

* FixedThreadPool for batch reports
* CachedThreadPool for stats
* ScheduledExecutorService for tasks

### Real-Time Dashboard

* Live statistics updates
* Background daemon thread
* Thread-safe data structures

### Caching System

* ConcurrentHashMap-based cache
* LRU eviction policy
* Cache statistics tracking

### Audit Trail

* Async logging
* Thread-safe logging queue
* Log rotation support

---

## Console Output Examples

### Main Menu

```
╔════════════════════════════════════════════╗
║   STUDENT GRADE MANAGEMENT - MAIN MENU     ║
╚════════════════════════════════════════════╝
```

### Features include:

* File export/import
* Real-time dashboard
* Batch processing
* Regex search
* Scheduled tasks

---

## User Stories

### US-1: Advanced Data Management

Use optimized collections for performance:

* HashMap → student lookup
* TreeMap → GPA ranking
* HashSet → unique courses

### US-2: Multi-Format File Operations

* CSV, JSON, Binary support
* NIO.2 streaming
* WatchService integration

### US-3: Regex Validation

Patterns:

* STU\d{3}
* Email regex
* Phone formats
* Date YYYY-MM-DD

### US-4: Concurrent Batch Reports

* ThreadPoolExecutor
* Progress tracking
* Performance comparison

### US-5: Real-Time Dashboard

* Auto-refresh every 5 seconds
* Background thread updates

### US-6: Scheduled Tasks

* Daily GPA calculation
* Hourly stats refresh
* Weekly reports

### US-7: Pattern Search

* Regex-based filtering
* Domain search
* ID search

### US-8: Caching System

* LRU cache
* Hit/miss tracking
* Thread-safe access

### US-9: Audit Trail

* Async logging
* Thread ID tracking
* Log rotation

### US-10: Stream Processing

* map, filter, reduce
* parallelStream
* Files.lines()

---

## Architecture

### Collections

* HashMap → Students
* TreeMap → GPA rankings
* ArrayList → ordered data
* HashSet → uniqueness
* ConcurrentHashMap → cache

### Thread Pools

* FixedThreadPool → reports
* CachedThreadPool → stats
* ScheduledThreadPool → tasks
* SingleThreadExecutor → logging

---

## Testing Requirements

* 25+ unit tests
* 10+ integration tests
* 85%+ coverage
* Concurrency testing
* Regex validation tests
* Stream processing tests

---

## Git Workflow

### Branch Strategy

* main
* develop
* feature branches

### Required Commits

* 30+ commits
* Conventional commits
* Feature-based structure

---

## Minimum Requirements

### Collections

* HashMap O(1) lookup
* TreeMap sorting
* HashSet uniqueness

### File I/O

* NIO.2 usage
* Streaming files
* Multi-format support

### Concurrency

* Thread-safe operations
* ExecutorService usage

### Regex

* Precompiled patterns
* ValidationUtils class

### Streams

* Functional operations
* Parallel processing

---

## Performance Benchmarks

* HashMap vs ArrayList lookup
* Sequential vs parallel streams
* File I/O comparisons
* Thread pool efficiency

---

## Final Requirement

All features must be fully implemented, tested, and documented with proper Git workflow and performance analysis.

# Database Fundamentals

## Complexity: Advanced | Time Estimate: 10–12 hours

---

## Project Objectives

By the end of this project, learners will be able to:

* Design and normalize a relational or non-relational database schema that models a blogging domain effectively.
* Develop conceptual, logical, and physical database models to ensure scalability and maintainability.
* Implement CRUD operations and complex queries using SQL (or equivalent NoSQL queries) and JDBC.
* Apply indexing, caching, searching, and sorting algorithms to optimize database access and performance.
* Integrate database operations into a JavaFX application interface for interactive content management.
* Compare relational (SQL) and NoSQL designs for unstructured data such as comments or reviews.
* Measure and document performance improvement through optimization and indexing techniques.

---

## Project Description

This stage of the Smart Blogging Platform focuses on building the data layer and persistence logic that will support all future modules.

Students will design a relational or non-relational database for a blogging system, implement the schema using SQL or NoSQL, and integrate it with a JavaFX application that performs core operations including post creation, comment management, tag assignment, and analytics reporting.

The system must reflect real-world blogging logic (users, posts, comments, tags, reviews) while incorporating data structure and algorithm (DSA) concepts such as indexing, caching, sorting, and searching to enhance performance and scalability.

---

## Epics and User Stories

### Epic 1: Database Design and Modeling

#### User Story 1.1

As a database designer, I want to create conceptual, logical, and physical database models so that the data structure of the blogging platform is efficient and scalable.

**Acceptance Criteria:**

* Conceptual ERD or NoSQL schema includes all major entities and relationships.
* Logical model defines attributes, primary/foreign keys, and relationships.
* Physical model includes SQL data types, constraints, and normalization up to 3NF.

#### User Story 1.2

As a database administrator, I want to define indexes and relationships so that queries and lookups run efficiently while maintaining data integrity.

**Acceptance Criteria:**

* Primary and foreign keys defined.
* Indexes created on frequently queried fields (title, author ID, tag name).
* Referential integrity enforced.

---

### Epic 2: Data Access and CRUD Operations

#### User Story 2.1

As a blogger, I want to add, update, and delete blog posts and comments through a JavaFX interface so that I can manage my content easily.

**Acceptance Criteria:**

* CRUD operations functional via JavaFX UI.
* Input validation and feedback messages implemented.
* Database constraints prevent invalid entries.

#### User Story 2.2

As a reader, I want to view and search for blog posts so that I can explore content of interest.

**Acceptance Criteria:**

* Dynamic post listing from database.
* Pagination, filters, and search implemented.
* Parameterized queries used (JDBC/NoSQL driver).

---

### Epic 3: Searching, Sorting, and Optimization

#### User Story 3.1

As a reader, I want to search posts by keyword, tag, or author so that I can find relevant content efficiently.

**Acceptance Criteria:**

* Case-insensitive search implemented.
* Indexing improves performance.
* Execution time improvements documented.

#### User Story 3.2

As a developer, I want caching and sorting mechanisms so frequently accessed data loads faster.

**Acceptance Criteria:**

* In-memory caching implemented (Map/List).
* Sorting/searching algorithms applied.
* Cache invalidation implemented.

---

### Epic 4: Performance and Query Optimization

#### User Story 4.1

As an analyst, I want performance reports comparing queries before and after optimization.

**Acceptance Criteria:**

* Execution time tracked.
* Indexing improvements demonstrated.
* Performance report documented.

#### User Story 4.2

As a developer, I want to store comments in NoSQL format for flexibility.

**Acceptance Criteria:**

* NoSQL schema implemented.
* Justification documented.
* Optional comparison with SQL provided.

---

### Epic 5: Reporting and Documentation

#### User Story 5.1

As a contributor, I want full documentation of the database system.

**Acceptance Criteria:**

* ERD/schema diagrams included.
* SQL/NoSQL scripts provided.
* README includes setup and execution steps.

---

## Technical Requirements

### Database

* MySQL/PostgreSQL or MongoDB
* 3NF normalization for SQL
* Entities: Users, Posts, Comments, Tags, Reviews
* Indexed fields for performance

### Application Layer (JavaFX)

* JavaFX UI for CRUD and analytics
* JDBC or MongoDB driver
* Layered architecture (Controller → Service → DAO)
* In-memory caching using Maps/Lists

### DSA Integration

* Hashing for caching
* Sorting/searching algorithms
* Indexing concept mapping
* Performance comparison metrics

---

## Deliverables

* Database Design Document (ERD + schema)
* SQL/NoSQL implementation scripts
* JavaFX application
* Performance report
* README setup guide
* Testing evidence

---

## Evaluation Criteria

* Database Design: 25 pts
* SQL/NoSQL Implementation: 20 pts
* JavaFX Integration: 20 pts
* DSA Application: 15 pts
* Performance Optimization: 10 pts
* Documentation & Code Quality: 10 pts

**Total: 100 pts**
