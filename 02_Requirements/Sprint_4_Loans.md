**✅ Sprint 4 – Loans**
**Sprint Goal**
Implement and validate loan creation, approval/rejection logic, and listing behavior.

**User Stories**
**US-1:** Add Loan – Approval Flow
As a Loan Manager
I want loans approved when eligibility rules are met
So that customers receive financing
**Acceptance Criteria**
- Monthly Income > Monthly Debt
- Loan term selectable (2, 5, 15 years)
- Loan appears in list
- Approval letter generated

**US-2:** Add Loan – Rejection Logic
As a Loan Officer
I want system to reject ineligible loans
So that financial risk is minimized
**Acceptance Criteria**
- Income = 0 → Rejection
- Income < Debt → Rejection
- Income = Debt → Rejection
- Rejection letter generated

**US-3:** Loan Field Validations
**Acceptance Criteria**
- Income numeric only
- Debt numeric only
- Max character limits enforced
- Required fields mandatory

**US-4:** Loans Search & Pagination
**Acceptance Criteria**
- Search by Customer Name
- Search by Address
- Search by Income
- Per Page toggle works

**Definition of Done**
- Decision logic validated
- False positives/negatives tested
- No Critical defects
  
**Automation added for:**
- Approval scenario
- Rejection scenario
