**✅ Sprint 2 – User & Customer Management**
**Sprint Goal**
- Validate creation, modification, search, and pagination functionality for Users and Customers modules.

**User Stories**
**US-1:** Add User (Positive Flow)
As a Branch Admin
I want to add a new user
So that system access can be provisioned
**Acceptance Criteria**
- Username is mandatory
- First Name is mandatory
- Last Name is mandatory
- Email format must be valid
- User role must be selected
- User is saved successfully
- User appears in Users list

**US-2:** Add User – Validation Handling
As a Branch Admin
I want validation messages
So that invalid data is prevented
**Acceptance Criteria**
- Duplicate username → “Username already exists”
- Invalid email → “Invalid email format”
- Empty mandatory fields → Proper validation message
- Role not selected → Validation message

**US-3:** Search & Pagination – Users
As a system user
I want to search and filter users
So that I can quickly find specific records
**Acceptance Criteria**
- Search by Username
- Search by First Name
- Search by Last Name
- Per Page toggle works (5 / 10 / All)
- Results update dynamically

**US-4: **Add Customer (Positive Flow)
As a Loan Manager
I want to add customers
So that loans can be processed
**Acceptance Criteria**
- Account # numeric (max 7 digits)
- Province required
- Phone format validated
- Email format validated
- Customer appears in Customers list

**US-5:** Customer Validation Handling
As a Loan Officer
I want validation messages
So that incorrect data is rejected
**Acceptance Criteria**
- Blank Account # → “Account # required”
- Non-numeric Account # → “Must be numeric”
- Invalid phone format → Warning
- Invalid email → Warning

**Definition of Done (Sprint 2)**
- All User & Customer test cases executed
- High/Critical defects resolved
- Search & pagination validated
- Regression suite updated
- Automation added for Add User & Add Customer
