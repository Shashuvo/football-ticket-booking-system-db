# Football Ticket Booking System Database

## Overview

This project implements a **Football Ticket Booking System** database designed to manage football fans, tournament matches, and ticket booking transactions. The project demonstrates database modeling concepts, ERD design, relational schema creation, and SQL query implementation.

## Project Objectives

* Design an Entity Relationship Diagram (ERD).
* Implement relational database tables with Primary Keys and Foreign Keys.
* Maintain referential integrity between entities.
* Write SQL queries using filtering, joins, aggregation, subqueries, null handling, and pagination.
* Demonstrate practical database management concepts through a real-world football ticket booking scenario.

---

## Database Schema

### 1. Users Table

Stores information about football fans and administrative staff.

| Column       | Description                               |
| ------------ | ----------------------------------------- |
| user_id      | Unique identifier for each user           |
| full_name    | User's full name                          |
| email        | Email address used for login              |
| role         | User role (Football Fan / Ticket Manager) |
| phone_number | Contact phone number                      |

### 2. Matches Table

Stores football match information and ticket details.

| Column              | Description                      |
| ------------------- | -------------------------------- |
| match_id            | Unique identifier for each match |
| fixture             | Competing teams                  |
| tournament_category | League or tournament name        |
| base_ticket_price   | Standard ticket price            |
| match_status        | Availability status              |

### 3. Bookings Table

Stores ticket booking transactions.

| Column         | Description               |
| -------------- | ------------------------- |
| booking_id     | Unique booking identifier |
| user_id        | References Users table    |
| match_id       | References Matches table  |
| seat_number    | Allocated stadium seat    |
| payment_status | Booking payment status    |
| total_cost     | Final ticket cost         |

---

## Entity Relationships

### One-to-Many

* One User can have multiple Bookings.

### Many-to-One

* Many Bookings can belong to one Match.

### Logical One-to-One

* Each booking record represents a unique reservation made by one user for one specific match and seat.

---

## Features Implemented

* Primary Key Constraints
* Foreign Key Constraints
* Referential Integrity
* NULL Handling
* Pattern Matching (LIKE / ILIKE)
* INNER JOIN
* LEFT JOIN
* Aggregate Functions
* Subqueries
* ORDER BY
* LIMIT & OFFSET Pagination

---

## SQL Queries Included

### Query 1

Retrieve all available Champions League matches.

### Query 2

Search users by name pattern using LIKE and ILIKE.

### Query 3

Replace NULL payment statuses using COALESCE.

### Query 4

Display booking details with user and match information using INNER JOIN.

### Query 5

Display all users and their bookings using LEFT JOIN.

### Query 6

Find bookings with total cost above average using a subquery.

### Query 7

Retrieve the second and third most expensive matches using ORDER BY, LIMIT, and OFFSET.

---

## ERD

The ERD illustrates:

- Users → Bookings (1:N)
- Matches → Bookings (1:N)
- Primary Keys (PK)
- Foreign Keys (FK)
- Relationship Cardinality
- Status Attributes

🔗 **[View ERD Diagram](https://drive.google.com/file/d/1WRZIC0-isFKklRLNlBzlYiCILurHdpxc/view?usp=sharing)**

---

## Project Structure

```text
football-ticket-booking-system-db/
│
├── README.md
├── QUERY.sql
├── schema.sql
├── sample_data.sql
└── ERD/
    └── football_ticket_booking_erd.png
```

---

## Technologies Used

* PostgreSQL / MySQL
* SQL
* Draw.io (ERD Design)
* Git & GitHub

---

## Learning Outcomes

This project demonstrates understanding of:

* Database Design
* ER Modeling
* Relational Schema Design
* SQL Query Development
* Database Constraints
* Data Integrity
* Join Operations
* Aggregate Functions
* Subqueries

---

## Author

**MD. Shahariat Hossen Shuvo**

BSc in Computer Science & Engineering

Database Management Systems Assignment
