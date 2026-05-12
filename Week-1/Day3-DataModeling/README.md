# Day 3 - Salesforce Data Modeling

## Overview

As part of this learning activity, I explored the core concepts of Salesforce Data Modeling and understood how structured data forms the foundation of enterprise applications. Effective data modeling helps organizations manage information efficiently, maintain data integrity, and support automation-driven business processes.

For this exercise, I designed a **College Admission Management System** to apply Salesforce data modeling concepts in a practical, real-world context.

---

## 1. Difference Between App, Object, Record, and Field

Understanding the hierarchy of Salesforce components is essential for designing scalable applications.

| Component | Description | Example |
|----------|-------------|---------|
| **App** | A collection of related tools, objects, tabs, and functionalities created for a specific business purpose | College Admission Management App |
| **Object** | A database structure used to store related information | Student Object |
| **Record** | A single entry within an object | One student’s admission details |
| **Field** | A specific attribute that stores individual data within a record | Name, Email, Admission Status |

### Practical Understanding

To simplify:

- **App** → Complete business system
- **Object** → Data table
- **Record** → Single row of data
- **Field** → Individual column within the table

### Example Scenario

In a college admission system:

- **App:** College Admission Management
- **Object:** Student
- **Record:** A specific student’s profile
- **Field:** Student Name, Course, Contact Number

---

## 2. Standard vs Custom Objects

Salesforce provides built-in standard objects for common CRM use cases, while custom objects are created to meet organization-specific requirements.

| Standard Objects | Custom Objects |
|-----------------|----------------|
| Predefined by Salesforce | Created by administrators/developers |
| Designed for common CRM processes | Designed for custom business requirements |
| Limited structural modifications | Fully customizable |
| Examples: Account, Contact, Lead, Opportunity | Examples: Student__c, Course__c, Admission__c |

### Standard Object Example

**Contact**

Stores information related to individuals such as:

- Full Name
- Email Address
- Phone Number
- Organization Details

### Custom Object Example

**Student__c**

Designed specifically for the college system to manage:

- Student Information
- Admission Status
- Academic Details
- Course Allocation

---

## 3. College Data Model

### System Name

**College Admission Management System**

This system is designed to streamline student admissions, academic course management, faculty allocation, and payment tracking.

---

### Objects Included

| Object Name | Purpose |
|-----------|---------|
| Student | Stores student profile and admission details |
| Course | Stores academic course information |
| Faculty | Stores faculty member details |
| Admission | Tracks student admission records |
| Fee Payment | Maintains fee transaction details |

---

### Object Relationships

| Parent Object | Child Object | Relationship |
|--------------|--------------|-------------|
| Course | Student | One-to-Many |
| Student | Admission | One-to-Many |
| Student | Fee Payment | One-to-Many |
| Faculty | Course | One-to-Many |

---

### Data Model Representation

```text
Faculty
   │
   └── teaches multiple Courses
           │
           ▼
        Course
           │
           └── enrolled by multiple Students
                    │
                    ▼
                 Student
                 /      \
                /        \
               ▼          ▼
        Admission      Fee Payment
```

If using a visual diagram:

```markdown
![College Data Model](images/college-data-model.png)
```

---

## 4. Formula Fields

### Definition

Formula Fields in Salesforce are custom fields that automatically calculate values based on other field data. These fields help eliminate manual calculations and improve data accuracy.

---

### Example 1: Student Full Name

**Formula**

```text
First_Name__c & " " & Last_Name__c
```

**Explanation**

Automatically combines the student’s first and last name into a single display field.

Example Output:

```text
Sruthi Konchada
```

---

### Example 2: Available Course Seats

**Formula**

```text
Total_Seats__c - Filled_Seats__c
```

**Explanation**

Calculates the number of remaining seats available in a course.

Example:

- Total Seats: 60
- Filled Seats: 45

Output:

```text
15
```

---

### Example 3: Academic Percentage

**Formula**

```text
(Obtained_Marks__c / Total_Marks__c) * 100
```

**Explanation**

Calculates the student’s academic percentage automatically.

Example Output:

```text
90%
```

---

## 5. Validation Rules

### Definition

Validation Rules enforce business logic by preventing invalid or incomplete data from being saved into the system. This ensures data consistency and reliability.

---

### Example 1: Minimum Age Validation

**Formula**

```text
Age__c < 17
```

**Error Message**

```text
Student must be at least 17 years old for admission.
```

**Purpose**

Ensures only eligible students can apply for admission.

---

### Example 2: Percentage Validation

**Formula**

```text
Percentage__c > 100
```

**Error Message**

```text
Percentage cannot exceed 100.
```

**Purpose**

Prevents invalid academic percentage values.

---

### Example 3: Mobile Number Validation

**Formula**

```text
LEN(Mobile_Number__c) <> 10
```

**Error Message**

```text
Mobile number must contain exactly 10 digits.
```

**Purpose**

Ensures correct contact information is entered.

---

## 6. Reflection: Why Structured Enterprise Data Matters

Structured enterprise data is essential for building scalable and reliable business applications.

Well-organized data enables organizations to:

- Maintain consistency across departments
- Improve reporting accuracy
- Support workflow automation
- Minimize duplicate or incorrect records
- Enable faster decision-making
- Improve operational efficiency

In the context of a college admission system, structured data ensures that student records, course allocations, admission workflows, and payment details remain properly connected and easy to manage.

This exercise provided practical insight into how Salesforce data architecture supports real-world enterprise solutions.

---

## Conclusion

This activity strengthened my understanding of Salesforce data modeling concepts, including objects, relationships, formula fields, and validation rules. Designing a practical college management system helped bridge theoretical concepts with real-world implementation.