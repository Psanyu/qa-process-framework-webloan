**✅ Sprint 3 – Customers**
**Sprint Goal**
Deliver full functionality for Customers module including validations and search.

**User Stories**
**US-1:** View Customers List
As a system user
I want to view customers
So that I can manage loan applicants
**Acceptance Criteria**
- Customers page loads
- Columns visible: Account #, Name, Address, Phone, Email, Edit button per row, Delete button per row

**US-2: Add Customer – Valid Data**
As a Loan Manager
I want to add customers
So that loans can be processed
**Acceptance Criteria**
- Account # numeric (max 7 digits)
- Province required
- Phone format validated
- Email format validated
- Customer saved successfully

**US-3:** Customer Validation Handling
As a system user
I want invalid inputs rejected
So that data integrity is maintained
**Acceptance Criteria**
- Blank Account # → Required message
- Non-numeric Account # → Numeric warning
- Invalid phone → Format warning
- Invalid email → Format warning

**US-4:** Search & Pagination – Customers
**Acceptance Criteria**
- Search by Account #
- Search by Name
- Per Page toggle works

**Definition of Done**
- Customer validations fully tested
- Edge cases executed
- High defects resolved
- Regression passed
