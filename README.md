# MeetSync – Professor–Student Meeting Scheduler

**Synchronizing Students and Professors**

MeetSync is a web-based academic appointment scheduling system designed to simplify and organize consultations between students and professors. It provides a centralized platform for managing professor availability, requesting meetings, handling approvals, preventing scheduling conflicts, and sending automated notifications.

## 📌 Table of Contents

- [Overview](#-overview)
- [Problem Statement](#-problem-statement)
- [Objectives](#-objectives)
- [Key Features](#-key-features)
- [User Roles](#-user-roles)
- [System Workflow](#-system-workflow)
- [Functional Requirements](#-functional-requirements)
- [Non-Functional Requirements](#-non-functional-requirements)
- [Proposed Technology Stack](#-proposed-technology-stack)
- [System Design and Documentation](#-system-design-and-documentation)
- [Development Methodology](#-development-methodology)
- [Future Enhancements](#-future-enhancements)
- [Project Team](#-project-team)

## 📖 Overview

Traditional academic meeting scheduling often relies on emails and informal messages, resulting in communication delays, unclear availability, and scheduling conflicts.

MeetSync aims to replace this manual process with an organized digital solution. Students can view available consultation slots and submit meeting requests, while professors can manage their schedules and respond to requests through a centralized platform.

The system also maintains meeting statuses and provides notifications for important events, including booking requests, approvals, rejections, rescheduling, and cancellations.

## ❗ Problem Statement

The conventional professor–student meeting scheduling process faces several challenges:

- Repeated back-and-forth communication through emails and messages.
- Lack of real-time visibility into professor availability.
- Double bookings and overlapping appointments.
- Delayed responses to meeting requests.
- Missed cancellations and rescheduling updates.
- Manual tracking of appointments and meeting history.
- Additional administrative workload for faculty.

MeetSync addresses these challenges by introducing a centralized, automated appointment management system.

## 🎯 Objectives

- Provide students with access to professor availability.
- Enable professors to create and manage consultation schedules.
- Allow students to request meetings independently.
- Prevent double bookings and scheduling conflicts.
- Support meeting approval, rejection, cancellation, and rescheduling.
- Generate automated notifications for meeting-related events.
- Maintain meeting statuses and historical records.
- Reduce manual communication and administrative effort.
- Provide role-based access for students, professors, and administrators.

## ✨ Key Features

### 📅 Availability Management
- Create and update professor consultation slots.
- Support recurring and one-time availability.
- Define blackout periods when meetings cannot be scheduled.
- Display available slots to students.

### 🤝 Meeting Management
- Submit meeting requests with a selected professor and time slot.
- Validate availability before creating a request.
- Prevent conflicting appointments.
- Accept or reject requests.
- Reschedule existing meetings.
- Cancel eligible appointments.

### 🔔 Automated Notifications
- Notify professors about new meeting requests.
- Inform students about approvals and rejections.
- Send updates for rescheduled and cancelled meetings.
- Maintain notification records.

### 📊 Meeting Tracking
- View current meeting statuses.
- Maintain meeting history.
- Track changes throughout the appointment lifecycle.

### 👤 Profile and Administration
- Support user registration and login.
- Provide profile viewing and updating.
- Support administrative configuration and system reports.
- Include optional payment gateway integration in the expanded system design.

## 👥 User Roles

### 1. Student
Students can:
- Register and log in.
- View and update their profiles.
- Browse professor availability.
- Request meetings.
- View meeting status and history.
- Cancel eligible meetings.
- Receive notifications.

### 2. Professor
Professors can:
- Log in and manage their profiles.
- Set and update availability.
- View incoming meeting requests.
- Accept or reject requests.
- Propose rescheduling.
- View meeting history.
- Receive notifications.

### 3. Administrator
The administrator is responsible for:
- Managing users and supported system settings.
- Configuring system-level options.
- Generating system activity reports.

### 4. External Services
The system design includes a notification system for meeting updates and an optional payment gateway for processing meeting fees.

## 🔄 System Workflow

The main meeting scheduling process follows these steps:

1. **Authentication:** The user registers or logs in.
2. **Availability Search:** The student selects a professor and views available consultation slots.
3. **Meeting Request:** The student selects a suitable slot and submits a request.
4. **Conflict Checking:** The system validates availability and checks for scheduling conflicts.
5. **Professor Action:** The professor accepts, rejects, or requests rescheduling.
6. **Status Update:** The system updates the meeting record.
7. **Notification:** The relevant student and professor receive meeting updates.
8. **Record Maintenance:** The system maintains meeting status and history.

## ⚙️ Functional Requirements

The Software Requirements Specification (SRS) defines the following functional requirements:

| ID | Requirement |
|---|---|
| FR-01 | User Authentication |
| FR-02 | Availability Scheduling |
| FR-03 | Availability Viewing |
| FR-04 | Booking and Conflict Checking |
| FR-05 | Approval Management |
| FR-06 | Meeting Cancellation |
| FR-07 | Meeting Status Tracking |
| FR-08 | Profile Management |
| FR-09 | Automated Notifications |
| FR-10 | Administrative Reporting |
| FR-11 | System Configuration |
| FR-12 | Optional Payment Processing |

## 🛡️ Non-Functional Requirements

The proposed system is designed around the following quality requirements:

- **Performance:** Target sub-second response times for availability browsing and booking confirmations.
- **Security:** Use password hashing with bcrypt, JWT-based session authentication, and role-based authorization.
- **Reliability:** Target 99.5% uptime during operational office and examination weeks.
- **Usability:** Provide a responsive interface for desktops, tablets, and smartphones.
- **Data Integrity:** Use ACID-compliant database transactions to prevent inconsistent meeting states and duplicate confirmations.
- **Maintainability:** Organize the system into separate functional components that can be developed and tested incrementally.

These are documented system targets and requirements, not claims of measured production performance.

## 🧰 Proposed Technology Stack

The project report identifies the following technologies for the proposed implementation:

| Technology | Purpose |
|---|---|
| React | Frontend user interface |
| Node.js | Backend application services |
| PostgreSQL | Relational database |
| bcrypt | Password hashing |
| JWT | Authentication and session tokens |

The final technology stack may be updated to reflect the tools actually used during implementation.

## 🏗️ System Design and Documentation

The project follows a structured Software Engineering approach, with documentation covering the following artifacts:

### 1. Project Selection Phase
- Software bid and project title.
- Problem statement and proposed solution.
- Project objectives.
- SDLC model selection and justification.
- Project overview.

### 2. Analysis Phase
- **Use-Case Diagrams:** Interactions between students, professors, administrators, and external services.
- **Use-Case Templates:** Detailed flows, preconditions, alternative flows, and postconditions.
- **Activity Diagram:** Overall meeting scheduling workflow.
- **Swimlane Diagram:** Responsibilities of the student, system, professor, and notification system.
- **Data Flow Diagrams (DFDs):** Context-level and detailed representations of system data flows.
- **Software Requirements Specification (SRS):** Functional requirements, non-functional requirements, interfaces, constraints, and feasibility study.
- **User Stories and Story Cards:** User needs, priorities, preconditions, and acceptance criteria.

### 3. Data Flow Diagram Levels
- **Level 0:** Represents the overall system and its interactions with external entities.
- **Level 1:** Decomposes the system into authentication and profile management, faculty availability management, meeting scheduling, and notification management.
- **Level 2:** Provides further decomposition of authentication, meeting management, availability management, and notification processes.

These artifacts establish the documented requirements and design of MeetSync.

## 🔁 Development Methodology

**Selected SDLC Model: Agile Scrum**

Agile Scrum is selected because the project can be developed incrementally, with features refined through feedback and continuous testing.

The proposed development process divides the system into manageable modules:

1. Authentication and profile management.
2. Professor availability management.
3. Meeting requests and scheduling.
4. Meeting approvals and rescheduling.
5. Notifications and meeting history.
6. Administrative functions and reporting.

This approach supports incremental delivery, early testing, risk identification, and continuous improvement.

## 🚀 Future Enhancements

Potential extensions to the documented system include:

- Calendar integration for easier appointment management.
- Email or push notifications.
- Automated meeting reminders.
- Search and filtering by professor or consultation availability.
- Meeting analytics and usage reports.
- Video conferencing integration.
- Enhanced scheduling preferences and recurring appointment management.

These are potential enhancements and may be considered as the project evolves.

## 👨‍💻 Project Team

Developed as part of the **UCS503 – Software Engineering Lab** project at Thapar Institute of Engineering & Technology (TIET), Patiala.

| Team Member | Student ID |
|---|---|
| Yogesh Goyal | 1024031015 |
| Rakshit Chaudhary | 1024031011 |
| Tanish Kumar Singla | 1024030759 |

**Submitted to:** Stuti Chugh

**Department:** Computer Science and Engineering

---

⭐ If you find this project interesting, consider starring the repository!

**MeetSync — Making academic consultations simpler, smarter, and more organized.**
