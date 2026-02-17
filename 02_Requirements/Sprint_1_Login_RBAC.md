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
- WebLoanAppFunctionalDesign_Loan…
- Username field is mandatory 
- WebLoanAppFunctionalDesign_Loan…
- Password field is mandatory 
- WebLoanAppFunctionalDesign_Loan…

Session is created upon login
Logout ends session

**US-2: Login – Validation Handling**
As a user
I want proper validation messages
So that I understand why login failed

**Acceptance Criteria**
- Empty Branch → “Please fill out this field.” 
- WebLoanAppFunctionalDesign_Loan…
- Empty Username → “Please fill out this field.” 
- WebLoanAppFunctionalDesign_Loan…
- Empty Password → “Please fill out this field.” 
- WebLoanAppFunctionalDesign_Loan…
- Invalid Branch → “Branch does not exist” 
- WebLoanAppFunctionalDesign_Loan…
- Invalid Username/Password → “Invalid user name or password” 
- WebLoanAppFunctionalDesign_Loan…

**US-3: Role-Based Access – Branch Admin**
As a Branch Admin
I want full system access
So that I can manage users and operations
**Acceptance Criteria**
Branch Admin can access:
- Users Page WebLoanAppFunctionalDesign_Loan…
- Customers Page WebLoanAppFunctionalDesign_Loan…
- Loans Page WebLoanAppFunctionalDesign_Loan…
- Events Page WebLoanAppFunctionalDesign_Loan…
- Policies Page WebLoanAppFunctionalDesign_Loan…

**US-4: Role-Based Access – Loan Manager**
As a Loan Manager
I want restricted user creation privileges
So that governance is maintained
**Acceptance Criteria**
Loan Manager:
- Cannot add new users WebLoanAppFunctionalDesign_Loan…
- Can manage customers
- Can manage loans
- Can view events

**US-5: Role-Based Access – Loan Officer**
As a Loan Officer
I want limited privileges
So that I only access operational areas
**Acceptance Criteria**
Loan Officer:
- Cannot add users WebLoanAppFunctionalDesign_Loan…
- Cannot view events WebLoanAppFunctionalDesign_Loan…
- Can manage customers
- Can manage loans

**Definition of Done (Sprint 1)**
All login test cases executed
RBAC matrix validated
Critical/High defects resolved
Regression of authentication completed
Automation added for valid login & invalid login
