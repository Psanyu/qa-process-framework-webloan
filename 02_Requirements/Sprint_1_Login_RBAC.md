**Sprint 1 – Authentication & RBAC**
**Sprint Goal**
Validate secure login functionality and enforce role-based access control (RBAC) across major navigation components.

**User Stories**
**US-1:** Login – Successful Authentication
As a branch user
I want to log in with valid credentials
So that I can access the dashboard

**Acceptance Criteria**
- Branch field is mandatory 
- Username field is mandatory 
- Password field is mandatory 

Session is created upon login
Logout ends session

**US-2: Login – Validation Handling**
As a user
I want proper validation messages
So that I understand why login failed

**Acceptance Criteria**
- Empty Branch → “Please fill out this field.” 
- Empty Username → “Please fill out this field.” 
- Empty Password → “Please fill out this field.” 
- Invalid Branch → “Branch does not exist” 
- Invalid Username/Password → “Invalid user name or password” 

**US-3: Role-Based Access – Branch Admin**
As a Branch Admin
I want full system access
So that I can manage users and operations
**Acceptance Criteria**
Branch Admin can access:
- Users Page 
- Customers Page 
- Loans Page 
- Events Page 
- Policies Page 

**US-4: Role-Based Access – Loan Manager**
As a Loan Manager
I want restricted user creation privileges
So that governance is maintained
**Acceptance Criteria**
Loan Manager:
- Cannot add new users 
- Can manage customers
- Can manage loans
- Can view events

**US-5: Role-Based Access – Loan Officer**
As a Loan Officer
I want limited privileges
So that I only access operational areas
**Acceptance Criteria**
Loan Officer:
- Cannot add users 
- Cannot view events 
- Can manage customers
- Can manage loans

**Definition of Done (Sprint 1)**
- All login test cases executed
- Critical/High defects resolved
- Regression of authentication completed
- Automation added for valid login & invalid login

**RBAC matrix validated**
## RBAC Access Matrix

| Module      | Branch Admin | Loan Manager | Loan Officer |
|-------------|--------------|--------------|--------------|
| Users       | Full Access  | View/Edit    | No Access    |
| Customers   | Full Access  | Full Access  | Full Access  |
| Loans       | Full Access  | Full Access  | Full Access  |
| Events      | Full Access  | View         | No Access    |
| Policies    | Full Access  | View         | View         |


