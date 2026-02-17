# qa-process-framework-webloan
End-to-end Agile QA operating model for a Financial Loan Management System (WebLoan), covering Manual, API, and UI Automation testing with full SDLC/STLC governance.

📖 Overview

This repository demonstrates an end-to-end Agile QA operating model for a Financial Loan Management System (WebLoan LMS).

The project simulates real-world enterprise QA delivery using:

✅ Manual Testing

✅ REST API Testing

✅ UI Automation (Selenium + TestNG)

✅ Agile Sprint Execution

✅ SDLC & STLC Governance

✅ Risk Management & Traceability

The objective is to showcase a structured, scalable, and production-ready QA framework similar to what is implemented in enterprise environments.

🏦 System Under Test (SUT)

Application: WebLoan – Loan Management System (LMS)

The system enables financial institutions to:

Manage user roles (Branch Admin, Loan Manager, Loan Officer)

Create and manage customers

Process and calculate loans

Generate prequalification letters

Track loan lifecycle events

Enforce role-based access control (RBAC)

Architecture follows a standard 3-tier model:

Presentation Layer

Business Logic Layer

Data Layer

Technology stack (as per system documentation):

PHP (Laravel Framework)

MySQL

Apache

Ubuntu

🧩 Project Structure
01_Executive_Summary        → Business context & QA vision
02_Requirements             → User stories, acceptance criteria, business rules
03_Design                   → Architecture notes, test design techniques
04_Test_Plan                → Test strategy, scope, entry/exit criteria
05_Test_Cases               → Sprint-based test case design
06_Defect_Management        → Defect log, severity model, RCA
07_Modeling_BC_ST           → Boundary value, equivalence, state transitions
08_UI_Mockups               → UI references (if applicable)
09_Traceability             → RTM (Requirement ↔ Test ↔ Defect mapping)
10_RiskMgmt                 → Risk register & mitigation strategy
11_AgileDocs                → Sprint planning, standups, retrospectives
12_API_Testing              → Postman collections & API test design
13_Automation               → Selenium + API automation framework

🔄 Agile Execution Model

This project is structured into simulated Agile sprints:

Sprint	Scope
Sprint 1	Login + Authentication + RBAC Smoke
Sprint 2	User Management
Sprint 3	Customer Management
Sprint 4	Loan Creation & Calculation
Sprint 5	Prequalification Letter Workflow
Sprint 6	Regression + Automation Expansion

Each sprint includes:

User Stories

Acceptance Criteria

Test Cases

RTM

Defect Tracking

Sprint Review & Retrospective Notes

🧪 Testing Layers Implemented
1️⃣ Manual Testing

Functional validation

UI validation

Negative testing

Boundary value analysis

Role-based access testing

Regression coverage

2️⃣ API Testing

Endpoint validation

Status code validation

Schema validation

Negative API testing

Authentication & authorization checks

Postman collection design

Newman execution reports

3️⃣ UI Automation

Framework built using:

Java

Selenium WebDriver

TestNG

Maven

Page Object Model (POM)

Automation scope includes:

Login flows

Mandatory field validation

Role-based navigation

High-risk regression paths

📊 Traceability & Governance

This repository demonstrates:

Requirement Traceability Matrix (RTM)

Defect lifecycle tracking

Severity classification

Root Cause Analysis (RCA)

Risk identification & mitigation

Entry & Exit criteria enforcement

Definition of Done (DoD)

Definition of Ready (DoR)

🎯 Key Objectives

Simulate enterprise-level QA delivery

Demonstrate SDLC and STLC maturity

Show Agile QA leadership capabilities

Present structured documentation practices

Integrate Manual + API + Automation testing layers

Showcase cross-domain QA adaptability

🚀 Future Enhancements

CI/CD integration (GitHub Actions)

Automated regression pipeline

Test coverage reporting

Code quality integration

Security testing layer

👩‍💻 Author

QA Portfolio Project
Agile Manual + API + Automation Framework
