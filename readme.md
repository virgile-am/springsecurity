# Table of Contents
- [Technologies Used](#technologies-used)
- [Features](#features)
- [Getting Started](#getting-started)
    - [Prerequisites](#prerequisites)
    - [Installation](#installation)
- [Usage](#usage)


## Technologies Used
- **Java 21**: Programming language used for the application.
- **Spring Boot 3.3.2**: Framework for building the application.
- **Spring Security**: Provides authentication and authorization features.
- **Thymeleaf**: Templating engine for rendering views.
- **Maven 3.8**: Build automation tool for dependency management and project build.

## Features
- **In-Memory User Management**: Includes predefined users with roles (user and admin).
- **Basic Authentication**: Configured with form-based and HTTP Basic Authentication.
- **Role-Based Access Control**: Protects different URLs based on user roles.
- **Custom Login and Logout Pages**: Provides custom endpoints for user authentication and session management.

## Getting Started

### Prerequisites
- Java 21 or later
- Maven 3.8 or later

### Installation
1. Clone the repository:
   ```
   git clone https://github.com/virgile-am/springsecurity.git
   ```
2. Navigate to the project directory:
   ```
   cd springsecurity
   ```
3. Install the required dependencies:
   ```
   mvn install
   ```
4. Start the application:
   ```
   mvn spring-boot:run
   ```
5. Open your web browser and go to `http://localhost:8080` to access the application.

## Usage

### Accessing the Application

* Home Page: http://localhost:8080/
* Login Page: http://localhost:8080/login
* User Page: http://localhost:8080/user (Accessible only for users with USER role)
* Admin Page: http://localhost:8080/admin (Accessible only for users with ADMIN role)

### Credentials

* **User Login:**
    * Username: *`user`*
    * Password: `password`
* **Admin Login:**
    * Username: *`admin`*
    * Password: `admin`

### Configuration

#### Controllers

* **HomeController**: Manages requests to the home and login pages.
    * Path: *`/`* and *`/login`*
    * View Templates: `home.html` and `login.html`
* **UserController**: Manages requests to user-specific pages.
    * Path: *`/user`*
    * View Template: `user.html`
* **AdminController**: Manages requests to admin-specific pages.
    * Path: *`/admin`*
    * View Template: `admin.html`