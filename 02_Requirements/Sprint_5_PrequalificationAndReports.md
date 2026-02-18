**✅ Sprint 5 – PDF Letter, Role Access & System Stabilization**
**Sprint Goal**
Finalize document preview functionality, RBAC enforcement, and complete regression.

**User Stories**
**US-1:** Preview Prequalification Letter
As a Loan Manager
I want to preview the loan letter
So that I can verify customer communication
**Acceptance Criteria**
- PDF dialog opens
- Customer details correct
- Buttons visible: Bold, Italics, Strikethrough, Link, Bullet, Number Bullet, Block Quote, Attach Files, Save & Cancel functional

**US-2:** Role-Based Access Validation
As QA
I want RBAC validated
So that access is restricted properly
**Acceptance Criteria**
- Branch Admin → Full Access
- Loan Manager → Restricted User creation
- Loan Officer → No Events access
- Direct URL access blocked

**US-3:** Logout & Session Management
**Acceptance Criteria**
- Logout redirects to login
- Back button does not restore session
- Session properly destroyed

**Definition of Done**
- All 94 test cases executed
- 0 Critical defects
- High defects resolved
- Regression suite passed
- Test Closure Report completed
