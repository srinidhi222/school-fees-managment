# school-fees-managment
This project implements a simple school fees management system using Python and SQLite.
Features

*   Add new students with their details and total fees.
*   View a list of all students and their fee status.
*   Record payments made by students.
*   View a history of all payments.

## How to Use

1.  Run the first code cell to create the SQLite database and necessary tables.
2.  Run the second code cell, which contains the main application logic.
3.  Follow the on-screen menu to perform actions like adding students, viewing students, recording payments, and viewing payments.

## Database Schema

The database `school_fees_management.db` contains two tables:

### `students`

| Column      | Type    | Description                      |
| :---------- | :------ | :------------------------------- |
| `student_id` | INTEGER | Primary Key, Auto-incrementing   |
| `name`      | TEXT    | Student's Name                   |
| `class`     | TEXT    | Student's Class                  |
| `fees_paid` | REAL    | Total fees paid by the student   |
| `total_fees`| REAL    | Total fees for the student       |

### `payments`

| Column        | Type    | Description                        |
| :------------ | :------ | :--------------------------------- |
| `payment_id`  | INTEGER | Primary Key, Auto-incrementing     |
| `student_id`  | INTEGER | Foreign Key referencing `students` |
| `amount`      | REAL    | Amount paid in the payment         |
| `payment_date`| DATE    | Date of the payment                |

