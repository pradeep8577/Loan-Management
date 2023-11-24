# Loan Management System (Web Application)

The Loan Management System is a web application that aims to solve the problems of traditional loan application systems by 
providing a user-friendly platform for users to apply for loans, view their loan details, and make EMI payments. Additionally, 
the system includes an admin module for loan officers to approve user loan applications efficiently.

## Features

- User Registration and Authentication: Users can create an account and log in to access the loan application and other features.
- Loan Application: Users can apply for loans by providing necessary details and documents.
- Loan List: Users can view a list of their active loans and their respective details.
- EMI Payment: Users can make EMI payments using various payment methods.
- Admin Module: Loan officers with admin credentials can approve or reject user loan applications.

## Project Setup Steps

To set up the Loan Management System project, follow these steps:

### Prerequisites

- Java JDK 11 or higher installed on your system
- Apache Maven installed
- MySQL or any other compatible database system

### Step 1: Clone the Repository

Clone the project repository from GitHub to your local machine using the following command:

```
git clone https://github.com/pradeep8577/Loan_Application_System.git
```

### Step 3: Import the Project

Open your java editor, import the project file using option import maven project.

### Step 2: Configure Database

1. Create a MySQL database with the name "loanapp".

  ```
   CREATE DATABASE loanapp;
   USE loanapp;
  ```
   
3. Open the "application.properties" file located in `src/main/resources`.
4. Update the database connection properties, such as `spring.datasource.username` and `spring.datasource.password`, with your MySQL credentials.

```
#Configure database - mysql
spring.datasource.url=jdbc:mysql://localhost:3306/loanapp?useSSL=false&serverTimeZone=UTC&useLegacyDatetimeCode=false
spring.datasource.username=root
spring.datasource.password=root

#configuration
spring.jpa.properties.hibernate.dialect= org.hibernate.dialect.MySQL5InnoDBDialect
#Hibernate auto ddl
spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
logging.level.org.hibernate.SQL=DEBUG
logging.level.org.hibernate.type.descriptor.sql=trace

```

### Step 4: Run the Application

Run the Spring Boot application using run command run as springboot project.


The application will start, and you can access it at `http://localhost:8080`.

### Step 5: Access Admin Module

To access the admin module, create an admin account in the database. You can do this manually using MySQL queries or create an API endpoint to register an admin user.


```
-- ----------------------------------------------------------------------
-- To insert one admin into the admin table based on the schema you provided
-- ----------------------------------------------------------------------  
INSERT INTO `loanapp`.`admin` (`admin_id`, `a_email`, `a_password`, `fname`, `lname`)
VALUES ('admin123', 'admin@example.com', 'adminpassword', 'John', 'Doe');
```

### Step 6: Start Using the Application

1. Register as a user through the application's registration page.
2. Log in with your credentials.
3. Apply for a loan by providing the required details and documents.
4. Use the loan list to track your active loans and their details.
5. Make EMI payments through the payment gateway integration.

As an admin, you can log in using the admin credentials and approve/reject user loan applications.

```
   email : admin@example.com
   password : adminpassword
```

## Technologies Used

- Spring Boot: Java-based framework for building web applications.
- MySQL: Database to store application data.
- Maven: Dependency management and build tool.
