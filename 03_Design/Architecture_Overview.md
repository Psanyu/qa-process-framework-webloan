Architecture Overview – WebLoan LMS
1. System Architecture Summary
   The WebLoan Loan Management System (LMS) follows a 3-tier architecture model consisting of:
   - Presentation Layer
   - Business Logic Layer
   - Data Layer
   This separation ensures scalability, maintainability, and structured testing across system components 

2. Presentation Layer
   The Presentation Layer is implemented using:
   - Laravel Blade templates
   - HTML
   - CSS
   - JavaScript
   This layer renders UI components including:
   - Login Page
   - Dashboard
   - Navigation Bar
   - Users, Customers, Loans pages

**QA Focus Areas**
- UI field validation
- Error message verification
- Role-based visibility
- Session handling
- Client-side vs server-side validation behavior
- Navigation consistency across pages

3. Business Logic Layer

The Business Logic Layer is implemented using Laravel MVC architecture :
- Controllers – Handle incoming requests
- Models (Eloquent ORM) – Manage data and business rules
- Middleware – Filter HTTP requests
- Service Classes – Encapsulate core business logic
- Routing – URL-to-controller mapping
  
**QA Focus Areas**
- Authentication flow integrity
- Role-based access enforcement
- Loan calculation logic validation
- Returned customer discount application
- Central bank rate retrieval logic
- Transaction handling consistency
- Error handling and exception management

4. Data Layer
The Data Layer uses:
- MySQL relational database 
- Internal_Design_Document_ver3.1
- Laravel Eloquent ORM
**Key database entities include:**
- USERS
- CUSTOMERS
- LOANS
- EVENTS
- Database Constraint Highlights
- USERS.username → UNIQUE
- CUSTOMERS.account → UNIQUE (7 digits)
- Foreign keys (e.g., branch_id)
- NOT NULL constraints
- Auto-generated timestamps
**QA Focus Areas**
- Data integrity validation
- Uniqueness constraint testing
- Foreign key relationship validation
- Data persistence across sessions
- CRUD operation consistency
- Calculation storage accuracy

5. Deployment Environment
The application stack includes:
- PHP 8.1
- Laravel Framework
- MySQL
- Apache Web Server
- Ubuntu OS 
**QA Considerations**
- Browser compatibility testing
- Environment configuration validation
- Session timeout behavior
- Deployment smoke validation

6. Architectural Risk Considerations
Based on architecture analysis, the following areas are considered high risk:
- Loan interest rate calculation
- Central bank rate integration
- Role-based access enforcement
- Data consistency across modules
- Session security
These areas receive deeper regression coverage and automation support.

7. Testing Impact Across Layers
The architecture enables multi-layer validation:
- Layer	Testing Type
- Presentation	UI validation, negative testing
- Business Logic	Functional validation, RBAC testing
- Data Layer	Database validation, integrity testing
- Integration	End-to-end workflow validation
- Automation	Regression and high-risk path validation
