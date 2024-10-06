---
title: "Flask Task Manager App"
date: 2024-03-27T23:13:22+05:30
tags: ["Projects"]
cover:
  image: images/projects/Project-Flask-Task-Manager-App.png
draft: false
---

## Overview: Problem Statement

In today's fast-paced world, effective task management is essential for enhancing productivity in both personal and professional environments. Many existing task management solutions tend to be cumbersome or lack key functionalities, making them less effective for users. The **Flask Task Manager App** addresses this issue by offering a streamlined and intuitive interface for users to create, update, and manage their tasks efficiently, while ensuring secure user authentication through JWT (JSON Web Tokens).

## Features

- **Task CRUD Operations**: Users can seamlessly create, read, update, and delete tasks with a few clicks.
- **User Authentication**: Secure JWT-based authentication allows users to manage their tasks within a protected environment, enhancing data privacy.
- **Session Management**: Maintains secure user sessions, ensuring data integrity and user security across the application.
- **Real-time Logging**: The app features real-time logging capabilities, providing insights for debugging and monitoring task management activities.
- **Responsive Design**: The user interface is designed to be responsive, ensuring usability across different devices.

## Technologies Used

- **Flask**: The backend framework that offers a lightweight and flexible structure for web applications.
- **SQLite**: A serverless database used for storing user and task information, providing an easy setup for local development.
- **JWT (JSON Web Tokens)**: Implements secure user authentication and session management.
- **Python**: The primary programming language employed for backend development.
- **HTML/CSS/JavaScript**: Utilized for building the front-end interface, enhancing user interaction.

## Design and Build Process

The development of the **Flask Task Manager App** followed a methodical approach, emphasizing functionality, usability, and security:

1. **Initial Planning**: Identified core features—task management and secure user authentication—prioritizing usability and simplicity for a positive user experience.

2. **Environment Setup**: Created a virtual environment for the project, ensuring a clean workspace. Early installation of dependencies facilitated streamlined development.

3. **Database Design**: Chose SQLite for its simplicity and ease of integration, allowing effective management of user and task data without complex configurations.

4. **User Authentication**: Implemented JWT for secure user authentication. A significant challenge was ensuring robust session management, which was addressed by carefully validating tokens across user sessions.

5. **User Interface Design**: Focused on a clean and intuitive UI for task management actions. User feedback was invaluable in refining the design to balance simplicity and functionality.

6. **Testing and Debugging**: Conducted thorough testing for task creation, updates, and session security. Addressed minor issues related to session handling by optimizing token management and database queries.

This structured process facilitated efficient problem-solving and allowed for continuous improvement.

## Screenshots/Demonstration

![Task Manager App Screenshot](link-to-screenshot)

<!-- *(Include images or GIFs showcasing the application in use.)* -->

## Installation and Setup Instructions

### Prerequisites

- **Python 3.7+**
- **Flask**
- **SQLite**

### Set Up the Virtual Environment

1. **Create a Virtual Environment**:

   ```bash
   py -3 -m venv .venv
   ```

2. **Activate the Virtual Environment**:
   - For Windows:

     ```bash
     .venv\Scripts\activate
     ```

   - For Mac/Linux:

     ```bash
     source .venv/bin/activate
     ```

3. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

### Run the Application

To start the Flask application:

```bash
python app.py
```

The app will be available at `http://127.0.0.1:5000`.

## Usage Instructions

Once the app is running:

- **Home Page**: Access the task manager interface to add, edit, or delete tasks.
- **User Authentication**: Register or log in to manage personal tasks, with JWT tokens ensuring secure sessions.
- **Task Management**: Create new tasks, mark them as completed, or delete tasks that are no longer needed.

## Future Enhancements

Future enhancements may include:

- **Task Prioritization**: Implementing a priority system to categorize tasks based on urgency.
- **Due Dates**: Allowing users to set due dates for tasks, enhancing time management capabilities.
- **Notifications**: Integrating notifications to remind users of upcoming deadlines.

## Repository Link

For more details and to access the source code, visit the [GitHub Repository](https://github.com/rahuldabgotra/learn/tree/main/python/projects/flask-task-manager-app).
