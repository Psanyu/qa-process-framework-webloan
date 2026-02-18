TC_ID	Title	Priority	Type	Layer	Preconditions	Steps	Test_Data	Expected_Result	Status	Defect_ID	Automation_Candidate
WF-TC-001	Login page loads successfully	Critical	Smoke	UI	Browser available	Open login URL	qa.hitekschool.com/lms/loans/310{n}	Login page loads with Branch, Username, Password fields	Automated		Yes
WF-TC-002	Valid login navigates to Dashboard	Critical	Functional	UI	Valid test user exists	Enter Branch, Username, Password > Click Login	Branch=Tauranga; Username=<valid>; Password=<valid>	Dashboard opens after successful login	Automated		Yes
WF-TC-003	Branch mandatory validation	Critical	Negative	UI	On Login page	Leave Branch blank > Click Login	Blank Branch	System shows 'Please fill out this field.'	Automated		Yes
WF-TC-004	Username mandatory validation	Critical	Negative	UI	On Login page	Leave Username blank > Click Login	Blank Username	System shows 'Please fill out this field.'	Automated		Yes
WF-TC-005	Password mandatory validation	Critical	Negative	UI	On Login page	Leave Password blank > Click Login	Blank Password	System shows 'Please fill out this field.'	Automated		Yes
WF-TC-006	Verify form behavior with minimum field values	Critical	Boundary	UI	"1) Open URL: XXXXXX
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	"5) On ""Add Customer"" Page
- Enter Account# as 1 digit
--Title--Blank
-- First Name--Blank
-- Last Name--Blank
-- City--Blank
-- Province--Blank
-- Postal Code--Blank
-- Phone --Blank
-- Email --Blank
6) click Save"	"Account#: 1, 
-- Title: Blank 
-- First Name: Blank  
-- Last Name: Blank 
-- City: Blank 
-- Province: Blank 
-- Postal Code: Blank 
-- Phone: Blank 
-- Email: Blank"	"VP1:
Warning: Mandatory fields are missing"	Automated		Yes
WF-TC-007	Verify successful customer creation with all valid max input	Critical	Boundary	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	"5) On ""Add Customer"" Page
(Enter max chars for):
-- Account# 
-- Title
-- First Name
-- Last Name
-- City, 
-- Province, 
-- Postal Code, 
-- Phone and 
-- Email 

6) click Save"	"Account#: 1234567, 
-- Title: Mr., 
-- First Name: 32 chars, 
-- Last Name: 32 chars;
-- City: 32
-- Province: select any
-- Postal Code: 7
-- Phone: 10 chars
-- Email: 32 chars"	VP2: Customer is created	Automated		Yes
WF-TC-008	Verify customer creation with mid-range valid values	Medium	Functional	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	"5) On ""Add Customer"" Page
(Enter mid range data chars for):
-- Account# 
-- Title
-- First Name
-- Last Name
-- City, 
-- Province, 
-- Postal Code, 
-- Phone and 
-- Email 

6) click Save"	"Account#: 1234567, 
-- Title: Mr., 
-- First Name: 16 chars, 
-- Last Name: 16 chars;
-- City: 16
-- Province: select any
-- Postal Code: 3
-- Phone: 7 chars
-- Email: 16 chars"	VP3: Customer is created	Not Run		No
WF-TC-009	Verify warning when Account # is blank (min)	Critical	Negative	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	"5)Leave Account# blank
 
6) fill other fields:
-- Title
-- First Name
-- Last Name
-- City, 
-- Province, 
-- Postal Code, 
-- Phone and 
-- Email 

7) click Save"	"Account#: blank
-- Title: Any from dropdown
-- First Name: ""thirtytwocharacters"" 
-- Last Name:""thirtytwocharacters""
-- City:""thirtytwocharacters""
-- Province: Any from dropdown
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: 'thirty-two@char.com'"	VP4: Warning: 'Account #' field is required	Automated		Yes
WF-TC-010	Validate Account# for non-numeric input (invalid input)	Critical	Negative	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	"5) Enter alphanumeric Account#, 
-- Title
-- First Name
-- Last Name
-- City, 
-- Province, 
-- Postal Code, 
-- Phone and 
-- Email 
6)  click Save"	"Account#: abc1234
-- Title: Any from dropdown
-- First Name: ""thirtytwocharacters"" 
-- Last Name:""thirtytwocharacters""
-- City:""thirtytwocharacters""
-- Province: Any from dropdown
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: 'thirty-two@char.com'"	VP5: Warning: 'Account #' must be numeric	Automated		Yes
WF-TC-011	Validate Account# input exceeding 7 digits	Medium	Boundary	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	Enter 8 digits in Account#, click Save	"Account#: 12345678
-- Title: Any from dropdown
-- First Name: ""thirtytwocharacters"" 
-- Last Name:""thirtytwocharacters""
-- City:""thirtytwocharacters""
-- Province: Any from dropdown
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: 'thirty-two@char.com'"	VP6:  restricts input to 7 digits	Ready for Automation		Yes
WF-TC-012	Validate First Name for invalid characters	Medium	Negative	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	Enter invalid First Name with numbers/symbols, click Save	"Account#: 12345678
-- Title: Any from dropdown
-- First Name: Alex123!
-- Last Name:""thirtytwocharacters""
-- City:""thirtytwocharacters""
-- Province: Any from dropdown
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: 'thirty-two@char.com'"	VP7: Warning: Only letters allowed in 'First Name'	Ready for Automation		Yes
WF-TC-013	Validate Last Name for invalid characters	Medium	Negative	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	Enter invalid Last Name with numbers/symbols, click Save	"Account#: 12345678
-- Title: Any from dropdown
-- First Name: ""thirtytwocharacters"" 
-- Last Name: @nderson123
-- City:""thirtytwocharacters""
-- Province: Any from dropdown
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: 'thirty-two@char.com'"	VP8: Warning: Only letters allowed in 'Last Name'	Ready for Automation		Yes
WF-TC-014	Validate phone number format	Critical	Negative	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	Enter invalid phone number, click Save	"Account#: 12345678
-- Title: Any from dropdown
-- First Name: ""thirtytwocharacters"" 
-- Last Name: @nderson123
-- City:""thirtytwocharacters""
-- Province: Any from dropdown
-- Postal Code, 
-- Phone: 123
-- Email: 'thirty-two@char.com'"	VP9:Warning: Phone must be in (999)999-9999 format	Automated		Yes
WF-TC-015	Validate email address format	Critical	Negative	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	Enter email without '@', click Save	"Account#: 12345678
-- Title: Any from dropdown
-- First Name: ""thirtytwocharacters"" 
-- Last Name: @nderson123
-- City:""thirtytwocharacters""
-- Province: Any from dropdown
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: user#domain.com"	VP10: Warning: Invalid email address	Automated		Yes
WF-TC-016	Validate province selection is required	Critical	Negative	UI	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 
2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page
3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner
4) Click on ""Add Customer"" button on top right corner"	Leave Province unselected, click Save	"Account#: 12345678
-- Title: Any from dropdown
-- First Name: ""thirtytwocharacters"" 
-- Last Name: @nderson123
-- City:""thirtytwocharacters""
-- Province: Blank
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: user#domain.com"	VP11: Warning: Province is mandatory	Automated		Yes
WF-TC-017	Verify Login Page opens with all its features	Medium	Functional	UI	Browser is Operational	Open URL: [subdomain].hitekschool.com/lms/[build_number]	https://qa.hitekschool.com/lms/3106/login	"Login Page opens with all its features:
- Text Field ""Branch Name""
- Text Field ""User Name""
- Text Field ""Password""
- Text Field ""Sign In Button""
- Radio Button ""Remember Me"" 
- Smartbank Logo
- Smartbank Image
- Text ""Sign in to your Branch account"""	Not Run		No
WF-TC-018	Verify "SignIn" button is functioning	Medium	Functional	UI	URL is Open: [subdomain].hitekschool.com/lms/[build_number]	"Enter Data in Text fields and Radio button below:
- Text Field ""Branch Name""
- Text Field ""User Name""
- Text Field ""Password""
- Text Field ""Sign In Button""
- Radio Button ""Remember Me"""	"Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"""	Dashboard Page (Homepage) Opens	Not Run		No
WF-TC-019	Verify Dashboard Page opens with all its features	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Review all features on the Dashboard (homepage) of the WebLoan App

3) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Review Loading of 
- Summary Chart 
- ""Total Approved""
- ""Total Rejected""
- ""Total Customer""
- ""Navigation Bar"""	"Dashboard Page opens with all its features 
- Summary Chart 
- ""Total Approved""
- ""Total Rejected""
- ""Total Customer""
- ""Navigation Bar"""	Not Run		No
WF-TC-020	Verify "Users - [branch name] Branch" opens with all its features	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) Link for ""Users"" is active in the Navigation Bar on the ""Dashboard"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Dashboard page opens with all the features:
- Summary Chart 
- ""Total Approved""
- ""Total Rejected""
- ""Total Customer""
- ""Navigation Bar""

3)Click on the Link for ""Users"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

4) ""Users - [branch name] Branch"" / List for Users page opens

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Review Loading of 
- Summary Chart 
- ""Total Approved""
- ""Total Rejected""
- ""Total Customer""
- ""Navigation Bar""

3) Click on the Link for ""Users"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

4) ""Users - 'Tauranga' Branch"" / List for Users page opens

5) Logout"	"Page opens with all its features:
1) Table with Column Features below :
 - Username
 - First Name
 - Last Name
 - Company
 - Phone
 - Email
 - Edit button for each individual User line
 - Delete button for each individual User line
2) Search field
3) Per Page Toggle button
4) ""Add User"" button"	Not Run		No
WF-TC-021	Verify "Search" functions as expected when varied data fields are searched for	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Users - [branch name] Branch"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""Users"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Users - [branch name] Branch"" / List for Users page opens

4-1) Type text [Username] in the search data field and click enter and observe results

4-2) Type text [First Name] in the search data field and click enter and observe results

4-3) Type text [Last Name] in the search data field and click enter and observe results

4-4) Type text [Company] in the search data field and click enter and observe results

4-5) Type text [Email] in the search data field and click enter and observe results

4-6) Type text [Phone] in the search data field and click enter and observe results

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Users"" on the ""Navigation Bar""

3) ""Users - Tauranga Branch"" Opens

4-1) Username = jsmith0506

4-2) First Name = Jonathan

4-3) Last Name =Smith

4-4) Company = Smartbank

4-5) Email = jsmith@smartbank.com

4-6) Phone = (666)777-8888

5) Logout"	"4-1) 1 result of jsmith0506

4-2) 1 result of jsmith0506

4-3) 1 result of jsmith0506 and
        1 result of Walter78

4-4) 6 results

4-5) 1 result of jsmith0506 

4-6) 1 result of jsmith0506 

5) Logout"	Not Run		No
WF-TC-022	Verify "Per Page"  Function works by filtering for a set number in the Users list	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Users - [branch name] Branch"" page"	"1)Click on the Link for ""Users"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

2) ""Users - [branch name] Branch"" / List for Users page opens

3) Select [# of Users to be shown Per Page] on the Per Page Toggle function

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Users"" on the ""Navigation Bar""

3-1) Per Page = 5
3-2) Per Page = 10
3-3) Per Page = All

4) Logout"	"3-1) 5 result on Page

3-2) 10 results on Page

3-3) All results on Page

4) Logout"	Not Run		No
WF-TC-023	Verify "Customers - [branch name] Branch" opens with all its features	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Customers - [branch name] Branch"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""Customers"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Cutomers - [branch name] Branch"" / List for Customers page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on the Link for ""Customers"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Customers - 'Tauranga' Branch""  page opens

4) Logout"	"Page opens with all its features:
1) Table with Column Features below :
 - Account #
 - Name
 - Address
 - Phone
 - Email
 - Edit button for each individual Customer line
 - Delete button for each individual Customer line

2) Search field

3) Per Page Toggle button

4) ""Add Customer"" button"	Not Run		No
WF-TC-024	Verify "Search" data field functions as expected when varied data fields are searched for	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Customers - [branch name] Branch"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""Customers"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Customers - [branch name] Branch"" / List for Customers page opens

4-1) Type numbers [Account#] in the search data field and click enter and observe results

4-2) Type text [Name] in the search data field and click enter and observe results

4-3) Type text [Address] in the search data field and click enter and observe results

4-4) Type text [Phone] in the search data field and click enter and observe results

4-5) Type text [Email] in the search data field and click enter and observe results

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Customers"" on the ""Navigation Bar""

3) ""Customers - Tauranga Branch""  page opens

4-1) Account # = 1234567

4-2) Name = Mrs. Adrian Lekailo

4-3) Address =34 Goto Road, Bumberton Ontario, L5E 6NO

4-4) Phone = (416)788-0000

4-5) Email = al@sample.com

5) Logout"	"4-1) 1 result of Mrs. Adrian Lekailo

4-2) 1 result of Mrs. Adrian Lekailo

4-3) 1 result of Mrs. Adrian Lekailo

4-4) 1 result of Mrs. Adrian Lekailo

4-5) 1 result of Mrs. Adrian Lekailo 

4-6) 1 result of Mrs. Adrian Lekailo 

5) Logout"	Not Run		No
WF-TC-025	Verify "Per Page"  Function works by filtering for a set number in the Users list	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Customers - [branch name] Branch"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

3) Click on the Link for ""Customers"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

4) ""Customers - [branch name] Branch"" / List for Customers page opens

5) Select [# of Customers to be shown Per Page] on the Per Page Toggle function

6) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Customers"" on the ""Navigation Bar""

3) ""Customers - Tauranga Branch""  page opens

4-1) Per Page = 5
4-2) Per Page = 10
4-3) Per Page = All

5) Logout"	"4-1) 5 results on Page

4-2) 10 results on Page

4-3) All results on Page

5) Logout"	Not Run		No
WF-TC-026	Verify "Loans - [branch name] Branch" opens with all its features	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Loans - [branch name] Branch"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""Loans"" link on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Loans - [branch name] Branch"" / List for Loans page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Loans - 'Tauranga' Branch"" page opens

4) Logout"	"""Loans - 'Tauranga' Branch"" Page opens with all its features:
3-1) Table with Column Features below :
 - Customer Name
 - Address
 - Income/debt
 - Loan Terms 
 - Returning Customer 
 - PDF button for each individual Customer line
 - Edit button for each individual Customer line
 - Delete button for each individual Customer line

3-2) Search field

3-3) Per Page Toggle button

3-4) ""Add Loans"" button

4) Logout"	Not Run		No
WF-TC-027	Verify "Search" data field functions as expected when varied data fields are searched for	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Loans - [branch name] Branch"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Loans - [branch name] Branch"" / List for Loans page opens

4-1) Type numbers [Customer Name] in the search data field and click enter and observe results

4-2) Type text [Address] in the search data field and click enter and observe results

4-3) Type text [Income/ Debt] in the search data field and click enter and observe results

4-4) Type text [Loan Terms] in the search data field and click enter and observe results

4-5) Click Radio Button [Returning Customer] in the search data field and click enter and observe results

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Loans"" on the ""Navigation Bar""

3) ""Loans - Tauranga Branch"" page opens

4-1) Customer Name = Mrs. Adrian Lekailo
4-2) Address =34 Goto Road, Bumberton Ontario, L5E 6NO
4-3) Income: $5,000.00
4-4) Debt: $1,200.00
4-5) Payments: $467.00
4-6) Term Years: 15
4-7) Approved Rate: 7.50%
4-8) Loan Amount: $50,377.00

5) Logout"	"4-1) 3 results of Mrs. Adrian Lekailo
4-2) 3 results of Mrs. Adrian Lekailo
4-3) 3 results of Mrs. Adrian Lekailo
4-4)  1 result of Mrs. Adrian Lekailo
4-5) 1 result of Mrs. Adrian Lekailo
4-6) 1 result of Mrs. Adrian Lekailo
4-7) 1 result of Mrs. Adrian Lekailo
4-8) 4 results 
4-9) 4 results
4-10) 1 result of Mrs. Adrian Lekailo

5) Logout"	Not Run		No
WF-TC-028	Verify "Per Page"  Function works by filtering for a set number in the Users list	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Loans - [branch name] Branch"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Loans - [branch name] Branch"" / List for Customers page opens

4) Select [# of Loans to be shown Per Page] on the Per Page Toggle function

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Loans"" on the ""Navigation Bar""

3) ""Loans - Tauranga Branch"" page opens

4-1) Per Page = 5
4-2) Per Page = 10
4-3) Per Page = All

5) Logut"	"4-1) 5 result on Page

4-2) 10 results on Page

4-3) All results on Page

5) Logout"	Not Run		No
WF-TC-029	Verify Prequalification Letter opens on clicking on PDF button for Individual Customer Loan Application line on the "Loans - [branch name] Branch"	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Loans - [branch name] Branch"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Loans - [branch name] Branch"" / List for Customers page opens

4) Click on PDF button for an individual user line

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Loans"" on the ""Navigation Bar""

3) ""Loans - Tauranga Branch"" page opens 

4) Click on PDF button for Mrs. Adrian Lekailo

5) Logout"	"4) Prequalification letter for Mrs. Adrian Lekailo opens in a separate dialogue box

5) Logout"	Not Run		No
WF-TC-030	Verify "Policies" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Policies"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Policies"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Policies"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Policies"" on the ""Navigation Bar""

3) ""Policies"" page opens

4) Logout"	Policies Page Opens	Not Run		No
WF-TC-031	Verify "About" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""About"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""About"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""About"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""About"" on the ""Navigation Bar""

3) ""About"" page opens

4) Logout"	About Page Opens	Not Run		No
WF-TC-032	Verify "Help" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Help"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Help"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Help"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Help"" on the ""Navigation Bar""

3) ""Help"" page opens

4) Logout"	HELP Page Opens	Not Run		No
WF-TC-033	Verify User Logs out successfully and Login page appears	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User Clicks on ""User Role"" button on top right button and click on Logout button on the ""Dashboard"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on ""User Role"" button on top right button 

3) Click on Logout button on the ""Dashboard"" page

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

4) Logout"	User Logs out and Login page [subdomain].hitekschool.com/lms/[build_number] loads	Not Run		No
WF-TC-034	Verify "Add loan" page appearance is clear and all objects and properties are visible	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Dashboard page opens with all the features:
- Summary Chart 
- ""Total Approved""
- ""Total Rejected""
- ""Total Customer""
- ""Navigation Bar""

3)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

4) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4) Add Loan page opens 
5) Logout"	"Add Loan page opens succcessfully with the fields and buttons below:
1) ""Customer financial data"":
  - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
3) ""Returned Customer"" Radio button for Yes/ No
4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
5) ""Preview Prequalification letter"" button
6) Save button
7) Save & Add Another button
8) Cancel button"	Automated		Yes
WF-TC-035	Verify "Add loan" page gives valid output for all datafields having valid input while term year "2" is selected when "Save" button is clicked (Positive)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""2""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 5000"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =2"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-036	Verify "Add loan" page gives valid output for all datafields having valid input while term year "5" is selected when "Save" button is clicked (Positive)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""5""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 5000"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =5"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-037	Verify "Add loan" page gives valid output for all datafields having valid input while term year "15" is selected when "Save" button is clicked (Positive)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""15""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 5000"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =15"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-038	Verify "Save & Add another" button works for "Add loan" page (Positive)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on ""Save & Add another""

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on ""Save & Add another""

5) Logout"	"1) New ""Add Loan"" page opens succcessfully with ""Customer financial data"", ""Loan Terms"", ""Term Years"", ""Returned Customer"",""Central Bank Rate"", ""Preview Prequalification letter"" button, ""Save"" button, ""Save & Add Another"" button and ""Cancel"" button

2)""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 5000"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =10"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-039	Verify "Cancel" button works for "Add loan" page (Positive)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Cancel

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Cancel

5) Logout"	"Loans-Tauranga" page doe not generate a new line (new row) for the test data	Automated		Yes
WF-TC-040	Verify "Preview Prequalification letter" button works for "Add loan" page (Positive)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on ""Preview Prequalification letter"" and ""Save""

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	A pdf dialogue box opens with a prequalification letter for "Mrs. Adrian Lekailo"	Automated		Yes
WF-TC-041	Verify "Add loan" page gives warning message "The 'Customer' field is required"  for "Customer Name" having invalid input when "Save" button is clicked (Negative)	Critical	Negative	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown is not selected
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Do not Select any Customer Name
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"Loans-Tauranga" page does not generate a new line and a warning message appears for "The 'Customer' field is required"	Automated		Yes
WF-TC-042	Verify "Add loan" page generates a rejection letter for 'Customer' having datafield "Monthly Income" (0) when "Save" button is clicked (Negative)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name""
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= ""Mrs. Adrian Leikalo""
 - Monthly Income= ""0"" 
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"1) ""Loans-Tauranga"" page generates a rejection letter for the related Customer Name

""Dear Mrs. Adrian Lekailo,
                     
 Thank you for contacting SmartBank about your credit needs. Unfortunately, after careful review of your application, we must decline your loan request at this time. However, we would gladly reconsider your request when your income-to-debt ratio changes.
                 
 Sincerely,""        

2) ""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 0"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =10"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-043	Verify "Add loan" page generates a rejection letter for 'Customer' having datafield "Monthly Income" (<) "Monthly Debt"/  "Monthly Debt" (>) "Monthly Income"when "Save" button is clicked (Negative)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name""
 - ""Monthly Income"" datafield < "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= ""Mrs. Adrian Leikalo""
 - Monthly Income= 890
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"1) ""Loans-Tauranga"" page generates a rejection letter for the related Customer Name

""Dear Mrs. Adrian Lekailo,
                     
 Thank you for contacting SmartBank about your credit needs. Unfortunately, after careful review of your application, we must decline your loan request at this time. However, we would gladly reconsider your request when your income-to-debt ratio changes.
                 
 Sincerely,""        

2) ""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 890"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =10"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-044	Verify "Add loan" page generates a rejection letter for 'Customer' having datafield "Monthly Income" (=) "Monthly Debt" when "Save" button is clicked (Negative)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name""
 - ""Monthly Income"" datafield = "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= ""Mrs. Adrian Leikalo""
 - Monthly Income= 1200
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"1) ""Loans-Tauranga"" page generates a rejection letter for the related Customer Name

""Dear Mrs. Adrian Lekailo,
                     
 Thank you for contacting SmartBank about your credit needs. Unfortunately, after careful review of your application, we must decline your loan request at this time. However, we would gladly reconsider your request when your income-to-debt ratio changes.
                 
 Sincerely,""        

2) ""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 1200"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =10"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-045	Verify "Add loan" page generates a rejection letter for 'Customer' having datafield "Monthly Income" = 'non numeric' when "Save" button is clicked (Negative)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name""
 - ""Monthly Income"" datafield = attempt entering text in this datafield
 - ""Monthly Debt""
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= ""Mrs. Adrian Leikalo""
 - Monthly Income= ""abc""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"1) ""Monthly Income"" field stays empty

1) ""Loans-Tauranga"" page generates a rejection letter for the related Customer Name

""Dear Mrs. Adrian Lekailo,
                     
 Thank you for contacting SmartBank about your credit needs. Unfortunately, after careful review of your application, we must decline your loan request at this time. However, we would gladly reconsider your request when your income-to-debt ratio changes.
                 
 Sincerely,""    

3) ""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 0"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =10"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-046	Verify "Add loan" page generates a rejection letter for 'Customer' having datafield "Monthly Income" = > 6 characters when "Save" button is clicked (False Positive)	Medium	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name""
 - ""Monthly Income"" datafield = attempt entering characters more than 6 fields in this datafield
 - ""Monthly Debt""
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= ""Mrs. Adrian Leikalo""
 - Monthly Income= attempt entering ""999999"" cannot enter stays at ""99999""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"1) ""Monthly Income"" field stays empty

2) ""Loans-Tauranga"" page generates an acceptance letter for the related Customer Name


3) ""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 99999"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =10"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Ready for Automation		Yes
WF-TC-047	Verify "Add loan" page generates a rejection letter for "Customer Name" having datafield for "Monthly Debt" = 'non-numeric' when "Save" button is clicked (False Positive)	Medium	Negative	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name""
 - ""Monthly Income"" 
-  ""Monthly Debt""= Text
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= ""Mrs. Adrian Leikalo""
 - Monthly Income= ""1200""
 - Monthly Debt= ""abc""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"1) ""Monthly Income"" field stays empty

2) ""Loans-Tauranga"" page generates an acceptance letter for the related Customer Name

""Dear Mrs. Adrian Lekailo,
                     
 You have been approved for a Loan of $41,856.00 at an interest rate of 8% per annum from SmartBank.
 Please don't hesitate to contact us for more information.
                 
 Sincerely,                    
                                     
 Tauranga Branch Admin""       

3) ""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 1200"", ""Debt= 0"", ""Monthly payments of = 400"" 
- ""Loan Terms"": ""Tern years =10"", ""Approved Rate: 7.50%"", ""Loan Amount: $41,856""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Ready for Automation		Yes
WF-TC-048	Verify "Add loan" page generates a rejection letter for "Customer Name" having datafield for "Monthly Debt" = '999999' for characters more than 5 numbers when "Save" button is clicked (False Positive)	Medium	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name""
 - ""Monthly Income"" 
-  ""Monthly Debt""= more than 6 number of characters
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= ""Mrs. Adrian Leikalo""
 - Monthly Income= ""1200""
 - Monthly Debt= ""999999""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"1) ""Monthly Income"" field stays empty

2) ""Loans-Tauranga"" page generates a rejection letter for the related Customer Name

3) ""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 1200"", ""Debt= 99999"", ""Monthly payments of = 0"" 
- ""Loan Terms"": ""Tern years =10"", ""Approved Rate: 7.50%"", ""Loan Amount: $41,856""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Ready for Automation		Yes
WF-TC-049	Verify "Add loan" page generates a new line for related 'Customer Name' having not generate 'Central Bank Rate' when "Save" button is clicked (Negative)	Critical	Functional	UI	Customer is created using "Add Customer" on the "Cutomers - [branch name] Branch" page	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name""
 - ""Monthly Income"" 
-  ""Monthly Debt""
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms"" - ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) Don't click on ""Central Bank Rate"" red button 
4-5) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= ""Mrs. Adrian Leikalo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""don't click
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"1) ""Monthly Income"" field stays empty

2) ""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 1200"", ""Debt= 0"", ""Monthly payments of = 400"" 
- ""Loan Terms"": Empty
- ""Returned Customer"": Empty checkbox
- PDF button
- Edit button
- Delete button"	Automated		Yes
WF-TC-050	Verify "Preview Prequalification letter" button works for "Add loan" page (Positive) and the dialogue box with "Prequalified Letter" page appearance is clear and all objects and properties are visible	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on ""Save"" on the ""Add Loans"" Page

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
with all its buttons:
- Bold
- Italics
- Strikethrough
- Link
- Bullet 
- Number Bullet
- Block quotes
- Attach files
- Undo
- Redo
- Open PDF
- Save
- Cancel"	Automated		Yes
WF-TC-051	Verify Bold button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select the Salutation ""Dear Mrs. Adrian"" Click on Bold button
4-7) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate""- Click on""Central Bank Rate"" red button 
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select the Salutation ""Dear Mrs. Adrian"" Click on Bold button
4-7) Click on Save

6) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Salutation is in bold letters

""Dear Mrs. Adrian Lekailo,
                     
 You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
 Please don't hesitate to contact us for more information.
                 
 Sincerely,                    
                                     
 Tauranga Branch Admin"""	Automated		Yes
WF-TC-052	Verify Italic button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" 
4-6) Select the Salutation ""Dear Mrs. Adrian"" Click on Italics button
4-7) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select the Salutation ""Dear Mrs. Adrian"" Click on Italics button
4-7) Click on Save

5) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Salutation is in italics letters

""Dear Mrs. Adrian Lekailo,
                     
 You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
 Please don't hesitate to contact us for more information.
                 
 Sincerely,                    
                                     
 Tauranga Branch Admin"""	Automated		Yes
WF-TC-053	Verify Strikethrough button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Slect the Salutation ""Dear Mrs. Adrian"" Click on Strikethrough button
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Slect the Salutation ""Dear Mrs. Adrian"" Click on Strikethrough button
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Salutation is in striked through

""Dear Mrs. Adrian Lekailo,
                     
 You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
 Please don't hesitate to contact us for more information.
                 
 Sincerely,                    
                                     
 Tauranga Branch Admin"""	Automated		Yes
WF-TC-054	Verify Link button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select the link button and attempt to hyperlink
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select the link button and attempt to hyperlink a document (https://qa.hitekschool.com/lms/3106/login)
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter has a hyperlink 
""Dear Mrs. Adrian Lekailo,
                     
 You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
 Please don't hesitate to contact us for more information.
(https://qa.hitekschool.com/lms/3106/login)
                 
 Sincerely,                    
                                     
 Tauranga Branch Admin"""	Automated		Yes
WF-TC-055	Verify Blockquote button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select the letter body and click on block quote button
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select the letter body and click on block quote button
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter body is in block quotes
Dear Mrs. Adrian Lekailo,
                     
>  You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
 Please don't hesitate to contact us for more information.
                 
 Sincerely,                    
                                     
 Tauranga Branch Admin 
 Sanyogita  Herwathe"	Automated		Yes
WF-TC-056	Verify Bullet buttons works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Type ""a, b, c"" on separate lines in the letter body and select the bullet button
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6)  Type ""a, b, c"" on separate lines in the letter body and select the bullet button
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter body has bullets
Dear Mrs. Adrian Lekailo,
                     
You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
Please don't hesitate to contact us for more information.

* a
* b
* c
                 
 Sincerely,                    
                                     
 Tauranga Branch Admin 
 Sanyogita  Herwathe"	Automated		Yes
WF-TC-057	Verify Numeric Bullet buttons works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Type ""a, b, c"" on separate lines in the letter body and select the numeric bullet button
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6)  Type ""a, b, c"" on separate lines in the letter body and select the numeric bullet button
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter body is in numeric bullets
Dear Mrs. Adrian Lekailo,
                     
You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
Please don't hesitate to contact us for more information.

1. a
2. b
3. c
                 
 Sincerely,                    
                                     
 Tauranga Branch Admin"	Automated		Yes
WF-TC-058	Verify Attach files button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Attach files button, browse and select a word doc related to the application
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6)  Click on Attach files button, browse and select a word doc related to the application
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter has a attachment of file with it
Dear Mrs. Adrian Lekailo,
                     
You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
Please don't hesitate to contact us for more information.
              
 Sincerely,                    
                                     
 Tauranga Branch Admin"	Automated		Yes
WF-TC-059	Verify Undo button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select salutation of the letter ""Dear Mrs. Adrian"" and click on ""Bold"" button and click on ""Undo"" button 
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select salutation of the letter ""Dear Mrs. Adrian"" and click on ""Bold"" button and click on ""Undo"" button 
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter has no changes"	Automated		Yes
WF-TC-060	Verify Redo button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select salutation of the letter ""Dear Mrs. Adrian"" and click on ""Bold"" button and click on ""Undo"" and then ""Redo"" button 
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Select salutation of the letter ""Dear Mrs. Adrian"" and click on ""Bold"" button and click on ""Undo"" and ""Redo"" button 
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter's Salutation is in bold post (Undo and Redo)
 Dear Mrs. Adrian Lekailo,
                     
You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
Please don't hesitate to contact us for more information.
              
 Sincerely,                    
                                     
 Tauranga Branch Admin"	Automated		Yes
WF-TC-061	Verify Open PDF button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on ""Open PDF"" button 
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on ""Open PDF"" button
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter will be generated in a pdf attachment that will open
 Dear Mrs. Adrian Lekailo,
                     
You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
Please don't hesitate to contact us for more information.
              
 Sincerely,                    
                                     
 Tauranga Branch Admin"	Automated		Yes
WF-TC-062	Verify Save PDF button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on ""Save PDF"" button 
4-7) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on ""Save PDF"" button
4-7) Click on Save

7) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter will be generated in a pdf attachment that will open and saved on selected location 
 Dear Mrs. Adrian Lekailo,
                     
You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
Please don't hesitate to contact us for more information.
              
 Sincerely,                    
                                     
 Tauranga Branch Admin"	Automated		Yes
WF-TC-063	Verify Cancel PDF button works for "Preview Prequalification letter"	Critical	Functional	UI	"1) Customer is created using ""Add Customer"" on the ""Cutomers - [branch name] Branch"" page

2) Numeric fields below have characters within character limit 0 to 99999
- ""Monthly Income"" 
- ""Monthly Debt"""	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"": ""Customer Name"" dropdown, ""Monthly Income"" datafield, "" Monthly Debt"" datafield, ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- ""Term Years"" 
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) Click on ""Preview Prequalification letter"" button
4-6) Type ""ABC"" on the letter body and click cancel 
4-7) Click on Save
4-8) Click on ""Preview Prequalification letter"" button again 
4-9) The PDF opened will have no ""ABC""

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""10""
4-3) ""Returned Customer""= don't click
4-4) ""Central Bank Rate"" - Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on ""Save PDF"" button
4-7) Click on Save
4-8) Click on ""Preview Prequalification letter"" button again 
4-9) The PDF opened will have no ""ABC"" words in it and will have not changes

5) Logout"	"4-5) A pdf dialogue box opens with a prequalification letter for ""Mrs. Adrian Lekailo""
1) with all its buttons: Bold, Italics, Strikethrough, Link,  Bullet, Number Bullet, Block quotes, Attach files, Undo, Redo, Open PDF, Save and Cancel

2) Letter will be generated in a pdf attachment that will open and saved on selected location and The PDF opened will have no ""ABC"" words in it and will have not changes

 Dear Mrs. Adrian Lekailo,
                     
You have been approved for a Loan of $38,491.00 at an interest rate of 8% per annum from SmartBank.
Please don't hesitate to contact us for more information.
              
 Sincerely,                    
                                     
 Tauranga Branch Admin"	Automated		Yes
WF-TC-064	Validate email address format	Critical	Negative	UI	URL is valid: [subdomain].hitekschool.com/lms/[build_number]	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 

2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner

4) Reach on ""Customers- Tauranga"" page and click on ""Add Customer"" button on top right corner

5)Enter details on ""Add Customer"" Page for features/ datafields (Account#, ""Title"", ""First Name"", ""Last Name"", ""City"", ""Province"", ""Postal Code"", ""Phone"" and ""Email"" with invalid input ) with buttons (""Save"", ""Save & Add another"" and ""Cancel"")

6) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Open URL: 
https://qa.hitekschool.com/lms/3106/loans/create

2) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

3&4) Navigate to ""Add Customer"" Page from ""Customers - Tauranga Branch"" page

5) On Add Customer Page add the details below: 
-- Account#: 1234501
-- Title: Any from dropdown
-- First Name: ""thirtytwocharacters"" 
-- Last Name: Anderson123
-- City:""thirtytwocharacters""
-- Province: Any from dropdown
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: user#domain.com

6) Save

7) Logout"	"""Add Customer"" page gives warnings for details on ""Add Customer"" Page for features/ datafields (""Email""):
-- Email: The 'Email' field must be a valid email address."	Automated		Yes
WF-TC-065	Validate province selection is required	Critical	Negative	UI	URL is valid: [subdomain].hitekschool.com/lms/[build_number]	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 

2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner

4) Reach on ""Customers- Tauranga"" page and click on ""Add Customer"" button on top right corner

5)Enter details on ""Add Customer"" Page for features/ datafields (Account#, ""Title"", ""First Name"", ""Last Name"", ""City"", ""Province""with invalid input , ""Postal Code"", ""Phone"" and ""Email"") with buttons (""Save"", ""Save & Add another"" and ""Cancel"")

6) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Open URL: 
https://qa.hitekschool.com/lms/3106/loans/create

2) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

3&4) Navigate to ""Add Customer"" Page from ""Customers - Tauranga Branch"" page

5) On Add Customer Page add the details below: 
-- Account#: 1234524
-- Title: Ms.
-- First Name: ""thirtytwocharacters"" 
-- Last Name: Anderson123
-- City:""thirtytwocharacters""
-- Province: Blank
-- Postal Code, 
-- Phone: '2010054568' 
-- Email: user@domain.com

6) Save

7) Logout"	"""Add Customer"" page gives warnings for details on ""Add Customer"" Page for features/ datafields (""Province""):
-- Province: The 'Province' field must be selected."	Automated		Yes
WF-TC-066	Verify "Save & Add another" button works for "Add loan" page (Positive)	Critical	Functional	UI	URL is valid: [subdomain].hitekschool.com/lms/[build_number]	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 

2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner

4) Reach on ""Customers- Tauranga"" page and click on ""Add Customer"" button on top right corner

5)Enter details on ""Add Customer"" Page for features/ datafields (Account#, ""Title"", ""First Name"", ""Last Name"", ""City"", ""Province"", ""Postal Code"", ""Phone"" and ""Email"") with buttons (""Save"", ""Save & Add another"" and ""Cancel"")

6) Click on Save & Add another

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Open URL: 
https://qa.hitekschool.com/lms/3106/loans/create

2) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

3&4) Navigate to ""Add Customer"" Page from ""Customers - Tauranga Branch"" page

5) On Add Customer Page add the details below: 
-- Account#: 1234514
-- Title: Mr.
-- First Name: ""Sal"" 
-- Last Name: ""Phill""
-- City:""Surrey""
-- Province: BC
-- Postal Code= XCVGH9
-- Phone: '2010054568' 
-- Email: user@domain.com

6) Save& Add another (New ""Add Customer"" Page opens)

7) Logout"	"1) ""Customers-Tauranga"" page generates a line (new row)for  columns:
-- Account#: 1234567
-- Title: Mr.
-- First Name: ""Sal"" 
-- Last Name: ""Phill""
-- City:""Surrey""
-- Province: BC
-- Postal Code= XCVGH9
-- Phone: '2010054568' 
-- Email: user@domain.com
- Edit button
- Delete button

2) Save& Add another (New ""Add Customer"" Page opens)"	Automated		Yes
WF-TC-067	Verify "Cancel" button works for "Add loan" page (Positive)	Critical	Functional	UI	URL is valid: [subdomain].hitekschool.com/lms/[build_number]	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 

2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner

4) Reach on ""Customers- Tauranga"" page and click on ""Add Customer"" button on top right corner

5)Enter details on ""Add Customer"" Page for features/ datafields (Account#, ""Title"", ""First Name"", ""Last Name"", ""City"", ""Province"", ""Postal Code"", ""Phone"" and ""Email"") with buttons (""Save"", ""Save & Add another"" and ""Cancel"")

6) Click on Cancel

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Open URL: 
https://qa.hitekschool.com/lms/3106/loans/create

2) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

3&4) Navigate to ""Add Customer"" Page from ""Customers - Tauranga Branch"" page

5) On Add Customer Page add the details below: 
-- Account#: 1234526
-- Title: Mr.
-- First Name: ""Sal"" 
-- Last Name: ""Phill""
-- City:""Surrey""
-- Province: BC
-- Postal Code= XCVGH9
-- Phone: '2010054568' 
-- Email: user@domain.com

6) Click on ""Cancel""

7) Logout"	"Customers-Tauranga" page does not generate a new line (new row)for the columns	Automated		Yes
WF-TC-068	Verify "Account#" duplicate does not allow a new customer creation (Negative)	Critical	Functional	UI	URL is valid: [subdomain].hitekschool.com/lms/[build_number]	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 

2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner

4) Reach on ""Customers- Tauranga"" page and click on ""Add Customer"" button on top right corner

5)Enter details on ""Add Customer"" Page for features/ datafields (Account# duplicate, ""Title"", ""First Name"", ""Last Name"", ""City"", ""Province"", ""Postal Code"", ""Phone"" and ""Email"") with buttons (""Save"", ""Save & Add another"" and ""Cancel"")

6) Click on Cancel

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Open URL: 
https://qa.hitekschool.com/lms/3106/loans/create

2) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

3&4) Navigate to ""Add Customer"" Page from ""Customers - Tauranga Branch"" page

5) On Add Customer Page add the details below: 
-- Account#: 1234567
-- Title: Mr.
-- First Name: ""Sal"" 
-- Last Name: ""Phill""
-- City:""Surrey""
-- Province: BC
-- Postal Code= XCVGH9
-- Phone: '2010054568' 
-- Email: user@domain.com

6) Click on ""Cancel""

7) Logout"	"""Add Customer"" page gives warnings for details on ""Add Customer"" Page for features/ datafields (""Account#""):
-- Account#: The 'Account #' already exists."	Automated		Yes
WF-TC-069	Validate User can be created with valid input	Medium	Functional	UI	URL is Open: [subdomain].hitekschool.com/lms/[build_number]	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""Users"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Users - [branch name] Branch"" / List for Users page opens

4-1) Type text [Username] in the search data field and click enter and observe results

4-2) Type text [First Name] in the search data field and click enter and observe results

4-3) Type text [Last Name] in the search data field and click enter and observe results

4-4) Type text [Company] in the search data field and click enter and observe results

4-5) Type text [Email] in the search data field and click enter and observe results

4-6) Type text [Phone] in the search data field and click enter and observe results

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) URL:  [subdomain].hitekschool.com/lms/[build_number] 
2&3) Reach: Users - 'Tauranga' Branch
4) Enter User Details
Username: jsmith0506
Password: jsmith@0506
First Name: Jonathan
Last Name: Smith
Company: Smartbank
Email: jsmith@smartbank.com
Phone: (666)777-8888"	"1) New User is created as an added line on Users - 'Tauranga' Branch page as:
Username: jsmith0506
First Name: Jonathan
Last Name: Smith
Company: Smartbank
Email: jsmith@smartbank.com
Phone: (666)777-8888

2) Login Data below can be used to login on URL page  ""[subdomain].hitekschool.com/lms/[build_number] "":
- Branch Name = ""Tauranga""
- User Name = ""jsmith0506""
- Password = ""jsmith@0506""
- Click on Radio Button ""Remember Me"""	Ready for Automation		Yes
WF-TC-070	Validate Customer can be created with valid input	Medium	Functional	UI	URL is Open: [subdomain].hitekschool.com/lms/[build_number]	"1) Open URL: [subdomain].hitekschool.com/lms/[build_number] 

2) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

3) Click on ""Customers"" link on the ""Navigation"" bar link in the top left corner

4) Reach on ""Customers- Tauranga"" page and click on ""Add Customer"" button on top right corner

5) Enter details on ""Add Customer"" Page for features/ datafields (""Account#"" , ""Title"", ""First Name"", ""Last Name"", ""City"", ""Province"", ""Postal Code"", ""Phone"" and ""Email"") with buttons (""Save"", ""Save & Add another"" and ""Cancel"")

6) Click on Save

7) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Open URL: 
https://qa.hitekschool.com/lms/3106/loans/create

2) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

3&4) Navigate to ""Add Customer"" Page from ""Customers - Tauranga Branch"" page

5) On Add Customer Page add the details below: 
-- Account#: 1234567
-- Title: Mrs. 
-- First Name: Adrian 
-- Last Name: Lekailo
-- Street: 34 Goto Road
-- City: Bumberton 
-- Province: Ontario 
-- Postal Code: L5E 6NO
-- Phone: (416)788-0000
-- Email: al@sample.com

6) Save

7) Logout"	"""Customers-Tauranga"" page generates a line (new row)for  columns:
- ""Account#"" = ""1234567""
- ""Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Phone"":  ""(416)788-0000"", 
- ""Email"" = ""al@sample.com"",
- Edit button
- Delete button"	Ready for Automation		Yes
WF-TC-071	Validate loan can be created, a central bank rate can be obtained and a prequalification letter can be viewed, saved and printed	Medium	Functional	UI	URL is Open: [subdomain].hitekschool.com/lms/[build_number]	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page with all the features: ""Summary Chart"", ""Total Approved"", ""Total Rejected"", ""Total Customer"" and ""Navigation Bar""

2)Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) Click on the button for ""Add Loan"" on the top right corner of the ""Loans - [branch name] Branch"" page

4) Enter valid input in all Data fields below:
4-1) ""Customer financial data"":
 - ""Customer Name"" dropdown
 - ""Monthly Income"" datafield
 - "" Monthly Debt"" datafield
 - ""Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""
- ""Term Years"" with 4 radio buttons for (2,3,5,10,15)
4-3) ""Returned Customer"" Radio button for Yes/ No
4-4) ""Central Bank Rate""
- ""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""
4-5) ""Preview Prequalification letter"" button
4-6) Click on Save

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2)Dashboard opens
3) Loans-Tauranga Branch opens
4)Enter Input on ""Add Loan"" page 
4-1) ""Customer financial data"":
 - Customer Name= Select ""Adrian Lekailo""
 - Monthly Income= ""5000""
 - Monthly Debt= ""1200""
 - Monthly payments of"" generated greyed out datafield
4-2) ""Loan Terms""- Term Years = Click on ""2""
4-3) ""Returned Customer= don't click
4-4) ""Central Bank Rate""
- Click on""Central Bank Rate"" red button 
- ""Central Bank Rate"" generated greyed out datafield
- ""Prequalified for principle of"" generated greyed out datafield
- ""Customer Interest rate""generated greyed out datafield
4-5) Click on ""Preview Prequalification letter"" button
4-6) Click on Save

5) Logout"	"""Loans-Tauranga"" page generates a line (new row)for  columns:
- ""Customer Name""= ""Mrs. Adrian Lekailo""
- ""Address""= ""34 Goto Road, Bumberton Ontario, L5E 6NO""
- ""Income/ Debt"":  ""Income= 5000"", ""Debt= 1200"", ""Monthly payments of = 467"" 
- ""Loan Terms"": ""Tern years =2"", ""Approved Rate: 7.50%"", ""Loan Amount: $50,377.00""
- ""Returned Customer"": empty checkbox
- PDF button
- Edit button
- Delete button"	Ready for Automation		Yes
WF-TC-072	Validate Search for User functionality	Medium	Functional	UI	URL is Open: [subdomain].hitekschool.com/lms/[build_number]	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""Users"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Users - [branch name] Branch"" / List for Users page opens

4-1) Type text [Username] in the search data field and click enter and observe results

4-2) Type text [First Name] in the search data field and click enter and observe results

4-3) Type text [Last Name] in the search data field and click enter and observe results

4-4) Type text [Company] in the search data field and click enter and observe results

4-5) Type text [Email] in the search data field and click enter and observe results

4-6) Type text [Phone] in the search data field and click enter and observe results

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Users"" on the ""Navigation Bar""

3) ""Users - Tauranga Branch"" Opens

4-1) Username = jsmith0506

4-2) First Name = Jonathan

4-3) Last Name =Smith

4-4) Company = Smartbank

4-5) Email = jsmith@smartbank.com

4-6) Phone = (666)777-8888

5) Logout"	"4-1) 1 result of jsmith0506

4-2) 1 result of jsmith0506

4-3) 1 result of jsmith0506 and
        1 result of Walter78

4-4) 6 results

4-5) 1 result of jsmith0506 

4-6) 1 result of jsmith0506 

5) Logout"	Not Run		No
WF-TC-073	Validate Search for Customer functionality	Medium	Functional	UI	URL is Open: [subdomain].hitekschool.com/lms/[build_number]	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""Customers"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Customers - [branch name] Branch"" / List for Customers page opens

4-1) Type numbers [Account#] in the search data field and click enter and observe results

4-2) Type text [Name] in the search data field and click enter and observe results

4-3) Type text [Address] in the search data field and click enter and observe results

4-4) Type text [Phone] in the search data field and click enter and observe results

4-5) Type text [Email] in the search data field and click enter and observe results

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Customers"" on the ""Navigation Bar""

3) ""Customers - Tauranga Branch""  page opens

4-1) Account # = 1234567

4-2) Name = Mrs. Adrian Lekailo

4-3) Address =34 Goto Road, Bumberton Ontario, L5E 6NO

4-4) Phone = (416)788-0000

4-5) Email = al@sample.com

5) Logout"	"4-1) 1 result of Mrs. Adrian Lekailo

4-2) 1 result of Mrs. Adrian Lekailo

4-3) 1 result of Mrs. Adrian Lekailo

4-4) 1 result of Mrs. Adrian Lekailo

4-5) 1 result of Mrs. Adrian Lekailo 

4-6) 1 result of Mrs. Adrian Lekailo 

5) Logout"	Not Run		No
WF-TC-074	Validate Search for Loan functionality	Medium	Functional	UI	URL is Open: [subdomain].hitekschool.com/lms/[build_number]	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Loans - [branch name] Branch"" / List for Loans page opens

4-1) Type numbers [Customer Name] in the search data field and click enter and observe results

4-2) Type text [Address] in the search data field and click enter and observe results

4-3) Type text [Income/ Debt] in the search data field and click enter and observe results

4-4) Type text [Loan Terms] in the search data field and click enter and observe results

4-5) Click Radio Button [Returning Customer] in the search data field and click enter and observe results

5) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Loans"" on the ""Navigation Bar""

3) ""Loans - Tauranga Branch"" page opens

4-1) Customer Name = Mrs. Adrian Lekailo
4-2) Address =34 Goto Road, Bumberton Ontario, L5E 6NO
4-3) Income: $5,000.00
4-4) Debt: $1,200.00
4-5) Payments: $467.00
4-6) Term Years: 15
4-7) Approved Rate: 7.50%
4-8) Loan Amount: $50,377.00

5) Logout"	"4-1) 3 results of Mrs. Adrian Lekailo
4-2) 3 results of Mrs. Adrian Lekailo
4-3) 3 results of Mrs. Adrian Lekailo
4-4)  1 result of Mrs. Adrian Lekailo
4-5) 1 result of Mrs. Adrian Lekailo
4-6) 1 result of Mrs. Adrian Lekailo
4-7) 1 result of Mrs. Adrian Lekailo
4-8) 4 results 
4-9) 4 results
4-10) 1 result of Mrs. Adrian Lekailo

5) Logout"	Not Run		No
WF-TC-075	Verify Dashboard Page opens with all its features	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Review all features on the Dashboard (homepage) of the WebLoan App

3) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Review Loading of 
- Summary Chart 
- ""Total Approved""
- ""Total Rejected""
- ""Total Customer""
- ""Navigation Bar"""	"Dashboard Page opens with all its features 
- Summary Chart 
- ""Total Approved""
- ""Total Rejected""
- ""Total Customer""
- ""Navigation Bar"""	Not Run		No
WF-TC-076	Verify User Logs out successfully and Login page appears	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User Clicks on ""User Role"" button on top right button and click on Logout button on the ""Dashboard"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on ""User Role"" button on top right button 

3) Click on Logout button on the ""Dashboard"" page"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Navigate to Logout button

3) Logout"	User Logs out and Login page [subdomain].hitekschool.com/lms/[build_number] loads	Not Run		No
WF-TC-077	Verify total customers are displayed	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Observe the ""Total Customers"" widget  on the Dashboard page

3) Click on the ""Customers"" link on the ""Navigation"" Bar on the top left corner

4) On the ""Customers-[Branch]"" page Observe the ""Total Customers"" 

5) Verify the (Count of the Lines of the ""Customers"" on the ""Customers-[Branch]"" page) is the same as (the ""Total Customers"" widget on the Dashboard page) 

6) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Observe ""10"" ""Total Customers"" widget  on the Dashboard page

3&4) Navigate to ""Customers-[Tauranga]"" page

5) Count ""10""  (lines on the ""Customers-[Tauranga]"" page) same as (""Total Customers"" widget  on the Dashboard page)

6) Logout"	Count "10"  (lines on the "Customers-[Tauranga]" page) same as ("Total Customers" widget  on the Dashboard page)	Not Run		No
WF-TC-078	Verify total approved loans are displayed	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Observe the ""Total Approved Loans"" widget  on the Dashboard page

3) Click on the ""Loans"" link on the ""Navigation"" Bar on the top left corner

4) On the ""Loans-[Branch]"" page count the number of lines  for ""Loans"" 

5) Verify the (Count of the Lines of the ""Approved Loans"" on the ""Loans-[Branch]"" page) is the same as (the ""Total Approved Loans"" widget on the Dashboard page) 

6) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Observe ""11"" ""Total Approved Loans"" widget  on the Dashboard page

3&4) Navigate to ""Loans-[Tauranga]"" page

5) Count ""11""  (lines of ""Approved Loans"" on the ""Loans-[Tauranga]"" page) same as (""Total Approved Loans"" widget  on the Dashboard page)

6) Logout"	Count "11"  (lines of "Approved Loans" on the "Loans-[Tauranga]" page) same as ("Total Approved Loans" widget  on the Dashboard page)	Not Run		No
WF-TC-079	Verify total rejected loans are displayed	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Observe the ""Total Rejected Loans"" widget  on the Dashboard page

3) Click on the ""Loans"" link on the ""Navigation"" Bar on the top left corner

4) On the ""Loans-[Branch]"" page count the number of lines  for ""Rejected Loans"" by opening the pdfs for each line

5) Verify the (Count of the Lines of the ""Rejected Loans"" on the ""Loans-[Branch]"" page) is the same as (the ""Total Rejected Loans"" widget on the Dashboard page) 

6) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Observe ""7"" ""Total Approved Loans"" widget  on the Dashboard page

3&4) Navigate to ""Loans-[Tauranga]"" page

5) Count ""7""  (lines of ""Rejected Loans"" on the ""Loans-[Tauranga]"" page) same as (""Total Rejected Loans"" widget  on the Dashboard page)

6) Logout"	Count "7"  (lines of "Rejected Loans" on the "Loans-[Tauranga]" page) same as ("Total Rejected Loans" widget  on the Dashboard page)	Not Run		No
WF-TC-080	Verify the loan chart displays correct data	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Scroll to the chart area and review monthly values

3) Verify the (Count of the Lines of the""Approved Loans"" and ""Rejected Loans"" as per the chosen month when all individual pdfs are opened for the ""Loans-[Branch]"" page) is the same as (the ""Total Approved Loans"" and ""Total Rejected Loans"" monthly values in the chart area of the Dashboard page) 

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Observe ""2"" ""Total Approved Loans"" and ""1"" ""Total Rejected Loans"" for ""current month""  toggle on the Dashboard page

3)  Count ""2"" & ""1"" (lines of ""Rejected Loans"" and ""Approved Loans"" for ""current month"" on the ""Loans-[Tauranga]"" page) same as (""Total Rejected Loans"" and ""Total Approved Loans""  for ""current month"" on the Dashboard page)

4) Logout"	Chart should display "2" and "1" for "current month" breakdown for loans requested, approved, and rejected	Not Run		No
WF-TC-081	Verify dashboard shows monthly loan trend	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Scroll to chart and view June data spike

3) Verify the (Count of the Lines of June month of the ""Loans-[Branch]"" page) is the same as (the June data spike in the chart area of the Dashboard page) 

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Observe spike for month of june""  toggle on the Dashboard page

3)  Count the (Count of the Lines of June month of the ""Loans-[Branch]"" page) is the same as (the June data spike in the chart area of the Dashboard page

4) Logout"	Chart should reflect correct values for June (e.g., 15 requested, 9 approved, 6 rejected)	Not Run		No
WF-TC-082	Verify branch name is displayed correctly	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) View the page title 

3) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) View  ""SmartBank Dashboard - 'Tauranga' branch""

3) Logout"	Page title shows: "SmartBank Dashboard - 'Tauranga' branch"	Not Run		No
WF-TC-083	Verify profile icon appears for logged-in user	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Check the top-right of the screen

3) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Check the top-right of the screen

3) Logout"	Profile circle with â€œAâ€ (admin) is displayed	Not Run		No
WF-TC-084	Verify year filter dropdown works	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the â€œCurrent yearâ€ dropdown near the chart

3) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on the â€œCurrent yearâ€ dropdown near the chart

3) Logout"	Dropdown expands and allows year selection	Not Run		No
WF-TC-085	Verify dashboard not accessible without login	Medium	Functional	UI	Not logged in	Directly enter dashboard URL: https://qa.hitekschool.com/lms/3107 in browser	URL: https://qa.hitekschool.com/lms/3107	Redirect to login page or show "Unauthorized access" error	Not Run		No
WF-TC-086	Verify chart handles for "Last year"	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) View the chart area

3) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Chart area is empty for ""Last year""

3) Logout"	Chart shows empty graph or "No data available" message	Not Run		No
WF-TC-087	Verify chart handles null/no data for "Last month"	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) View the chart area

3) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Chart area is empty for ""Last month""

3) Logout"	Chart shows empty graph or "No data available" message	Not Run		No
WF-TC-088	Verify user cannot access another branchâ€™s dashboard	Medium	Functional	UI	Not logged in	Attempt to change URL to another branch ID	URL tampering	Access denied or redirected to authorized branch only	Not Run		No
WF-TC-089	Verify logout behavior after session timeout	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	User session is idle for extended time	Wait for session to expire, then refresh dashboard	User is redirected to login page	Not Run		No
WF-TC-090	Verify graph is empty for a future date filter	Medium	Functional	UI	"User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on year dropdown > select future year

3) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) year = 2030 in filter

3) Logout"	Graph displays â€œNo dataâ€ message, UI remains stable	Not Run		No
WF-TC-091	Verify "Dashboard" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Dashboard"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Dashboard"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Dashboard"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Dashboard"" on the ""Navigation Bar""

3) ""Dashboard"" page opens

4) Logout"	Dashboard Page Opens	Not Run		No
WF-TC-092	Verify "Users" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Users"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Users"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Users"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Users"" on the ""Navigation Bar""

3) ""Users"" page opens

4) Logout"	Users Page Opens	Not Run		No
WF-TC-093	Verify "Customers" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Customers"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Customers"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Customers"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Customers"" on the ""Navigation Bar""

3) ""Customer"" page opens

4) Logout"	Customers Page Opens	Not Run		No
WF-TC-094	Verify "Loans" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Loans"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Loans"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Loans"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Loans"" on the ""Navigation Bar""

3) ""Loans"" page opens

4) Logout"	Loans Page Opens	Not Run		No
WF-TC-095	Verify "Events" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Events"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Events"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Events"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Events"" on the ""Navigation Bar""

3) ""Events"" page opens

4) Logout"	Events Page Opens	Not Run		No
WF-TC-096	Verify "Policies" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Policies"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Policies"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Policies"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Policies"" on the ""Navigation Bar""

3) ""Policies"" page opens

4) Logout"	Policies Page Opens	Not Run		No
WF-TC-097	Verify "About" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""About"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2)Click on the Link for ""About"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""About"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""About"" on the ""Navigation Bar""

3) ""About"" page opens

4) Logout"	About Page Opens	Not Run		No
WF-TC-098	Verify "Help" page opens	Medium	Functional	UI	"1) User is Logged in with 
- ""Branch Name"", 
- ""UserName"" and 
- ""Password"" 
and reaches the Dashboard page

2) User has Navigated to the ""Help"" page"	"1) Login with ""Branch Name"", ""UserName"" and ""Password"" and reach Dashboard page

2) Click on the Link for ""Help"" on the Navigation Bar on the top left corner of the ""Dashboard"" page

3) ""Help"" page opens

4) Navigate to User profile on the top right corner and click on the ""Logout"" link"	"1) Use Login Data below:
- Branch Name = ""Tauranga""
- User Name = ""admin""
- Password = ""sherwathe1122""
- Click on Radio Button ""Remember Me"" 

2) Click on ""Help"" on the ""Navigation Bar""

3) ""Help"" page opens

4) Logout"	HELP Page Opens	Not Run		No
WF-TC-099	Verify login fails with invalid credentials	Medium	Negative	UI	URL is Open: [subdomain].hitekschool.com/lms/[build_number]	"1. Navigate to login page
2. Enter incorrect Branch Name, Username, or Password
3. Click â€œLoginâ€"	"Branch Name = Taurung
Username = admin
Password = wrongpass"	Error message displayed, user not redirected to dashboard	Ready for Automation		Yes


