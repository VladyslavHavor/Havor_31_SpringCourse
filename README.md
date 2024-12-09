# Havor_31_SpringCourse

## Overview
This system provides tools for monitoring and recording attendance in lectures and lab sessions in educational institutions. It facilitates interaction between administrators, instructors, and students by offering registration, attendance tracking, and reporting features.


## Functional Requirements
1. Registration, Authorization, and Authentication
   
- Users can register as either students or teachers by providing personal information (name, email, password).
- Login functionality is available using an email and password.
- Role-based access control (student, teacher).

2. User Management
- Students can view their enrolled courses, lectures, and attendance.
- Teachers can add lectures, lab sessions, and manage students' attendance.

3. Course Management
- Teachers can create, view, and edit course information.
- Courses can include lectures and lab sessions.

4. Attendance Logging
- Record attendance statuses for students during lectures and lab sessions.
- Store all attendance data securely for reporting.

5. Notifications
- Ability to send messages to students and teachers regarding important events (e.g., schedule changes).

6. Reporting
- Teachers can generate attendance reports for students for each course.
Reports include information about the number of attended and missed sessions for each student.

7. Configuration
- Personalized settings for courses and instructors (e.g., scheduling and customization).

## REST API endpoints
**Authentication:**
POST /api/auth/register: Register a new user.
POST /api/auth/login: Log in to the system.
POST /api/auth/logout: Log out from the system.

**User Management:**
GET /api/users: Retrieve a list of all users (admin only).
GET /api/users/{id}: Get details of a specific user.
POST /api/users: Create a new user (admin only).
PUT /api/users/{id}: Update user details.
DELETE /api/users/{id}: Delete a user (admin only).

**Course Management:**
GET /api/subjects: Retrieve all courses.
GET /api/subjects/{id}: Get details of a specific course.
POST /api/subjects: Create a new course (teacher only).
PUT /api/subjects/{id}: Update course details (teacher only).
DELETE /api/subjects/{id}: Delete a course.

**Attendance Log:**
POST /api/attendance/lectures: Add attendance records for lectures (teacher only).
POST /api/attendance/labs: Add attendance records for lab sessions (teacher only).
GET /api/attendance/{courseId}/students: Get attendance details for students in a course.

**Messaging**
POST /api/messages/students: Send a message to students (admin or teacher).
POST /api/messages/teachers: Send a message to teachers (admin or teacher).

**Reports**
GET /api/reports/{courseId}/attendance: Generate attendance reports for students in a course (teacher only).

## Implemented Features in Our Project
Completed Features:
Registration for teachers and students via REST API.
CRUD operations for managing courses (subjects) by teachers.
Creation of lecture and lab session schedules.
Attendance tracking for students during lectures and labs.
Basic frontend for:
Students to view their attendance.
Teachers to manage courses, lectures, and student attendance.
H2 in-memory database for storing system data.
Pending Features:
Notification system to send messages to students and teachers.
Detailed reporting (attendance reports for download or export).

## Database 
[My ERD diagram](https://github.com/VladyslavHavor/Havor_21_SpringCourse/blob/main/ERD.png)

