# ER Diagram Workshop – Submission Template
# NAME: MANIYARASAN R
# REG NO: 212224040185

## Objective
To understand and apply ER modeling concepts by creating ER diagrams for real-world applications.

## Purpose
Gain hands-on experience in designing ER diagrams that represent database structure including entities, relationships, attributes, and constraints.

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
 
![Workshop - ER Diagram1 jpg](https://github.com/user-attachments/assets/f5ab0112-6170-4275-a082-d52617854ef0)


### Entities and Attributes

| Entity      | Attributes (PK, FK)                                   | Notes                              |
|-------------|--------------------------------------------------------|------------------------------------|
| TRAINER     | Trainer_ID (PK), Trainer_Name, Phone_Number, Specialization | Stores trainer details             |
| PROGRAM     | Program_ID (PK), Program_Name, Duration, Schedule      | Training programs offered          |
| MEMBER      | Member_ID (PK), Name, Start_Date, Membership_Type      | Registered members                 |
| PAYMENT     | Payment_ID (PK), Payment_Type, Amount, Payment_Date    | Payments made by members           |
| SESSION     | Session_ID (PK), Session_Date, Session_Time            | Training session details           |
| ATTENDANCE  | Attendance_ID (PK), Status                             | Attendance record for sessions     |


### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|-------------|--------------|------|
| ASSIGNED_TO  | M : N       | Partial       | Trainers can be assigned to multiple programs |
| JOINS        | M : N       | Partial       | Members can join multiple programs |
| MAKES        | 1 : N       | Total on PAYMENT | A member can make multiple payments |
| BOOKS        | 1 : N       | Partial       | Members can book multiple sessions |
| ATTENDS      | 1 : N       | Total on ATTENDANCE | Each session can have multiple attendance records |




### Assumptions

- Each trainer can be assigned to multiple programs, and a program may have multiple trainers.
- Members can join more than one program at the same time.
- Each payment is made by exactly one member, but a member can make multiple payments.
- Members can book multiple sessions, but each booking belongs to one member.
- Each attendance record corresponds to a specific session.
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
![Workshop - ER Diagram_page-0002 jpg](https://github.com/user-attachments/assets/d926a0ae-b3b3-4eb8-b810-d99a76d3bbc9)



### Entities and Attributes


| Entity   | Attributes (PK, FK)                     | Notes                          |
|----------|------------------------------------------|--------------------------------|
| MEMBER   | M_ID (PK), Name, Email, Phno, Addr      | Stores member details          |
| LOAN     | Loan_ID (PK), Loan_Date, Return_Date, F_Amt | Records borrowing transactions |
| BOOK     | Book_ID (PK), Title, Author, Category   | Information about books        |
| EVENT    | Event_ID (PK), Event_Name, Date, Time   | Library events conducted       |
| SPEAKER  | Speaker_ID (PK), Name, Expertise        | Speakers invited for events    |
| ROOM     | Room_ID (PK), Room_Name, Capacity       | Rooms used for events          |


### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes                                   |
|--------------|-------------|--------------|-----------------------------------------|
| BORROWS      | 1 : N       | Total on LOAN | A member can borrow multiple books      |
| LOAN_FOR     | N : 1       | Total on LOAN | Each loan refers to one book            |
| REGISTERS    | M : N       | Partial       | Members can register for multiple events|
| HAS          | 1 : N       | Partial       | An event can have multiple speakers     |
| CONDUCTED    | N : 1       | Total on EVENT| Each event is conducted in one room     |



### Assumptions

- A member can borrow multiple books, but each loan record corresponds to one member and one book.
- Members can register for multiple events and each event can have multiple members registered.
- Each event can have one or more speakers.
- Every event is conducted in exactly one room, but a room can host multiple events at different times.
- A loan may include a fine amount if the book is returned late.

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
*Paste or attach your diagram here*  
![ER Diagram](er_diagram_restaurant.png)

### Entities and Attributes

| Entity | Attributes (PK, FK) | Notes |
|--------|--------------------|-------|
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |
|        |                    |       |

### Relationships and Constraints

| Relationship | Cardinality | Participation | Notes |
|--------------|------------|---------------|-------|
|              |            |               |       |
|              |            |               |       |
|              |            |               |       |

### Assumptions
- 
- 
- 

---

## Instructions for Students

1. Complete **all three scenarios** (A, B, C).  
2. Identify entities, relationships, and attributes for each.  
3. Draw ER diagrams using **draw.io / diagrams.net** or hand-drawn & scanned.  
4. Fill in all tables and assumptions for each scenario.  
5. Export the completed Markdown (with diagrams) as **a single PDF**
