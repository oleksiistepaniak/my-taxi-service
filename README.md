# Taxi Service App
This project imitates the work of a taxi service. The project has been built on the SOLID-principles. The project has a built-in security mechanism that ensures the protection of user confidential information and ride data. To use the service, you need to register and authorize.The project follows the Model-View-Controller (MVC) design pattern.

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

# Structure:
- ### **Controllers:**
 
| Controller                    | Description                                   | Address               |
|-------------------------------|-----------------------------------------------|-----------------------|
| IndexController               | Get to the home page                          | /index or /           |
| LoginController               | Authenticate as a user                        | /login                |
| LogoutController              | Logout from the account                       | /logout               |
| AddCarController              | Add car to the database                       | /cars/add             |
| AddDriverToCarController      | Add driver to the car                         | /cars/drivers/add     |
| DeleteCarController           | Delete car from the database                  | /cars/delete          |
| GetAllCarsController          | Get all cars from the database                | /cars                 |
| GetMyCurrentCarsController    | Get all cars of authorized user (driver)      | /drivers/cars         |
| AddDriverController           | Add driver to the database (register)         | /drivers/add          |
| DeleteDriverController        | Delete driver from the database               | /drivers/delete       |
| GetAllDriversController       | Get all drivers from the database (all users) | /drivers              |
| AddManufacturerController     | Add manufacturer to the database              | /manufacturers/add    |
| DeleteManufacturerController  | Delete manufacturer from the database         | /manufacturers/delete |
| GetAllManufacturersController | Get all manufacturers from the database       | /manufacturers        |

- ### **DAO:**

| DaoImpl (handler)   | Model        |
|---------------------|--------------|
| CarDaoImpl          | Car          |
| DriverDaoImpl       | Driver       |
| ManufacturerDaoImpl | Manufacturer |

- ### **Exceptions:**

| Custom exception        | Description                                                            |
|-------------------------|------------------------------------------------------------------------|
| AuthenticationException | an exception indicating problems with authentication                   |
| DataProcessingException | an exception indicating problems with processing data on the DAO layer |

- ### **Models:**

| Model        | Description                         |
|--------------|-------------------------------------|
| Car          | a model representing a car          |
| Driver       | a model representing a driver       |
| Manufacturer | a model representing a manufacturer |

- ### **Services:**

| Service                   | Description                                                    |
|---------------------------|----------------------------------------------------------------|
| AuthenticationServiceImpl | a service happening all business logic with authentication     |
| CarServiceImpl            | a service happening all business logic with car model          |
| DriverServiceImpl         | a service happening all business logic with driver model       |
| ManufacturerServiceImpl   | a service happening all business logic with manufacturer model |

- ### **Util:**

| Util           | Description                                                  |
|----------------|--------------------------------------------------------------|
| ConnectionUtil | an utility allows us to establish connections with databases |

- ### **Web.Filter:**

| Filter               | Description                                 |
|----------------------|---------------------------------------------|
| AuthenticationFilter | a filter handles the authentication process |


# How to run this project locally?

- clone this repository;
- open this project (you can do it in Intellij IDEA or in a different environment of development);
- run the SQL script (it's located in src/main/resources/init_db.sql);
- set up ConnectionUtil variables (it's located in src/main/java/util/ConnectionUtil);
- build the project (you need to use Maven);
- deploy the WAR file to a servlet container (for instance, it may be Tomcat);
- open your browser and navigate to http://localhost:8080 (after that you will have access to the taxi service app).