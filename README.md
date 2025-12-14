## 📚 Mini Project: Library Management System
## 📝 Project Overview

## This project is a Library Management System developed as part of the Mini Project Assignment (Group of 2) for your course.
## It allows librarians to manage books, register new librarians, and view available books. The system is deployed publicly for testing and demonstration.

## Domain: libraryvugatime

## Group Members:

## Name	RegNumber
## ROBERT NIYONKURU	24RP05300
## ALINE SIWEMUBI	24RP05404

## Live URL:
https://libraryvugatime.free.nf/

## Test Credentials:

Admin / Librarian Login

Username: robert

Password: robert

## Additional librarians can register via the Signup page.

💻 Technical Details
1️⃣ Database (MySQL)

## The project uses MySQL / MariaDB with the following tables:

## Tables:

1. librarians

Column	Type	Notes
id	INT	Primary Key, Auto Increment
fullname	VARCHAR	Required
username	VARCHAR	Required, Unique
password	VARCHAR	Hashed

2. books

Column	Type	Notes
id	INT	Primary Key, Auto Increment
title	VARCHAR	Required
author	VARCHAR	Required
year	INT	Required
category	VARCHAR	Required
description	TEXT	Optional
# and other tables# 
## Constraints:

Unique username for librarians

Auto-increment IDs

Proper field types for each column

Database Export:
Include library_db.sql in the submission folder.

## 2️⃣ PHP Backend

## A. PDO with Prepared Statements

All database interactions use PDO.

Both named and positional placeholders are used.

bindParam() / bindValue() used to prevent SQL injection.

## B. Form Data Validation

All required fields validated.

Input trimmed to remove unnecessary spaces.

User-friendly error messages.

Passwords hashed using password_hash().

## C. Login & Logout (Session Management)

Librarian signup and login implemented.

Password encryption with password_hash() and password_verify().

Protected pages use session checks.

Logout destroys sessions.

## D. CRUD Operations

Books Module: Add, View, Edit, Delete books.

Librarians Module: Signup, Login, View registered librarians.

## E. Exception Handling

try {
    // PDO database operations
} catch(PDOException $e) {
    echo "Database Error: " . $e->getMessage();
}

## 3️⃣ UI / Frontend

Simple, clean HTML/CSS structure.

Forms with proper validation and placeholders.

Success and error messages displayed clearly.

Navigation links between Home, Books, Library, and Logout.

Optional Bootstrap used for responsiveness and styling.

## 4️⃣ Deployment

Hosting: InfinityFree

Live URL: https://libraryvugatime.free.nf/

Database imported via phpMyAdmin.

All PHP files linked properly to handle CRUD and login.

## 5️⃣ Submission Includes

Full project folder with PHP files.

style.css for styling.

library_db.sql for database.

README file with all project details.

Live demo URL and test login credentials.
