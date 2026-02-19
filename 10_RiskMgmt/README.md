**Risk Register – WebLoan LMS QA Framework**
**1. Purpose**

This document identifies potential project risks across functional, technical, operational, and delivery domains, along with mitigation strategies.

**2. Risk Scoring Model**

Risk Score = Probability × Impact

**Impact	Description**
High	Business disruption or data loss
Medium	Feature degradation
Low	Minor inconvenience

**3. Risk Register Table**

ID, Risk Description, Category, Probability, Impact, Score, Mitigation, Strategy

R1	Duplicate Loan Applications	Functional	High	High	9	Add validation rule + negative testing

R2	500 Internal Server Error	Technical	Medium	High	6	Backend validation + API testing

R3	Login Failure	Security	Medium	High	6	Authentication regression suite

R4	Incorrect Loan Calculations	Financial	Low	High	6	Boundary & equivalence testing

R5	Data Not Updating on Dashboard	Integration	Medium	Medium	4	API validation + DB verification

R6	Search Logic Failure	Functional	Medium	Medium	4	Data-driven test cases

R7	UI Field State Errors	Usability	Medium	Low	3	UI checklist review

R8	Performance Degradation under Load	Performance	Low	High	6	Performance baseline testing

R9	Mobile Compatibility Issues	Compatibility	Medium	Low	3	Cross-device validation

R10	Production Data Integrity Risk	Data	Low	High	6	Data validation checkpoints

**4. High-Risk Areas Identified**

**Primary Risk Zones:**

- Loan creation & duplication logic

- Authentication & RBAC

- Financial calculations

- Prequalification letter generation

- Backend resource handling

These were treated as regression priority flows.

**5. Risk Mitigation Framework**

For High & Medium risks:

✔ Early test case design
✔ Negative testing scenarios
✔ API validation
✔ Data verification
✔ Regression automation

**6. Risk Monitoring Strategy**

- Reviewed during sprint planning
- Updated during defect triage
- Evaluated before release sign-off
- Included in post-release review

**7. Residual Risk at Release**
- Minor UI issues (Low impact)
- Partial search behavior limitations
- Business-approved functional deferrals
- Residual risk deemed acceptable by stakeholders.

**8. Risk Governance Outcome**

The structured risk approach ensured:
- No financial calculation failures
- No login breakdowns in production
- No critical production incidents
- Controlled business exposure
