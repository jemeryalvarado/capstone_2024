# Perfect Timing

## Overview

**Perfect Timing** is a task management web app designed to assist users, especially those with ADHD, in managing their tasks effectively by using intrusive alarm notifications that take up the screen and can be snoozed. This ensures that important tasks are hard to ignore and receive multiple reminders.

### Problem

People with ADHD often struggle with time management and task completion due to distractions and the inability to focus. Traditional notifications are easily dismissed and thus tasks are forgotten. Traditional task management apps send notifications that can be ignored or missed, leading to uncompleted tasks and increased stress. Perfect Timing addresses this by using screen-filling alarms and persistent reminders to ensure tasks are noticed and acted upon.

### User Profile

**Target Users** :

* Individuals with ADHD or other attention-related challenges.
* Busy professionals who need persistent reminders for tasks.
* Students managing multiple assignments and deadlines.

**Usage** :

* Users will create tasks with specific due dates and times.
* Notifications will appear as full-screen alarms that require user interaction.
* Users can snooze alarms to be reminded again shortly.

**Special Considerations** :

* The app needs to handle interruptions gracefully without being overly disruptive.
* Customizable snooze intervals and alarm tones.
* Accessibility features for users with different needs.

### Features

* **Task Creation** : Users can create tasks with details like title, description, due date, and time.
* **Full-Screen Alarms** : Notifications appear as full-screen alarms that require user interaction to dismiss or snooze.
* **Snooze Functionality** : Users can snooze alarms for custom intervals.
* **Recurring Reminders** : Multiple reminders leading up to the task deadline.
* **Task List** : Overview of all tasks with options to edit, delete, and mark as complete.
* **User Profiles** : Allow users to save their tasks and preferences.
* **Custom Notifications** : Options to customize alarm sounds and snooze intervals.
* Implementation

### Tech Stack

* **Frontend** :
  * React
  * Javascript
  * Sass
* **Backend** :
  * Node.js with Express
  * Knex.js
  * MySQL
  * JWT: For authentication.
* **Libraries** :
  * FullCalendar: For calendar and scheduling features.
  * Axios: For making HTTP requests from the frontend to the backend.

### APIs

* Not exactly sure yet

### Sitemap

1. **Home** : Introduction and login/signup buttons.
2. **Dashboard** : Overview of tasks, calendar view, and quick access to create tasks.
3. **Task Management** : Page to add, edit, and view tasks.
4. **Profile** : User profile settings and preferences.
5. **Notifications** : Settings for alarm tones and snooze intervals.

### Mockups

1. **Home Screen** : Login and sign-up options.
2. **Dashboard** : Calendar view with upcoming tasks.
3. **Task Management** : Form for creating and editing tasks.
4. **Full-Screen Alarm** : Alarm notification taking up the entire screen with options to dismiss or snooze.
5. **Profile Settings** : Options to manage user information and notification preferences.

### Data

* **User** :
  * ID
  * Name
  * Email
  * Password (hashed)
  * Notification Preferences
* **Task** :
  * ID
  * UserID
  * Title
  * Description
  * Due Date
  * Notification Times

### Endpoints

* **POST /signup** : Create a new user.

  * Request: { username, name, password }
  * Response: { success: true }
* **POST /login** : Authenticate a user and return a JWT.

  * Request: { username, password }
  * Response: { token }
* **GET /tasks** : Get all tasks for the logged-in user.

  * Request: Header with JWT
  * Response: { tasks: [ ... ] }
* **POST /tasks** : Create a new task.

  * Request: { title, description, dueDate, notificationTimes }
  * Response: { success: true, task }
* **PUT /tasks/**
  : Update an existing task.

  * Request: { title, description, dueDate, notificationTimes }
  * Response: { success: true, task }
* **DELETE /tasks/**
  : Delete a task.

  * Request: Header with JWT
  * Response: { success: true }

### Auth

Authentication will be implemented using JWT. Users will log in with a username and password to receive a token, which will be required for accessing task management and profile endpoints.

## Roadmap

1. **Week 1** :
   * Set up project structure.
   * Implement user authentication (signup/login).
2. **Week 2** :
   * Develop task creation and management endpoints.
   * Create frontend components for task management.
3. **Week 3** :
   * Implement full-screen alarm notifications.
   * Integrate snooze functionality.
4. **Week 4** :
   * Build user profile and settings page.
   * Test and debug the application.
5. **Week 5** :
   * Final touches and deployment.
   * Write documentation and create user guides.

## Nice-to-haves

* **Mobile App** : Develop a mobile version for iOS and Android.
* **Calendar Integration** : Sync tasks with Google Calendar.
* **Voice Commands** : Add support for voice commands to manage tasks.
* **Analytics** : Track task completion rates and user activity.
* **Advanced Analytics** : Provide detailed insights into task completion rates and patterns
# capstone_2024
