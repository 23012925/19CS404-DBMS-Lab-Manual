# ER Diagram Workshop – Submission Template

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

## NAME : JANARTHANAN K
## REG. NO: 212223040072
---

# Scenario A: City Fitness Club Management

**Business Context:**  
FlexiFit Gym wants a database to manage its members, trainers, and fitness programs.

**Requirements:**  
- Members register with name, membership type, and start date.  
- Each member can join multiple programs (Yoga, Zumba, Weight Training).  
- Trainers assigned to programs; a program may have multiple trainers.  
- Members may book personal training sessions with trainers.  
- Attendance recorded for each session.  
- Payments tracked for memberships and sessions.

### ER Diagram:



### Entities and Attributes



### Relationships and Constraints


---

# Scenario B: City Library Event & Book Lending System

**Business Context:**  
The Central Library wants to manage book lending and cultural events.

**Requirements:**  
- Members borrow books, with loan and return dates tracked.  
- Each book has title, author, and category.  
- Library organizes events; members can register.  
- Each event has one or more speakers/authors.  
- Rooms are booked for events and study.  
- Overdue fines apply for late returns.

### ER Diagram:


### Entities and Attributes


### Relationships and Constraints

---

# Scenario C: Restaurant Table Reservation & Ordering

**Business Context:**  
A popular restaurant wants to manage reservations, orders, and billing.

**Requirements:**  
- Customers can reserve tables or walk in.  
- Each reservation includes date, time, and number of guests.  
- Customers place food orders linked to reservations.  
- Each order contains multiple dishes; dishes belong to categories (starter, main, dessert).  
- Bills generated per reservation, including food and service charges.  
- Waiters assigned to serve reservations.

### ER Diagram:

<img width="1305" height="818" alt="image" src="https://github.com/user-attachments/assets/2a6027cf-9b50-484d-b505-0ed37a548a01" />

### Entities and Attributes

Customer: Customer_ID, Name

Reservation: Reservation_ID, Date, Time, No_of_Guests, Customer_ID, Table_ID

Table: Table_ID, Capacity

Dish: Dish_ID, Name, Price, Category_ID

Category: Category_ID, Name


### Relationships and Constraints

TO (Customer → Reservation) (Cardinality: 1:N, Participation: Partial)
Each customer can make many reservations, and each reservation belongs to one customer.

FOR (Reservation → Table) (Cardinality: 1:N, Participation: Partial)
A reservation may include one or more tables; each table may be reserved multiple times.

SELECT (Category → Dish) (Cardinality: 1:N, Participation: Total)
A category can contain many dishes; each dish belongs to one category.

TOTAL (Reservation → Bill) (Cardinality: 1:1, Participation: Total for Bill)
Every reservation generates one bill.
