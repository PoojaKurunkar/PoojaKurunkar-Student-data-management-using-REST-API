This project is a REST API designed to manage student data, developed using Hibernate and Spring Boot. It leverages a robust application architecture to ensure scalability and maintainability. The inclusion of a service layer as an intermediate layer for DAO sources enhances the structure and functionality of the application. This project was a significant learning experience, helping to deepen my skills in building reliable and scalable applications.

This structure follows the typical layout for a Spring Boot application, organized into various packages under the src directory.

**src/main/java**
This is the primary source folder where your Java code resides. It is organized into several packages:

**com.demo Package:**

Application.java: This is the main entry point for your Spring Boot application. It typically contains the @SpringBootApplication annotation and the main method to run the application.
com.demo.controller Package:

home.java: This likely contains the REST controller logic. Controllers are responsible for handling HTTP requests and returning appropriate responses.
com.demo.dao Package:

studentDao.java: DAO stands for Data Access Object. This interface or class is responsible for interacting with the database. It usually contains methods for CRUD operations (Create, Read, Update, Delete).
com.demo.model Package:

student.java: This class represents the data model for a student. It typically contains attributes related to a student and is often annotated with JPA annotations like @Entity to map it to a database table.
com.demo.service Package:

studentService.java: This interface defines the business logic for the application. It usually declares methods that the service layer will implement.
studentServiceImpl.java: This class implements the studentService interface. It contains the actual business logic and interacts with the DAO layer to perform operations on the database.


**src/main/resources**
This folder contains configuration files and other resources needed by the application.

application.properties: This file contains various configuration settings for the Spring Boot application, such as database connection details, server port, logging levels, etc.

server.port=9010
# database information
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.datasource.url=jdbc:mysql://localhost:3306/sb        #sb is the name of my database
spring.datasource.username=root

**#hibernate information**
spring.jpa.properties.hibernate.dialect=org.hibernate.dialect.MySQL5Dialect
spring.jpa.properties.hibernate.hbm2ddl.auto=update
spring.jpa.properties.hibernate.show_sql=true
spring.jpa.properties.hibernate.format_sql=true 

**Explanation**
Main Application Class (Application.java): This is the starting point of your Spring Boot application. Running this class will launch your application.
Controller (home.java): This handles incoming HTTP requests, directs them to appropriate service methods, and returns responses. It uses annotations like @RestController and @RequestMapping.
Data Access Object (studentDao.java): This is responsible for direct database interactions. It may use Spring Data JPA repositories or custom queries.
Model (student.java): This defines the structure of the student entity. It includes fields like sid, sname, scity,smarks , etc., and their respective getters and setters.
Service Layer (studentService and studentServiceImpl.java): The service layer contains business logic. The interface studentService defines the methods, and the implementation class studentServiceImpl provides the logic for these methods.
Configuration (application.properties): This file is crucial for setting up your application's environment and dependencies.
This structured approach helps in maintaining a clean, modular, and scalable codebase, making it easier to manage and extend in the future.


**Technologies used:**
* Hibernate: For efficient ORM and database operations. 
-Spring Boot: To streamline the development process and ensure a smooth, modular structure.
* Application Architecture: To maintain a clean and scalable codebase, ensuring easy maintenance and future 
enhancements.
* Postman: For thorough testing and validation of the API endpoints.
**Uses:**
* Create, Read, Update, and Delete (CRUD) operations for employee data.
* Proper error handling and validation to ensure data integrity.
-Seamless integration with MySQL for persistent storage.
