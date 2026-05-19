# Movie_ticket_booking_system
An online movie ticket system in Java is a project that allows us to view movies, we can also search for showtimes, and book tickets. This project helps beginners to learn core concepts like object-oriented programming, collections, and user-input handling as well.

Project Title
Movie Ticket Booking System
Project Description
The Movie Ticket Booking System is a Java-based application developed to automate the process of booking movie tickets. This system allows users to view available movies, select show timings, book tickets, and manage booking details efficiently.
The project is designed using Java concepts such as classes, objects, inheritance, exception handling, collections, file handling, and JDBC for database connectivity. It provides a simple and user-friendly interface for managing movie ticket reservations.
Features
User registration and login
Display available movies
Show movie timings and seat availability
Book movie tickets
Cancel booked tickets
Generate booking details and receipt
Admin can add/update/delete movie details
Database connectivity using JDBC
Simple and interactive user interface
Software Requirements
Hardware Requirements
Processor: Intel i3 or above
RAM: 4 GB minimum
Storage: 500 MB free space
Software Requirements
Operating System: Windows/Linux/Mac
Java Development Kit (JDK 8 or above)
NetBeans / Eclipse / IntelliJ IDEA
MySQL Database
JDBC Driver
Command Prompt or Terminal
Steps to Run the Project
Step 1: Install Required Software
Install Java JDK
Install MySQL Database
Install any Java IDE (NetBeans/Eclipse/IntelliJ)
Step 2: Create Database
Open MySQL.
Create a database named:
SQL
CREATE DATABASE movie_booking;
Create required tables for users, movies, bookings, etc.
Step 3: Configure JDBC
Add MySQL JDBC Driver to the project libraries.
Update database username and password in the Java code.
Example:
Java
String url = "jdbc:mysql://localhost:3306/movie_booking";
String user = "root";
String password = "your_password";
Step 4: Compile the Project
Using terminal:
Bash
javac Main.java
Step 5: Run the Project
Using terminal:
Bash
java Main
Or run directly using the IDE.
