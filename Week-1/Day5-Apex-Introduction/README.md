# Day 5 - Apex Introduction

# 1. What is Apex?

Apex is Salesforce’s object-oriented programming language used to implement custom business logic on the Salesforce platform. While Salesforce provides many no-code automation tools like Flow Builder, some business requirements become too complex for configuration alone. In such cases, Apex is used to build scalable, flexible, and powerful solutions.

Apex allows developers to interact with Salesforce data, automate backend processes, integrate with external systems, perform complex validations, and implement advanced business rules.

It is similar to Java in syntax and is designed specifically for the Salesforce ecosystem.

## Key Features of Apex

- Object-oriented programming language
- Strongly typed language
- Runs on the Salesforce platform
- Supports database operations (SOQL, SOSL, DML)
- Can create custom automation and triggers
- Supports API integrations
- Handles complex business logic
- Works with asynchronous processing

---

# 2. Difference Between Flow vs Apex

## Flow vs Apex

| Feature | Flow | Apex |
|--------|------|------|
| Type | No-code / Low-code automation | Programming-based automation |
| Development Style | Drag-and-drop interface | Written using code |
| Complexity Handling | Best for simple to medium logic | Best for advanced complex logic |
| User Friendliness | Easy for admins | Requires programming knowledge |
| Performance Control | Limited | High control and customization |
| Integration Capability | Basic | Advanced API integrations |
| Error Handling | Limited | Powerful exception handling |
| Reusability | Moderate | High |

### Example

**Flow Example:**  
Automatically send a welcome email when a student record is created.

**Apex Example:**  
Validate student eligibility, calculate scholarship percentage, check course seat allocation, and integrate with an external payment system.

---

## Configuration vs Coding

| Configuration | Coding |
|--------------|--------|
| Uses clicks instead of code | Requires programming |
| Faster for simple requirements | Better for complex requirements |
| Easy to maintain for admins | Requires developer expertise |
| Limited flexibility | Highly flexible |
| Best for standard automation | Best for custom business logic |

### Example

**Configuration:** Creating a validation rule for required student email.

**Coding:** Creating a custom scholarship eligibility engine.

---

# 3. Real Examples Where Apex Is Needed

## 1. Scholarship Eligibility Calculation

A college wants to automatically determine scholarship eligibility based on:

- Student academic percentage
- Family income
- Category reservation rules
- Special scholarship programs

This logic involves multiple conditions and calculations, making Apex the right choice.

---

## 2. Payment Gateway Integration

When students pay tuition fees, Salesforce needs to connect with an external payment gateway.

Apex can:

- Send payment requests
- Receive API responses
- Update payment status
- Handle payment failures

---

## 3. Automatic Seat Allocation System

When many students apply simultaneously:

- Check course availability
- Reserve seats
- Prevent duplicate allocation
- Handle concurrency issues

Such advanced backend processing requires Apex.

---

# 4. Integrated System Design – College Management System

## CRM in the System

CRM helps manage student interactions, communication, admissions, academic records, and administrative workflows.

Example:
- Student inquiries
- Admission follow-ups
- Fee reminders
- Course communication
- Parent notifications

---

## Objects Used

| Object Name | Purpose |
|------------|---------|
| Student__c | Stores student details |
| Course__c | Stores course information |
| Faculty__c | Stores faculty details |
| Enrollment__c | Links students and courses |
| Fee_Payment__c | Stores payment transactions |
| Attendance__c | Stores attendance records |

---

## Relationships

| Relationship | Type |
|-------------|------|
| Student → Enrollment | One-to-Many |
| Course → Enrollment | One-to-Many |
| Faculty → Course | One-to-Many |
| Student → Fee Payment | One-to-Many |
| Student → Attendance | One-to-Many |

---

## Validation Rules

Validation ensures accurate data entry.

Examples:

- Student email must not be blank
- Phone number must contain valid digits
- Fee amount cannot be negative
- Course capacity cannot exceed limit
- Attendance percentage must remain between 0–100

---

## Flow Usage

Flow Builder handles standard automation.

Examples:

- Send admission confirmation email
- Notify faculty about new enrollments
- Send fee due reminders
- Update attendance alerts
- Create onboarding tasks

---

## Apex Usage

Apex handles advanced backend logic.

Examples:

- Scholarship eligibility calculation
- Seat allocation engine
- Payment gateway integration
- Bulk student processing
- Complex approval workflows

---

# 5. Pseudocode Examples

## Scholarship Eligibility Logic

```text
IF student percentage > 85
   AND family income < 300000
THEN
   scholarship = 50%
ELSE
   scholarship = 0%
END
```

---

## Automatic Seat Allocation Logic

```text
IF available seats > 0
   THEN assign seat
   reduce seat count by 1
ELSE
   add student to waiting list
END
```

---

## Fee Payment Verification Logic

```text
IF payment successful
   update fee status = Paid
   send confirmation email
ELSE
   mark payment as Failed
   notify finance team
END
```

---

# 6. Reflection – Why Enterprise Systems Eventually Need Programming

Enterprise systems initially start with configuration-based solutions because they are faster to build and easier to maintain. However, as business requirements grow, standard tools often become insufficient.

Organizations eventually need programming because:

- Business logic becomes more complex
- External system integrations become necessary
- High-volume data processing requires better control
- Custom workflows exceed no-code capabilities
- Advanced security and exception handling are required

In a college management system, simple admission automation can be handled with Flow, but features like scholarship engines, payment integrations, and bulk academic processing require Apex.

This demonstrates why enterprise applications eventually move beyond configuration into programming-based customization.

---

# Conclusion

Apex is an essential part of Salesforce development for handling advanced business requirements that configuration tools alone cannot solve. A balanced combination of CRM design, objects, validation, flows, and Apex helps build scalable enterprise-grade systems efficiently.