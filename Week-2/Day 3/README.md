# Day 10 - College Management Mini Project

## System Overview

The College Management System is a Salesforce-based application designed to manage students, faculty, courses, and departments efficiently. The system integrates CRM concepts, automation, Apex logic, and Lightning Web Components to provide a complete enterprise application experience.

---

## CRM Concepts

The project is built around the following CRM entities:

### Student
- Student Registration
- Attendance Tracking
- Course Enrollment

### Faculty
- Course Management
- Student Monitoring
- Notifications

### Course
- Course Information
- Seat Availability
- Enrollment Management

### Department
- Department Details
- Faculty Assignment
- Course Allocation

---

## Data Model

### Objects
- Student (Custom Object)
- Faculty (Custom Object)
- Course (Custom Object)
- Department (Custom Object)

### Relationships
- Department → Faculty (One-to-Many)
- Department → Course (One-to-Many)
- Course → Student (One-to-Many)

### Important Fields
- Student Name
- Student Email
- Attendance Percentage
- Course Name
- Total Seats
- Available Seats
- Department Name

---

## Validation Rules

To maintain data quality, the following validations are implemented:

- Student Email is mandatory.
- Course seat limit cannot be exceeded.
- Attendance percentage must be between 0 and 100.
- Required fields cannot be left blank.
- Duplicate registrations are prevented.

---

## Flows

Salesforce Flows automate business processes:

### Registration Flow
- Automatically processes student registrations.

### Confirmation Flow
- Sends confirmation notifications after successful registration.

### Attendance Flow
- Generates alerts for low attendance.

### Seat Availability Flow
- Updates remaining seat count automatically.

---

## Apex Logic

Apex is used for advanced business requirements.

### Features
- Student eligibility calculation.
- Bulk student registration processing.
- Course seat validation.
- Custom business rule implementation.
- Backend processing for complex operations.

---

## Complete Data Flow

1. Student opens the Registration Screen.
2. Student submits course registration.
3. Validation Rules verify entered data.
4. Salesforce Flow processes the registration.
5. Apex Logic performs custom validations.
6. Trigger executes required backend actions.
7. Data is stored in Salesforce objects.
8. Notifications are sent to students and faculty.
9. Updated information is displayed on dashboards.

### Flow Summary

```text
Student
   ↓
LWC Registration Screen
   ↓
Validation Rules
   ↓
Flow Automation
   ↓
Apex Logic
   ↓
Trigger Execution
   ↓
Database Storage
   ↓
Notification
   ↓
Dashboard Update
```

---

## Reflection

This mini project helped me understand how multiple Salesforce technologies work together to build a real-world enterprise application. I learned how CRM concepts, data modeling, validation rules, Flows, Apex, Triggers, and Lightning Web Components integrate into a complete system. The project also improved my understanding of application architecture, automation, and data flow within Salesforce.

---

## Technologies Used

- Salesforce CRM
- Lightning Web Components (LWC)
- Apex
- SOQL
- Triggers
- Validation Rules
- Flow Builder
- Salesforce Objects & Relationships
- Lightning App Builder