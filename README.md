# Taxi Service App
This project imitates the work of a taxi service. The project has been built on the SOLID-principles.

# Technologies:
- JDK 11;
- Java Servlet API 4.0.1;
- JDBC API;
- SQL (a program that has been written on the MySQL Database Management System);
- MySQL 8.0.22;
- Maven 3.8.0;
- JSTL 1.2;
- Tomcat 9.0.73;
- JSP;
- CSS;

# Features:

- creating / deleting a driver;
- creating / deleting a manufacturer;
- creating / deleting a car;
- displaying all drivers / manufacturers / cars;
- assigning a driver to the car;
- authentication of user (it's been built based on the Driver model);

# How to run this project locally?

- clone this repository;
- open this project (you can do it in Intellij IDEA or in a different environment of development);
- run the SQL script (it's located in src/main/resources/init_db.sql);
- set up ConnectionUtil variables (it's located in src/main/java/util/ConnectionUtil);
- build the project (you need to use Maven);
- deploy the WAR file to a servlet container (for instance, it may be Tomcat);
- open your browser and navigate to http://localhost:8080 (after that you will have access to the taxi service app).