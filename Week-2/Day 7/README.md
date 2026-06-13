# Day 14 - Flow Governance

## Approval Workflow Examples

### 1. Course Creation Approval

**Requestor:** Faculty Member

**Approval Order:**
1. Department Head reviews the course proposal.
2. Academic Committee validates curriculum requirements.
3. Principal approves final course creation.

**After Approval:**
- Course record is created.
- Students can enroll in the course.
- Notification is sent to the faculty member.

**After Rejection:**
- Request is returned with comments.
- Faculty member can modify and resubmit.

---

### 2. Faculty Leave Request

**Requestor:** Faculty Member

**Approval Order:**
1. Head of Department reviews the leave request.
2. HR verifies leave balance.
3. Principal approves if required.

**After Approval:**
- Leave is recorded in the system.
- Timetable adjustments are initiated.

**After Rejection:**
- Faculty member receives a rejection notification.

---

### 3. Student Scholarship Request

**Requestor:** Student

**Approval Order:**
1. Scholarship Committee reviews eligibility.
2. Finance Department verifies funding.
3. Principal provides final approval.

**After Approval:**
- Scholarship is granted.
- Student receives confirmation.

**After Rejection:**
- Student receives rejection reason.

---

### 4. Budget Approval

**Requestor:** Department Head

**Approval Order:**
1. Finance Department reviews the budget.
2. Administrative Officer validates requirements.
3. Principal approves final allocation.

**After Approval:**
- Budget is released.
- Procurement activities can begin.

**After Rejection:**
- Budget request is returned for revision.

---

## Branching Flow Logic

### Attendance Monitoring Flow

**Decision Point 1**
- Is Attendance < 75%?

**If Yes**
- Send warning email to the student.

**Decision Point 2**
- Is Attendance < 60%?

**If Yes**
- Notify parents or guardians.

**Decision Point 3**
- Is Attendance < 50%?

**If Yes**
- Escalate the case to the administration.

### Flow Branches

| Attendance Percentage | Action |
|----------------------|---------|
| 75% or Above | No Action |
| Below 75% | Warning Email |
| Below 60% | Parent Notification |
| Below 50% | Administrative Escalation |

### Benefits

- Early intervention
- Improved student monitoring
- Automated communication
- Consistent policy enforcement

---

## Governance Explanation

Governance is the set of rules, policies, and controls used to manage business processes and data.

### Why Can't Everyone Change Important Records?

### Security
Unauthorized users may access or modify sensitive information.

### Misuse
Users could intentionally or unintentionally make harmful changes.

### Incorrect Approvals
Critical business decisions require proper authorization.

### Business Risk
Incorrect data can lead to financial, legal, or operational problems.

### Compliance
Organizations must follow regulations and maintain audit trails.

### Accountability
Every important action should be traceable to a responsible person.

Good governance ensures systems remain secure, reliable, and compliant.

---

## Reflection

Enterprises require controlled workflows because important business actions can affect finances, operations, compliance, and customer trust.

Unrestricted actions may result in:
- Data corruption
- Unauthorized changes
- Security issues
- Financial losses
- Compliance violations

Controlled workflows provide:
- Approval mechanisms
- Accountability
- Transparency
- Auditability
- Risk reduction

Through this exercise, I learned how approval workflows, branching logic, and governance work together to support secure and efficient enterprise business processes.