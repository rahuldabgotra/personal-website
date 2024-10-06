---
title: "Book Loop App"
date: 2024-10-06T23:13:22+05:30
tags: ["Projects"]
cover:
  image: images/projects/Project-Book-Loop-App.png
draft: false
---

## Overview: Problem Statement

In an increasingly connected world, book enthusiasts often seek ways to share their personal libraries while ensuring security and trust within their community. The **Book Loop App** addresses this need by providing a full-stack social platform where users can list, borrow, and return books in a secure environment. Built with Spring Boot and Angular, this application fosters a community-driven approach to book lending, making it easier for users to connect and share their literary collections.

## Features

- **Book Management**: Users can seamlessly list their books, borrow available titles, and return them with an approval workflow.
- **User Authentication**: Secure JWT-based authentication allows users to manage their books within a protected environment, enhancing data privacy.
- **Session Management**: Maintains secure user sessions, ensuring data integrity and user security across the application.
- **CRUD Operations**: Comprehensive management of books through Create, Read, Update, and Delete functionalities.
- **Responsive Design**: The user interface is built with Angular and Bootstrap, ensuring usability across different devices.

## Technologies Used

- **Spring Boot**: The backend framework that powers the application, providing a robust and scalable structure.
- **Angular**: The frontend framework used to create a dynamic and responsive user interface.
- **Docker**: Utilized for containerization, making deployment and environment management easier.
- **JWT (JSON Web Tokens)**: For secure user authentication and session management.
- **MySQL**: The database used for storing user and book information, ensuring efficient data handling.

## Design and Build Process

The development of the **Book Loop App** involved several structured phases to ensure an efficient and effective build:

1. **Initial Planning**: Identified core functionalities—book management, user authentication, and secure borrowing/returning processes—aiming to enhance community interaction among users.

2. **Environment Setup**: Created the necessary environment for both the backend and frontend, ensuring all dependencies were installed for smooth development.

3. **Database Design**: Implemented a MySQL database for effective management of user and book data, allowing for seamless data operations.

4. **User Authentication**: Leveraged JWT for secure user authentication and integrated Keycloak for managing user roles. Challenges included ensuring robust session management.

5. **User Interface Design**: Developed a clean and intuitive UI with Angular and Bootstrap, focusing on user experience and functionality.

6. **Testing and Debugging**: Conducted thorough testing for book management and user authentication, addressing any issues related to data integrity and user sessions.

This structured process facilitated efficient problem-solving and ensured a high-quality product.

## Screenshots/Demonstration

![Book Loop App Screenshot](link-to-screenshot)

<!-- *(Include images or GIFs showcasing the application in use.)* -->

## Installation and Setup Instructions

### Prerequisites

- **Java 21**
- **Node.js (16+)**
- **Angular CLI**
- **Docker**
- **MySQL**

### Backend Setup (Spring Boot: book-loop-api)

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/rahuldabgotra/book-loop-app.git
   cd book-loop-app/book-loop-api
   ```

2. **Configure MySQL Database**:

   - Set up a MySQL database and update `application.properties` with your database details.

3. **Run the Application**:

   ```bash
   ./mvnw spring-boot:run
   ```

4. **API Documentation**:

   - Access Swagger documentation at `http://localhost:8080/swagger-ui.html`.

### Frontend Setup (Angular: book-loop-ui)

1. Navigate to the frontend directory:

   ```bash
   cd ../book-loop-angular
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Run the Angular app:

   ```bash
   ng serve
   ```

   - Access the app at `http://localhost:4200`.

### Docker Setup

To run the full application with Docker:

```bash
docker-compose up
```

## Usage Instructions

Once the app is running:

- **User Registration**: Sign up for a new account to manage your books and borrow from others.
- **Book Management**: Add books to your personal collection, update details, and archive books as needed.
- **Borrowing and Returning**: Browse available books, borrow them, and return them when finished. The owner can approve return requests.

## Future Enhancements

Future enhancements may include:

- **Advanced Search**: Implementing search functionality using Elasticsearch to allow users to find books more efficiently.
- **User Reviews and Ratings**: Enabling users to review and rate books, fostering community interaction and feedback.
- **Notification System**: Adding notifications to alert users about borrowing requests and return approvals.

## Repository Link

For more details and to access the source code, visit the [GitHub Repository](https://github.com/rahuldabgotra/book-loop-app).
